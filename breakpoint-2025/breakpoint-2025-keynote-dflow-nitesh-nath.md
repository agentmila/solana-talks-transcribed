---
title: "Breakpoint 2025: Keynote: DFlow (Nitesh Nath)"
source: "https://www.youtube.com/watch?v=O0VYopeDMhk"
date: "2025-12-12"
transcribed: "2026-04-27"
model: "whisper.cpp large-v3"
language: "en"
words: 1326
duration_seconds: 576
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 060
---

# Breakpoint 2025: Keynote: DFlow (Nitesh Nath)

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-12
**Duration:** 9 min
**Transcription:** 1326 words
**Model:** whisper.cpp large-v3
**Playlist position:** 060/199

---

## Transcription

 Hey, everyone. How's it going? So here today to talk to you guys about our latest work, tokenizing predictions. Earlier this month, we released the Dflow Prediction Markets API, which is powered by Kalshi. And I want to tell everyone here a little bit more about how it's built, what to expect from it, and what's coming up in 2026. Before we get into that, though,
 let me talk a little bit about the background, what Dflow actually does, what we're building, and what we spent 2025 doing. So Dflow builds low latency trading infrastructure. What this means concretely today is we operate a Solana DEX aggregator. We aggregate 100% of liquidity on the network, construct a very large graph of prices, and then solve a very difficult optimization problem in order to determine the best routes from a token a user wants
 to give up for a token that they want to receive. This year has been pretty phenomenal for our growth. We have facilitated over 33 billion in trading volume since April 2025. We've contributed a lot to the app revenue that applications on the network have received. Month over month growth has been very strong, and we've serviced over a million users across the globe.
 In June of 2025, we released our Dflow Spot Trading API. This is our Solana DEX aggregator, which we aggregated the spot tokens on the network from and released this API so that applications and wallets could access the liquidity from the network. It took us about six months. And in June of 2025, we had four applications integrate our Spot Trading API. At this point in time, we had about $4 billion in cumulative volume
 that we had processed for the network through our contract, and about $2 million in revenue paid out to applications. In June of 2025, we also released sort of our new backend. This allowed streamlined DEX integrations. It was a quiet release, but it let us integrate DEXs very quickly. By September of 2025, we had 26 applications integrate the Dflow aggregator.
 We processed about $10 billion in cumulative volume, and we had paid $16 million in app revenue out. In September of 2025, we also released what I think is Solana's most exciting microstructure improvement of 2025, just-in-time routing. Just-in-time routing was a zero-to-one mechanism that was released on the network. At this time, just-in-time routing let a transaction, which was previously frozen,
 become dynamic on-chain at the time that it was processed. This led to drastically better execution for users, a lot of save price slippage that was returned to users' wallets, or that could be captured by applications in application revenue. By October of 2025, we had processed $18 billion in cumulative volume, and we had paid out $24 million in application revenue.
 We released both, and at this point in time, we had also expanded the team quite a bit. In October of 2025, we released a new prop-AMM integration backend. We spent a lot of time thinking about microstructure on the network. Prop-AMMs, as you heard from Ben before this, have been a very integral part of the process of providing great execution on-chain, spreads that are tighter, indeed, than Binance. This integration, this new backend, allowed prop-AMMs to integrate
 super smoothly into Dflow's routing, accessing features that were not available anywhere else, such as just-in-time routing. By November of 2025, last month, we had over 75 applications integrate, with $33 billion in cumulative trading volume, and over $34 million paid out in application revenue. Super exciting. Earlier this month, in fact, a few days ago,
 we released the Dflow prediction markets API, powered by Calshi. So what exactly is this? Calshi, as you guys know, is a prediction market operator. They operate prediction markets in sort of an off-chain, regulated way. And the Solana network is sort of where some of the world's most opinionated and active traders live. Dflow is the connective tissue, and in particular, our prediction markets API is the connective tissue
 between traders on the Solana network and the liquidity that lives on Calshi. So what does this actually mean for users? I think starting this month, and there will be a pretty exciting announcement later today, you guys should keep your eyes peeled for, Solana users will begin to receive market access to one of the most liquid prediction markets exchanges in the world. In exchange, Calshi receives access to some of the most
 of the most regulated, active degens that the world has ever seen. But how do we do this? We tokenize Calshi, but how does this actually work under the hood? So under the hood, we have released what we're calling a concurrent liquidity program. A concurrent liquidity program is something that will actually glue liquidity from off-chain sources like Calshi to the network in a way that when a user actually trades,
 with a concurrent liquidity program, they're receiving a token, an SPL token that actually represents their position. In the case of a prediction market, they can redeem these tokens for stable coins. The way this is done is in a multi-transaction flow. The first transaction that actually opens the order increases the user's position, escrows some of their funds, the second transaction
 that facilitates the trade actually performs the fill, mints them the token representing their position. Similar multi-transaction flow when it comes to redeeming the stable coins. The position is burnt in the prediction market case, and the user receives stable coins if their prediction was correct. So why is tokenization important? Tokenization was a choice. In building this prediction markets API, we did not need to tokenize, but we felt it was really important
 to do. And we didn't have a clear sense of why exactly it was important to do, but we understood the serendipitous nature of tokens and DeFi. The fact that you can compose liquidity, compose tokens, and have novel mechanisms designed by anyone was just phenomenal. So we took a bet on serendipity, and this is also a bet on the imagination of
 builders on Solana, and we tokenized Cauchy's prediction markets. So some of the ways in which I expect this sort of serendipitous nature of tokenization to take form is in perhaps borrow lending protocols, in sort of new liquidity formation mechanisms. You know, we've seen some really cool stuff come out of nowhere in the past, such as pump. And we've also seen sort of like more serious, but also
 very exciting things like prop AMMs come. We are very excited to see what builders on Solana do with prediction tokens. The last sort of thing category here is a party emoji. We have no idea what is coming next, but we're very excited for it. Not only are we excited for it, builders are very excited for it. So to date, we have over 100 integrations lined up, most of which will be going live
 in the next quarter, a lot of which will be going live this month as well, some of which will be going live or at least being announced today. From the builders that we've been talking to, we've seen some really exciting applications come up. Social trading has been a common theme. Applications that address sort of niche markets within sort of prediction markets, which are very general. Data vendors have reached out to us. Group trading applications.
 I think a lot of people here interact with each other in Telegram. And there are some really novel things you can do with prediction markets that are on chain and then accessible through things like Telegram. We've also seen interest in yield products. So what can you do today? You can go and look at the prediction markets API. You can get started. And then reach out to us, and we will help you
 build whatever you can imagine. Thank you.
