---
title: "Breakpoint 2025: Tech Talk: SevenLabs (Kellian Vitré)"
source: "https://www.youtube.com/watch?v=ffIOaK4bAqk"
date: "2025-12-12"
transcribed: "2026-04-27"
model: "whisper.cpp large-v3"
language: "en"
words: 1436
duration_seconds: 523
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 062
---

# Breakpoint 2025: Tech Talk: SevenLabs (Kellian Vitré)

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-12
**Duration:** 8 min
**Transcription:** 1436 words
**Model:** whisper.cpp large-v3
**Playlist position:** 062/199

---

## Transcription

 I'm Kélian, co-founder at 7Labs. Today I'm going to be talking about Carbon, the data pipeline for Solana. So, Carbon is a Rust framework to build indexes on Solana. Just for more context, we've been a dev shop for about two years on Solana, and about a year ago, we realized that a lot of teams were basically just rewriting the same pieces of code. So, for sourcing data, be it historical or real-time data,
 for decoding it from their IDL, and also for processing it, so like storing it or triggering workflows. So, that's when we started actually building Carbon, and the goal was to have a single pipeline that is modular and that you can just plug things into. So, just so you get a bit of an understanding of how you actually compose a Carbon pipeline, you can plug in any data source, and here we actually support most of the ways in the ecosystem
 to get data. You can then attach decoders for instructions and accounts. This will directly use your IDL, and then you can add processors, like for Postgres storage, or it could be really anything, and then you just run the pipeline end-to-end. So, as you can see in the code, you have a simple builder pattern. You can choose your source, then add the instruction and account pipes, and you have your indexer ready to run. So, let's get into each of the components a bit more deeply.
 So, for example, if you have an info provider, or if you have a local dump of data, you're able to simply ingest it into your pipeline by implementing that trait. But, of course, for most people, they don't want to do that. They want to just use something that's already implemented,
 and there are standard ways to actually get data to index. For real-time data, that would be gRPC, and for historical data, there's been a lot of teams pushing it this year. So, as the ecosystem grows, we actually maintain and publish a lot of different crates for data sources. So, I think this year there's been a lot of teams pushing historical data.
 So, we've integrated that. That means you can pretty much just for free stream historical transactions to your carbon pipeline, and that's at very high speeds. So, that's a good one. And then on the vendor side of things, you have Helios that has released, like, get transactions for address as a new RPC endpoint. And so, these are all methods that you can directly plug into Carbon.
 And you'll get the data inside your pipeline. So, that's an example of how you would do it. This would be for just from a data source. So, as you can see, you just choose your slot range, you choose your filters, and you're able to add it to your pipeline. Would work the same way with other data sources. You'd simply import another crate. So, then at that point, you have all of your raw data flowing inside your pipeline. And so, you need,
 then, to make sense of it, because that is the main point of Carbon, actually. It's getting all of your updates and then doing what you want with them. So, here, again, you have two traits inside the framework, but you don't really have to implement them. You could implement them if you want a custom digitalization logic, pretty much. What you can do, and what most people should do, is actually use the CLI. So, the CLI works with any IDL. So, we support anchor and column IDLs, and it will basically
 generate the whole decoder implementation from that IDL. That means you can then just import the code that's been generated and add it as an instruction or account pipe, and you'll have all of your decoded account or instruction updates for your program directly flowing to your pipeline. Once you've done that, you just need to do whatever you want to do with that data, and that is the part that, actually, you will spend most times writing when you're using Carbon. So,
 this is also a trait that you can implement, and you can do whatever you want inside of it. The good thing is, basically, you get all of your decoded updates, and you can use it. So, here, you have a logger implementation, as an example. So, what this would do is actually load the decoded updates, and it would also log some transaction metadata. So, you have access to the whole instruction or account update, all of the metadata that you need, and
 most importantly, your decoded type. So, something that's cool, actually, about the CLI is if you generate your decoder through the CLI from your IDL, you have a Postgres feature that is already implemented inside the generated crate. And so, if you enable it, you'll be able to directly use our Postgres account or instruction processor, and you'll be able, basically, in a few lines of code, to have a full
 index of all of your accounts and instructions in, like, a few lines of code inside Postgres. So, here, you just use the migrations inside of the generated crate to generate your tables, and then write this pipeline, and you'll have pretty much everything running. You just need, like, a gRPC connection to whatever info provider. So, this wraps it up for how you would actually use Carbon, and I recommend that you
 guys also use the Scaffold command on the CLI to try to generate a project and, like, play with it. But it's really simple to use, and after about a year experimenting with the API of the library, we're going to go to V1. So, we're going to have a stable API across all core crates. We're going to follow a simulating versioning finally. We've had a performance update with, like, more than 5x in raw pipeline throughput, which
 is really cool. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput.
 We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput.
 We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput.
 We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput.
 We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've had a performance update with, like, more than 5x in raw pipeline throughput. We've
