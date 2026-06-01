---
title: "Breakpoint 2025: Scaling the Read Layer to 1M TPS: FluxBeam / FluxRPC / RugCheck (Scott Hague)"
source: "https://www.youtube.com/watch?v=JQTr1ezjM24"
date: "2025-12-13"
transcribed: "2026-04-29"
model: "whisper.cpp large-v3"
language: "en"
words: 1008
duration_seconds: 309
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 177
---

# Breakpoint 2025: Scaling the Read Layer to 1M TPS: FluxBeam / FluxRPC / RugCheck (Scott Hague)

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-13
**Duration:** 5 min
**Transcription:** 1008 words
**Model:** whisper.cpp large-v3
**Playlist position:** 177/199

---

## Transcription

 So, I'm Scott. I'm the technical co-founder over at Flux or Flux Beam Ecosystem. And over the past year, we've been working with RPC issues. So, after seeing the demos from FireDancer last year, we realized there's going to be a big issue coming up around we can do the 1 million TPS from the ingestion side, but how do we then read all of that data coming through? So, when we look at the legacy approaches and what we've done for the past three or four years, this has typically been a load of kind of nonsense
 on voting validators with a RPC bolt-on stacked on top of each other, and then clients are just routed and directed to each one of these individual RPC layers. Now, while that's kind of worked, we've started to see cracks in that implementation. I think a lot of you have probably called get program accounts on pump fun and be met with pretty much silence because of the data load. And this gets even worse when you look at multiple clients fighting for this resource on this validator. This ends up resulting in lagging slots and stale data.
 We've had the whole issue around leader tracking. This is one of the main causes of that. And for us, working on latency-sensitive applications for stuff like rug check, this has been a real pain in our side. So, we decided to rebuild the entire RPC layer from the ground up, focused on three key premises, scalability, reliability, and performance. So, at the core layer, we've decoupled everything from the consensus layer. So, you can now scale the read layer independently from the consensus
 and voting side of the validators. This means you no longer need to stack up a load of really expensive hardware. You can actually do this on commodity hardware. It works perfectly in the cloud. And we've also worked on the bandwidth side to ensure that you're not getting huge egress bills as well. The benefit of all of this is, as it's basically a microservice architecture, we've got a huge amount of redundancy at each layer. And it actually allows us to pump out layer one data for everyone. So, you're no longer getting kind of this hierarchical
 data, but you're actually getting a lot of data when you're going to get your data through the original methods. But this still has its issues. When we look at kind of dApp development from Web 2, pretty much every single developer will be familiar with having your database and your data right next to your server. In Web 3, we like to do things the difficult way. So, over the past couple of years, everyone's basically been either calling out over the network every single time they need a piece of data or reinventing the wheel for the 50th time, indexing Yellowstone streams and having to
 manage all of that infrastructure internally, which is a little bit fragile. So, this is where Lantern comes in. And this has been our key focus over the past couple of months. Lantern's your local RPC that's tailored towards your dApp. So, no longer do you need to ingest the entire firehose of Solana data. You can pick and choose exactly what you need and then stream that in in real time into your data center right next to your app and then call it locally. So, zero latency means better UX for everyone.
 So, not much drop-in replacement for whatever you're using today. We've gone full to the fully compliant RPC side. So, whether it's WebSockets, Yellowstone, normal RPC calls, we'll even have webhooks coming in in a later development stage and direct to TPU transaction sending, just in case you want to avoid the toxic order flow that's going on at the moment from other providers. Lantern has you covered. And all of this in a really minimal resource footprint. If you actually pop out to our booth that's in the layer one over there, we've got Lantern
 running on a physical Lantern. So, even on a Raspberry Pi, you can stream in pretty much all the market data from Solana, no problem at all. And that basically breaks down into three stages of how we've built this. We started off with a validator fleet. We've got our own custom fire dancer tiles that ingest all of that data in, into our scalable ingestion engine powering both the public RPC, but then we've gone one step further. We've introduced what we call Delta Stream. And instead of sending you all the account updates of all the pieces of data
 over and over again, we're only sending you the bytes that change. So, rather than needing a 10 gig pipe, you can do this on 100 megabyte pipe. So, egress, ingress, a lot cheaper, a lot more scalable. If you need more TPS or RPS, you can just scale out these Lantern instances even more. And it's got intelligent subscriptions. So, if you get data coming in or you require data that's not quite cached in Lantern, it'll automatically detect that, set it up on the scale of an ingestion pipeline, and then Delta Stream will run it through.
 So, once you've got your data set up and you're good to go for your application. When we look at the results of that, from a public RPC side, you're getting about a 20% reduction in cost from normal RPCs. If you're running private RPCs, that's more like 80, 90%. So, no longer do you need to pay a couple of grand a month for these RPC servers. You can run Lantern locally. And this gives you 99% decrease in resource requirements, but most importantly, 99% reduction in latency. So, if you're interested in discussing more, please do reach out at the link below.
 You can't meet us in person, and we're also at the booth outside. But, yeah, thank you very much for listening, and I hope to see you soon.
