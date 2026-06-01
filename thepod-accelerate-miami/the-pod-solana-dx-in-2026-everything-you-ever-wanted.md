---
title: "The Pod: Solana DX in 2026: Everything You Ever Wanted"
source: "https://www.youtube.com/watch?v=5iVM7NfWncw"
date: "2026-05-15"
transcribed: "2026-05-31"
model: "whisper.cpp large-v3"
language: "en"
words: 1240
duration_seconds: 528
tags: [transcript, thepod, accelerate-miami, solana]
series: "ThePod at Accelerate Miami"
series_index: 009
---

# The Pod: Solana DX in 2026: Everything You Ever Wanted

**Event:** [ThePod at Accelerate Miami](https://www.youtube.com/playlist?list=PLilwLeBwGuK5N62XjqHAnWE3S72SZYc4o)  
**Date:** 2026-05-15  
**Duration:** 8 min  
**Transcription:** 1240 words  
**Model:** whisper.cpp large-v3  
**Playlist position:** 009/9

---

## Transcription

 This talk is about how to get everything you ever wanted in Solana as a Solana developer. It is not a vendor talk, it is relevant to everyone who is building, regardless of what company you use for blockchain infrastructure. I'm Mike, I work as a Solana developer relations at Quicknode. If you've seen videos on LightSVM or using Anchor and SolanaKit together on YouTube, it was probably me. We're going to talk about three things in the next 15 minutes. The first is why developing on Solana is still painful.
 Partner organizations have done about it. And the third thing is how you can join us in making your own Solana developer experience everything you ever wanted. So let's have a quick overview of where things are at right now. In the last year or so, a bunch of things have changed for the better. Anchor is finally on a stable Rust. Testing has swapped from JavaScript to Rust and LightSVM is now 100 times faster than Mocha was. JavaScript and TypeScript is now confined to the client and has moved to SolanaKit. But there's a few things that could be better.
 The first is that the biggest library of Solana programs until very recently used various versions of everything, going back to Anchor 0.26 from four years ago, which is approximately 900 years in blockchain time. That might seem okay because it's a programming example, you don't care. But keep in mind that GitHub is used to train LLMs. So if programming examples is out of date, and most production open source is also using older versions of Anchor, there's no good source of current training data for Solana programs.
 So Claude and Codex will still generate bad Anchor code out of the box. The next point is that Web3.js is not very well maintained and is everywhere. It has 1.4 million weekly downloads, which is nearly double what Kit has. It has a bunch of issues, including audit issues from transitive dependencies. And Web3.js also isn't particularly nice. It misses sensible defaults like getting a recent block hash every time you need to make a transaction.
 So people didn't want Solana Kit. Here's a really basic task, connecting to an RPC, getting an airdrop, and sending a transaction. The code came from a library that I didn't make to ensure this is a neutral test. Tokens are measured by the TypeScript compiler, which is a more accurate representation of code complexity than lines of code. And this is Solana Kit. It's nearly twice the size of Web3.js for most common tasks.
 It's already incredibly verbose. Most Kit libraries were still worse than Web3.js, so people stuck with Web3.js rather than use Kit. Separately, there's a general lack of financial education. Program education, and I'm criticizing myself here, is generally hello world escrow. And it's true, once you've managed escrow, everything else is downhill. But that downhill part is now completely on your own. The other thing is that a lot of Solana education ignores the libraries we all depend on.
 We don't use single user wallets for large amounts of funds in production. We use multisigs, which are generally squads. And if we have a prediction market and we need to send funds to somebody when they make a successful bet after the event has been settled, you would probably use TukTuk to schedule a call to an instruction handler rather than manually invoking an instruction handler. But most Solana education is weirdly fixated on the idea that Anza and Foundation are the only people that make open source.
 So if we're going to have 10 or 100 or 1000 times more people use Solana in the future than now, that means their ability to learn Solana matters more than our own ability to handle a little bit of discomfort.
 So we have pubkeys, which are explicitly not valid values for pubkeys. We have instructions, which are the input for program functions. And those program functions are also called instructions. It's a tautology. We waste attention by having concepts like program ID. What's a program ID? It's a program address. Why didn't you just call this a program address? That's already terminology. Basic things should not be hard to understand. And we are conditioned by the chewing glass meme to think there is value in things being hard, but not everything.
 I know people on Twitter would say that AI fixes everything. AI helps, but it's no panacea. AI output for Solana, as we've mentioned, is generally low quality because it's trained on GitHub, which is outdated and low quality. We waste context on adding skills to make models with bad training weights perform reasonably on Solana. And we wrap broken code to isolate it, but that doesn't fix it. You still have dependencies on broken, outdated, unmaintained code. So far, things aren't great, but if you wanted to hear people grumble about Solana, you could have just jumped on X.
 What are we actually doing about it? The first thing is that QuickNode took over the Solana program examples repo and ported just under 50 projects to the latest version of Anchor, added light SPM tests to every project, remapped it to the multiple files layout that is used in new Anchor projects, deleted all the Mocha-based Web3.js tests, sped up CI. So if you change a single program, it's going to take 20 seconds, not 20 minutes for CI to run. We also added examples for all programs using Quasar.
 We also added examples for all programs using Quasar.
 We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar.
 We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar.
 We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar.
 We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar.
 We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar.
 We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar. We also added examples for all programs using Quasar.
