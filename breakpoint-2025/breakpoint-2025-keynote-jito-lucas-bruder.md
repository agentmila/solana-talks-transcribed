---
title: "Breakpoint 2025: Keynote: Jito (Lucas Bruder)"
source: "https://www.youtube.com/watch?v=2gTdXSKSAOQ"
date: "2025-12-11"
transcribed: "2026-04-27"
model: "whisper.cpp large-v3"
language: "en"
words: 857
duration_seconds: 418
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 028
---

# Breakpoint 2025: Keynote: Jito (Lucas Bruder)

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-11
**Duration:** 6 min
**Transcription:** 857 words
**Model:** whisper.cpp large-v3
**Playlist position:** 028/199

---

## Transcription

 My name is Lucas Bruder. I'm the co-founder and CEO at JITO Labs. I'm here to talk about BAM today. BAM is Programmable Infrastructure for Internet Capital Markets. Solana is winning the speed war. This is pretty clear. We've seen a 6x increase in transactions per second over the last few years.
 Thanks to the hard work of all the Solana core engineers from Onza, Fire Dancer, and all the great apps on Solana. On the right here, you can see the block space increase over the past few years on Solana. At the beginning of this year, we were around 48 million compute units, went to 50 million compute units, 60 million compute units.
 Past then, I think it's going to continue to go exponential. Speed alone isn't enough, though. Markets need more. There's a few properties we think markets need. They need to be transparent. People need to know the rules of the market, how the market works. They need to be fair. This is very important. Same rules, consistently applied. It needs to be verifiable.
 It needs to be provable. Don't just promise it. They also need to be customizable. We think that different markets have different needs. We think that BAM can help solve some of these issues. BAM's a transparent, verifiable, and customizable scheduler for Solana. There's two main pieces for BAM. There's the BAM node, which schedules transactions
 inside of trusted execution environments. They produce cryptographic attestations so you can get the verifiability that I mentioned on the last slide. And BAM validators will execute those transactions. The really cool thing about BAM is plugins. I mentioned different markets, different needs. BAM will support customized sequencing rules for those applications on Solana. This is commonly known as ACE, or Application
 Controlled Execution. And we're also exploring a lot of interesting and unique transaction primitives that we think will upgrade Solana. There's a few key properties for BAM that we care a lot about and that provide a lot of value to Solana. We talked about plugins, custom sequencing logic. Applications can define their own markets through ACE. It's provable. You can know how it works.
 You can get attestations from the system to understand the software that's running, understand the market. And anyone can verify. The code that's running is what it says it is. It's private. Transactions are encrypted through secure hardware on the trusted execution environment. It's also very performant. Today we're running around seven BAM nodes. We envision tens or hundreds run by many operators.
 The performance overhead from BAM is very small. And we get all of these properties thanks to TEs. BAM's the sandbox for innovation. I mentioned Application Controlled Execution. This allows on-chain applications to implement their own ordering rules, create their own market microstructure. A common example here is Maker Priority.
 What this allows applications to do is provide better markets for makers. Ultimately, this results in better prices for users. ACE allows the market microstructure to become fully programmable. And we think that when any asset can be traded on Solana, any market and application can define its own rules, then Solana will become the best venue to trade any asset, including the securities that Michael was just talking about.
 Today, BAM's running on 8% of stake. It's processed tens of thousands of blocks over the past few months in hundreds of millions of transactions. We see performance comparable to other Validator clients on the network. So where are we going with BAM?
 We're working on BAM's Application Controlled Execution. This is something that we're going to start working on very shortly. It's the most requested feature from applications on Solana, from Prop AMMs to Perp DEXs and other trading-intense venues. I mentioned Verifiability. We're working on something that we internally called BARS. This is the BAM Attestation Report Service. This lets you understand the market and the software that's running inside of BAM.
 So traders can understand how the system works. A very important part of BAM is open sourcing the software. This is something that we're working on. We expect it to be open sourced within a few months. Decentralization is extremely important. And we'll be working on supporting multiple operators to onboard to BAM and run it across the world.
 Finally, we'll be working on IBRL. So this includes faster software, better performance, FireBAM, which is our FireDancer implementation of BAM as well. There's a lot of work to do. Job's not finished. If any of this interests you, if you're a Validator, you can scan the QR code, take you to bam.dev to learn more. If you're an application developer, please scan that.
 It's happy to learn more about your needs, what you want to see on the market. And if you're an engineer and any of this interests you, if you want to work on very high-performance systems, you want to help make Solana the best place it can be, the other QR code takes us to our job page, hiring a lot of engineering right now. So please apply. That's all I have for today. Thank you.
