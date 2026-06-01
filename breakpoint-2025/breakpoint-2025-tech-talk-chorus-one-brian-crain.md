---
title: "Breakpoint 2025: Tech Talk: Chorus One (Brian Crain)"
source: "https://www.youtube.com/watch?v=O1nZh0vg1VI"
date: "2025-12-12"
transcribed: "2026-04-27"
model: "whisper.cpp large-v3"
language: "en"
words: 1610
duration_seconds: 720
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 061
---

# Breakpoint 2025: Tech Talk: Chorus One (Brian Crain)

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-12
**Duration:** 12 min
**Transcription:** 1610 words
**Model:** whisper.cpp large-v3
**Playlist position:** 061/199

---

## Transcription

 Cool. Well, thanks so much for coming. I appreciate you being here. I think there's some competition somewhere else for this talk. So thank you so much. So yeah, so the Solana vision, right, is basically to create this internet capital markets where you can have people from all over the world create applications, transact with each other, potentially accommodate all kinds of economic activity. But for that to happen, right, the network underneath also
 needs to perform at a certain level. So today I want to look at a bit where is Solana right now in terms of its performance and capacities and what are the main changes that are coming up that really will get this network to the place where it's sort of fit for the Solana vision. So yeah, briefly about ourselves. So we've been deeply involved in Solana since the very beginning. Met Tolian Raj in like 2018, invested in Solana. We were there at the very first test nets.
 We were there at the very first test net. We were there at the very first test net.
 We'll talk a bit about that. So first of all, high level, where is Solana today? So we have seen Solana really improve tremendously in the last years. Even from the beginning, Solana had these ideas of 400 millisecond block times. But it wasn't the reality for years. Really, it was like 600 milliseconds, 500 milliseconds. And it took years to get us to the point where actually the network, if you look at this year, was really consistently below those 400 millisecond target. So tremendous improvement on that side.
 We've also had skip rate, right? In the past, we had a lot of issues with stability, blocks being skipped, I mean, downtime as well. So that has gotten way better. And today, skipping blocks has become a rare event. And of course, Solana has consistently high economic activity, a lot of transactions. So I think today it's around like 400 transactions from users per block. And it's definitely probably the most used of all time.
 And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well.
 And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well.
 And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well.
 And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well.
 And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well.
 And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well.
 And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well.
 And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well.
 And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well.
 And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well.
 And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well.
 And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well.
 And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well.
 And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well.
 And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well.
 And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well.
 And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well.
 And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well.
 And I think that's one of the reasons why Solana is doing so well. And I think that's one of the reasons why Solana is doing so well.
 you
