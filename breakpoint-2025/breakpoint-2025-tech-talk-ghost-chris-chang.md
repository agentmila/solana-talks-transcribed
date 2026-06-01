---
title: "Breakpoint 2025: Tech Talk: Ghost (Chris Chang)"
source: "https://www.youtube.com/watch?v=_VPQHv5WRP4"
date: "2025-12-12"
transcribed: "2026-04-28"
model: "whisper.cpp large-v3"
language: "en"
words: 1394
duration_seconds: 609
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 086
---

# Breakpoint 2025: Tech Talk: Ghost (Chris Chang)

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-12
**Duration:** 10 min
**Transcription:** 1394 words
**Model:** whisper.cpp large-v3
**Playlist position:** 086/199

---

## Transcription

 - Hello, my name is Chris Chang, co-founder of Ghost, also the team by Sandwich.me, the Solana Mev Data Hub. Today, we'll be demystifying the inner works of prop AMs. Prop AM now represent 90% of aggregated swap volume. They're a hot topic on Solana. And today, we will pop the hood and discover how they work
 and then show you how to reverse engineer them. And then we'll zoom in and look at the cat and mouse game between Toxic Flow and prop AMs. So what is prop AMs? Let's read it quickly. Prop AM looks like just another AM from a user's perspective, but they behave more like an on-chain market makers with active coding logic. They're closed source with private strategies and curves.
 They actively manage inventory, end quote. They don't take deposits and they oftentimes don't have front end. So you usually interact with them through aggregators. Some aggregators lean on prop AM more than others, but they all make a big on them because their price is great. Prop AM are very cool. They allow for permissionless swap.
 It's very competitive because they call very tightly. And all they call is very cheap. And so they can react very quickly. Generally, we see about two to four prop AMs that dominates the industry. But landscape can ship very quickly. So we became very interested in prop AM about nine months ago. Since then, we improve our simulation and infra and build visualizer on Sandwich.me.
 So let's dive into the tech. For given prop AMs, we want to build a quote function that takes input, direction, and relevant accounts. And then go from there to get the output amounts as you would get if you swap on-chain. So we don't want to run SVN simulation to get the answer. The goal is to create a readable Rust port of a swapping logic.
 So prop AM don't provide decoded or open quote interface. To see the output at any given time, you kind of have to swap or do the simulation. But we don't want to do that, right? It doesn't reveal the how. So what we want to do is that it's to educate you guys. It's fun. And closed and obfuscated sources can raise the bar. But they shouldn't be impossible to read.
 So let's talk about some important gotcha. There isn't a universal quote. Different signers and transaction composition can actually lead to different outputs. More on this later. So before going over the tools and technique, let's go over one of the popular prop AMs and how they work. You probably already heard or maybe even used Schoomfile. So let's look at how it works and think about it as a Oracle anchor market maker.
 With some controls. So one is the inventory control, which keeps reserve at a target. And flow control, which really means how much can be traded at a given price tier per slot. Now the orange value up there are from the pool parameters. Still Oracle protection is explicit. If core is too far away from the Oracle functions,
 the core simply refuses to quote. So on layer one, we have stuff on Oracle. Layer two, adjust price based on this reserve and desired reserve. Layer three, we penalize quotes as Oracle becomes stale. And layer four, we have execution across up to 10 lanes. And think about each lane as a separate tranche of liquidity of its own spread. The pool fell from the base tranche first,
 and then slowly walked down the ladder. So 10 lanes per side. Each with its own cap, meters, and PPN spread. By the way, PPN is parts per million. There's also building backfill logic, where next slot, after being consumed, refill half of the lane's capacity. And then the following slot after that, if it hasn't been consumed again, then refill completely.
 And you can see why quoting is not smooth. It's actually piecewise with explicit state per lane limit. And think about total out as a result of filling your order across 10 lanes, right? We scan from zero to nine. And if the lane's full, then skip it. Otherwise, we take as much as we can and then fill it in. And for the slide, we compute an out I
 which using the lanes quote, and then add it to the total out. And then the final total out then is the sum of the slide by slide fills. So now let's dive into how to reverse engineer one of them. So three pillars that we have in mind, we have simulator, trace, and static. A simulator is to execute transactions on the known state, right? And a trace is our fork of
 SBPF, which instructs the VN and log structure trace of what happened. And statics, we decompile the on-chain program using binary ninjas, high level intermediate language. And then lastly, we tie everything together using an AI eject. So everything is based on an awkward simulator. You need to be able to answer what would this guy use again, running the state and this input mount.
 SBPF is fork where we instruct the VN. And then so that every meaningful action such as function call return account rewrite operation, the output is a trace pocket file. From the trace, then we can then rebuild the code summary. Here we see a summary of a Tessera V swap, which you can see which function were invoked and how often, as well as how many times each function reads right to the stack, the heap,
 and the data. It's a nice bird's eye view. With just the trace, we can then instantly follow the output backward and figure out how it was built up. And this is often a nice starting point because then you can see how obfuscated a program is or isn't, and then get a sense of what's happening here. And now we can use the tool like binary ninja to decompile the prop NN, which you then need to install a plugin from AutoSec.
 Dump the on-chain program and then select the learner. Tessera V has 415 functions, but a swap only touches 68. We use our code summary to explore those functions and then putting everything together into a repeatable prop pipeline. One script simulate a swap and then write a full report bundle. And then the idea is that for every single swap simulation, it becomes a case file for your AI agent to consume.
 Or you can read it. Topologically sorting code trees also means that agent can start from the ground up, translate them first, and then keep on going up. The AI agent would get to get all the traces, metadata, decompile code. It's a good layer. So now, let's talk about prop AM, actually, and the toxic flow. When we look at atomic ops and exclusively touch prop AM,
 we can count for five to 10% of atomic op revenue. And reacting to toxic flow is one of the top priority for prop AM. And some prop AM actually give a different output depending on which aggregator program and method that involves the swap. Many prop AM, the instruction, use the instructions this far to inspect full transactions, who calls me, and what other swap I present and ordering.
 So here's an example of a swap. It's a web listed router, apply PPS penalty. Tessera V, missing a property, don't run, about two BPS penalty. If another prop AM swap is in the same transaction, human five may add 25 BPS. And then so five, three, two, 3.6 BPS. This is involving and cycle continues. So here's a bot that has full discrimination. They start from one transaction to multiple transaction now,
 and they have their own bundle. And then we look into atomic ops that has grown, and now it's the majority. And as you can see here, top pools, it lasts 30 seconds. And lastly, be on the lookout for unique data set coming soon. The data will execute every unchanged transactions, swap, a prop AM against other prop AMs, and then what the output will have been. And then kind of like ideal post factor G, to understand the gap between execution
 and achievable execution. Thank you so much.
