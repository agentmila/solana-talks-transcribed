---
title: "Breakpoint 2025: Anza Block: Alessandro Decina"
source: "https://www.youtube.com/watch?v=dLNVmnW5izQ"
date: "2025-12-12"
transcribed: "2026-04-28"
model: "whisper.cpp large-v3"
language: "en"
words: 1171
duration_seconds: 476
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 095
---

# Breakpoint 2025: Anza Block: Alessandro Decina

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-12
**Duration:** 7 min
**Transcription:** 1171 words
**Model:** whisper.cpp large-v3
**Playlist position:** 095/199

---

## Transcription

 All right. Just in case anyone is wondering what it's like working with Trent, I recently discovered I have anxiety to ship. We were having a conversation on Slack where I was profiling Agave 3.0. And I saw a slowdown, which we fixed. And so I was making sure that we backported the fix to 3.1. And yeah, this is what I get from Trent, to which I'm like, you're welcome, Trent.
 So today, I do want to talk to you about some of the things that I am very anxious to ship and that we're shipping soon, starting from XDP, which is actually in 3.0. We've been telling you, we've been asking you to test, because this is the one thing that will allow us to increase block space. I don't know if you remember, but at Accelerate, I showed you some performance profiles of XDP while we were doing some load testing. In the meantime, we've been doing some actual testing on both testnet and mainnet.
 And we measured that a turbine with XDP is as far as 200x faster than the legacy turbine with sockets, which is amazing. And you've also been helping us in testing different drivers and hardware. And we found some bugs, and we have fixed those bugs. So this was me sending a patch to the Linux kernel, fixing a bug in the Intel driver. And I have a patch coming for the Broadcom driver as well.
 So I'm mentioning this, because we are literally the only team across all of blockchains sending patches to the Linux kernel, right? Probably something. The AF XDP that we created for Agave is not only usable within Agave, but it's a standalone reusable general-purpose crate for Rust. And so it can be used by any projects.
 And so we've been doing some performance tweaks. So we've been doing some performance tweaks. And now we're planning on integrating this code in TPU in Q1 next year. So we will also start ingesting transactions using XDP soon. Also, the guys over at the Overclock Validator, one of my favorite validators. So please go stick with them.
 They just released ShredCaster, which is a JITO ShredStream-like crate project that can be used to stream shreds outside of Turbine. But because it uses XDP, it has much lower overhead and sends with a much lower latency. So if you're using JITO ShredStream, consider also checking out ShredCaster, which uses Agave XDP. Another huge thing that we just very recently released is WinCode. As you may know,
 WinCode is deserialization format used by Solana, both in protocol, regrettably, and by on-chain applications. WinCode, as far as the bitwire format goes, is pretty good. It's not too bad. But the implementation is extremely slow. This has been a longstanding issue in Agave because, you know, often we found bottlenecks in WinCode-related code, and we had to fix them. And this happened like dozens of times until
 a couple of months ago when Zach, tired of fixing the same bug over and over in different spots in the code base, created WinCode. WinCode went from not existing to being the second fastest Rust serialization library in the first release. Obviously, when we saw that, we all went to Zach, and we told him that we were extremely disappointed that it was second fastest. So the second WinCode release is the fastest Rust serialization library
 available today. Also, to accelerate, you might remember I showed many profiles, including a profile of Agave crossing the epoch boundary. At the time, I don't remember exactly what release we were running on my net, but it used to take more than two seconds to cross the epoch boundary due to some computations that we have to do right at the boundary. I told you that we were starting
 to look into them, and yeah, we've been looking into them. Now, in master, we can cross the boundary in less than 400 milliseconds. We are very close to not skipping slots anymore. We still sometimes do skip one slot, but Michal is working on a fix so that we will never skip blocks again. Shout out to Horan and Michal for the amazing work they've been doing here. This is probably the most exciting change that is coming to
 replay in Agave. This is 10 seconds worth of profiling Agave while doing replay of mainnet transactions, actual mainnet load. If you see the red lines, the red markers in the profile, each one of them is a disk operation, right? In these seconds alone, there's over 1,100 disk operations, right? That is bad because every time you hit the disk, you need to wait for the IO request to complete, so that adds jitter to
 both banking and replay. And also, it's bad for the lifetime of your disk, right? The more we write, the sooner your disk wears out. This is the same profile with the code in master, and I actually believe that we backported most of the fixes to 3.1. You can barely see the markers. In these 10 seconds, there's less than 80 IO operations. So great work, IO people.
 The base is probably the component that has improved the most in the last year. Because when I first started this performance push almost two years ago, whenever I tweaked something in Agave and I wanted to recompile and restart the validator to see whether my fix was effective, I would have to wait more than half an hour to restart. And I would go to Brooks and complain, like, why does it take so long to restart a piece of software? It's like mental, right?
 I'm so obsessed with restarts. Maybe just don't restart. And I was like-- But this is where we are today. It used to take more than 30 minutes to restart 1.x. 2.x restarted in less than 10 minutes. 3.1 will restart in less than a minute. And 4.x will restart in less than 30 seconds. And this is only with the changes we've done to the accounts DB. It does not include some changes that we're planning to do to replay and repair. So we will restart even faster.
 And finally, at Accelerate, towards the end, I showed you some bugs in the scheduler, including this one, where the scheduler is actually busier doing some overhead synchronizing with POH instead of actually executing transactions. So in this specific profile, we're spending 61% of the time, the banking time-- so while Agave is a leader-- just doing this overhead, not actually scheduling transactions.
 So 3.1 instead. We have completely fixed the bug. And the workers are busy. They're processing transactions for 91% of the time. And the remaining 10%, you just need to send more transactions, OK? This is how that conversation ended with a trend. I love 3.0. It's the fastest release we've ever done. 3.1 is so much better. And I can't wait to release it. Thank you.
