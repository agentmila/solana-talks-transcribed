---
title: "Breakpoint 2025: Anza Block: Alexander Meißner"
source: "https://www.youtube.com/watch?v=eMIPEUi3oWM"
date: "2025-12-12"
transcribed: "2026-04-28"
model: "whisper.cpp large-v3"
language: "en"
words: 997
duration_seconds: 445
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 098
---

# Breakpoint 2025: Anza Block: Alexander Meißner

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-12
**Duration:** 7 min
**Transcription:** 997 words
**Model:** whisper.cpp large-v3
**Playlist position:** 098/199

---

## Transcription

 So today I'm going to talk about all the things you need to know for the next roughly half a year that we're going to change. Because we at the SVM team, we develop as the name implies, the SVM. So what we try to do is improve mostly bandwidth and performance in terms of throughput. There's not so much we can do in terms of latency, unfortunately. We try to reduce protocol complexity.
 Which helps mostly other valid data implementations like Firedancer catching up. And also it reduces attack surfaces and therefore improves stability and robustness. And finally, a point which we have been ignoring a bit too much in the past, which we're trying to do better now, is improving usability for you guys. All right. But unfortunately, all medicine has side effects. And there are things we need to do, and specifically also you need to do,
 so that we can unlock the performance gains and the robustness gains we want to have on our chain. Specifically, we are going to introduce mandatory for all programs, even the deployed ones, a few new restrictions. All of these should not be done in the same programs. But for some historic reasons, they are, for example, part of the SDK or have been. So please, please test.
 Your programs with a recent or hopefully most recent test validator and all feature gates enabled. And some of you will see these three error messages. And the fixes for them are pretty simple, but they need to be fixed. Specifically, I want to call out programs here. And if you find yourself in there, that means that your program is not going to break entirely. But some of the instructions will fail.
 So please take a look and run the latest test validators. But again, there's an upside to all of this. What we are planning next after that is so-called API v2, which will allow us to expose most of the transaction information all the time, basically for free. That includes the sign-offs and all the pub keys in a transaction. We will change that you will have to do account metadata
 changes through syscalls. That means you have to kind of adjust some parts of your program. In turn, you gain basically unrestricted resizing of accounts. No more limits in terms of 10 kilobytes. You get a lot cheaper entry points. You get a lot cheaper CPI and a lot simpler CPI. So we're getting rid of account info. And we're also getting rid of the pub key and the account meta, which we will replace by an index.
 So furthermore, we're going to introduce SPPF v3, which for you guys mostly just means you have to recompile your program with the latest toolchain once. And that should be it. There should be no changes to the actual source code. And hopefully, then, your programs will simply become much smaller. And furthermore, it will also allow you to use more different toolchains because you're much closer to other--
 eBPF tool links, especially the upstream LLVM. So then we have further protocol complexity reductions. Specifically, the loader is going to change. There will be an overhaul of the upgradable loader. That means both inside how the account layout works-- we have to do that to unlock some performance gains in the load data--
 and also to what specific actions you can do in the upgradable loader. The entire thing is codenamed loader before. If there will be an actual change to the owner, we don't know yet. The thing will be opt-in in the beginning and then become mandatory later. Specifically, I think what a lot of you are looking forward here is after that, you will be able to completely close and reclaim program accounts, including the address and including
 all fans, like entirely deleting the account. And existing workflows, like the buffered redeployment, will continue to function. All right. Further improvements we want to do for you guys, there has been a lot, quite an increase in interest for debugging, specifically, and also for code
 coverage tooling. So we have been working with our partners and trying to improve the situation there. And I think we're close to enabling debuggers to even go through CPI throughout an entire transaction stack. Furthermore, there have been some changes. For example, there is this issue that you have to pass all the instruction accounts before you get to the instruction data.
 We now also pass in the instruction data pointer as one of the arguments. So you will be able to first discriminate your instruction and then pass your instruction accounts or skip them entirely. And now the most interesting part probably is we will be able to rise the limits of the CPI nesting depth from 4 to 8. And we will be able to rise the number of instruction accounts in CPI from 64 to 2955, which means you
 can CPI all accounts simultaneously of the entire transaction at once. All right. Finally, a few things which we are looking forward to in the future is we're still on the mission trying to basically migrate all the built-in programs we have to core programs being deployed on-chain in BPF itself. And specifically, that includes, like I mentioned, the loader. That also covers the vote program.
 And the proof program. And we have been looking into potentially exploring different ISAs or more compiler options and a few more complex performance optimizations, which probably are not too interesting for you guys. But if all of you have anything that has always been on your mind, like this is the feature I need in the SVM.
 And I've been dreaming of this all my life, essentially, then please come to us. Meet us on Discord or on the SMPTE discussion groups or simply after the talk. You will see me because I'm wearing red. All right. Thank you, guys.
