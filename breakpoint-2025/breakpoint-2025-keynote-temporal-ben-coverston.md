---
title: "Breakpoint 2025: Keynote: Temporal (Ben Coverston)"
source: "https://www.youtube.com/watch?v=Wo5xNy8cEmw"
date: "2025-12-12"
transcribed: "2026-04-27"
model: "whisper.cpp large-v3"
language: "en"
words: 1274
duration_seconds: 632
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 058
---

# Breakpoint 2025: Keynote: Temporal (Ben Coverston)

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-12
**Duration:** 10 min
**Transcription:** 1274 words
**Model:** whisper.cpp large-v3
**Playlist position:** 058/199

---

## Transcription

 Centralized markets don't fail loudly. They fail quietly. Centralized markets, they fail with small skews, invisible advantages, and decisions no one can see. That's exactly the problem
 in Solana's block building infrastructure today. Less competition doesn't just reduce efficiency. It erodes trust. So instead of rebuilding a better monopoly, we rebuilt the market. I'm Ben. I'm the co-founder and CEO of Temporal and Harmonic.
 We're revolutionizing block building on Solana through a marketplace. So let's zoom out a little bit. Let's just talk about internet capital markets for a second. We've come a long way in the last five to six years. Crypto was supposed to escape Wall Street. Instead, we've kind of started to rebuild it. But in order to compete with centralized markets, which are incredibly efficient, we need to be able to innovate,
 and experiment with new market structures. Solana and new market structures are our best shot at doing this extremely efficiently. So let's talk a little bit about how far we've come. TVL is up multiples in 2024. And even in 2025, we've seen incredible inflows. Network and app revenue are exploding as usage
 and fees scale. Solana is no longer a chain labeled for degens and meme coins. Solana is a chain for institutions. We have the Bitwise Solana spot ETF with over $600 million in inflows in just the last few months. And that's just one of the ETFs.
 We have Solanate here in the UAE. And we have several others. Solana is becoming the world's exchange. We can clear tens of thousands of trades per second at near zero cost. Anyone in the world can plug in. There's no seat licenses, no membership tiers. Just free, permissionless, and open for all. Wall Street-grade markets.
 Programmable, global, and open. So something we recently built was this DEX called Humidify. I won't talk too much about it, because we have a dedicated Humidify presentation in about four hours by one of the other Humidify co-founders, Kevin Pang. But the thing that I kind of want to drill into everyone's heads is that this thing is quoting tighter than Binance, at least for retail. Retail can go on Solana and get tighter spreads than they would
 get on Binance. Average fills on the order of just a few bps. This thing is doing 60% of all spot volume on Solana. And we're just getting started. So prop AMMs are a pretty unique market structure. So they're essentially smart contracts on chain. But the difference is they're kind of actively managed liquidity.
 So the problem is that the liquidity just kind of sits there, reacts to trades, think like x, y equals k. But prop AMMs, like Humidify, they are actively managed by a sophisticated trader that's kind of sitting in the back end. And this is actually really good, because we get institutional-grade liquidity. We can stack up 10 plus 20 of these all in one router. And router gets a last look and just says, hey, give my user the best price.
 M&Ms also come with a lot of demands. We need fast inclusion. We need predictable ordering. We need millions and millions of TPS. We need fair access, no rate limits. We need a new architecture in order to create this kind of infrastructure. So again, as volume and institutions grow, incentives concentrate, small set of players can dominate block construction, quiet off-chain deals,
 decide who get the fast lane. Validators risk becoming dumb pipes. Stakers get table scraps. Applications get unpredictable inclusion and latency. So let's talk a bit more about Harmonic now. First of all, I want to hit home that it's very, very fast. Market makers like Humidify need high throughput. They need low latency. It's exactly what Harmonic delivers. Not only can we do ACE and make sequencing decisions
 in TPS, but soon with the advent of Harmonic Transformer Layer 2.0, we'll enable the whole system to operate at that throughput, not just the sequencing logic. So for anyone that's paying attention on mainnet, you may have seen us doing some experiments. We're experimenters, after all, at Temporal and Harmonic. And so over the last few days, we've just put out some blocks to kind of demonstrate the power of this thing. And so you guys can all go look at this mainnet
 block right now on mainnet. 385921704 and a few others. These are blocks that are completely full of Humidify Oracle updates. A block full of 10,000 of them. 25x more than the average mainnet block today. We're bringing a new kind of capacity to this network. And it's going to enable new market structures and tighter spreads.
 And we're going to be able to build like we've never seen before. So how does it kind of work, right? Well, so instead of the validator being locked into a single block builder, we essentially aggregate blocks from up to end builders in real time. Validators select the best block according to their preferences. And they replace a single builder monopoly with a market.
 And so we get validator income. We get better user outcomes. We give apps more control. And we improve network performance. So essentially what apps and decks like Humidify want is that they want to be able to get in really fast. They want the execution to be fair. They want their inclusion to be predictable.
 They want stable rewards. And they also want to have a lot of control over what's in their blocks, right? And in Harmonic, they can kind of set all their preferences and say, hey, this is kind of how I want my block to be constructed. This is what I want to achieve. And then we as Harmonic, we say, OK, this is what the validator wants to achieve. Our job is to now align these incentives with all the applications. Applications like Humidify. So we give apps and users fair execution.
 And then we make the changes. Solana becomes an open market and the world's exchange. So to reiterate what we believe in, right? Block building kind of resembles high frequency market routing, right? You look at all the centralized exchanges like NASDAQ, like NYSE. These guys are fast, right? These guys are capable of also doing millions of TPS, right? Maybe you won't see that on the average day.
 But this is fast infrastructure built by some of the best performance engineers in the world. Solana needs the same. There's no better way to achieve this than competition. This empowers validators to choose. And this also empowers applications to receive fast, fair, and deterministic execution. It's important for Mev to be transparent.
 It's important for Mev to be controlled. With Harmonic, all of this is out in the open. We are building a ton of tooling. And some of you guys may have seen more recently some of the demos and previews of some of the tooling that we're building to make block building more transparent and to overall make Solana as a protocol more visible to the average user. Solana can out-compete sexes because it is a base layer.
 It's a market. And once again, to reiterate, again, Solana can host Wall Street scale markets on chain. Humidify has already proved that these markets can beat sexes. And now with Harmonic, we're going to make competition rather than capture the default of the base layer.
 So Solana is where it is today because its apps compete. Its borrow lens compete. Its routers compete. Its clients compete. And now its infrastructure competes. The market is open. Thank you.
 ♪ ♪
