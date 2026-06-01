---
title: "Breakpoint 2025: Solana in the Multi-Chain World by NEAR Intents: NEAR Protocol (Illia Polosukhin)"
source: "https://www.youtube.com/watch?v=eKVklQBW09I"
date: "2025-12-13"
transcribed: "2026-04-29"
model: "whisper.cpp large-v3"
language: "en"
words: 1363
duration_seconds: 502
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 185
---

# Breakpoint 2025: Solana in the Multi-Chain World by NEAR Intents: NEAR Protocol (Illia Polosukhin)

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-13
**Duration:** 8 min
**Transcription:** 1363 words
**Model:** whisper.cpp large-v3
**Playlist position:** 185/199

---

## Transcription

 Okay. Well, thanks everyone who made it to the almost end of the day. Really excited to be here. For those who are not familiar with me, I actually, before jumping into blockchain rabbit hole, was AI researcher. I work at Google Research on, effectively, deep learning, machine understanding. And I'm one of the co-authors of Attention is All You Need, which is a paper that introduced Transformers, T and GPT.
 Now, in 2017, I left Google to start AI company. And we quickly realized that we actually need a blockchain so that we can coordinate and pay people around the world. Now, that's how we got to Neo Protocol in 2018. We actually were neighbors with Solana in San Francisco when we were starting. And today I want to talk about kind of cross-chain and what we've been building on the side and how we've been working with Solana.
 Cross-chain has been extremely painful. And if we look out, the reality is most of users have been sitting on centralized exchanges kind of historically for all of the time that blockchain existed. It's been too hard to use. If I have some Bitcoin and I want some Solana, if I have some XRP and I want some Near, there's gas costs. You need to figure out how to reach wallet to use, et cetera. There's a lot of risks that involve with this.
 I constantly fail. It's a lot of fragmentation that, you know, you never know is like, is this bridge actually works with this chain? Do I need another bridge to kind of go somewhere, et cetera? And at the end, like if you think of like Web3 wallets, right, the wallets that we actually use, for them, it's really complicated to support all of these routes, all of these different bridges. It, you know, kind of adds a lot of complexity on their side. And so that's kind of been the general feel of kind of multi-chain,
 multi- ecosystem where every blockchain and ecosystem became an island. They've been, you know, existing on their own. And it's really limited what we can do, right? And again, most users ended up just sitting on centralized exchanges and not benefiting from accessing DeFi. Now, what we brought in with Near Intents is effectively redefining how this experience works. We're really introducing new type of transaction. We call it an intent where you can actually express the outcome you want
 without needing to figure out how exact the execution is going to work, right? What you can do, you can say, hey, you know, I have some, for example, Solana. I want to buy some Zcash. I have some Bitcoin. I want USDT. And you effectively get matched with a, we call them solvers, effectively a market maker or an AI agent that is willing to take the other part, that is willing to provide this. Now, it was extremely important. This actually ends up
 very cheap because you can actually source liquidity from all of the sources, right? There's going to be market makers that are concentrating on Binance. There can be some prop trading firms that are taking a position, the reverse position. There's no MEV because this contract between you and the counterparty is done off-chain. And so now how do you actually ensure that the security of this is done, right? And this is what kind of the infrastructure
 that Nier has been building for the past few years comes in place where we have thresholds, multi-party computation. This enables to actually custody assets across different chains. We have trusted execution environments for verifiable and confession computing. We use it for kind of running services as well as AI and kind of an economic incentive to deploy this. So this is a very simple API to really enable this for any wallet or an application. And we're already working with a number of chains as well as a number of
 wallets and distribution channels, right? I think we have 28 chains now. We have more coming. All the major ones are already integrated as well as, you know, Trust, Ledger, Infinex, Skybar, et cetera, are being using Nier Intents to really access all of this liquidity and all of those different assets as effectively providing a centralized exchange experience to decentralized users, kind of self-custodial users. So really exciting. It's been great.
 It's been growing extremely. It's been doubling every month since we launched it kind of end of last year. We just, I think, crossed 3.6 billion in the last 30 days as well as the number of transactions and actions and intents we're processing. Super quickly, for those who are technical and want to understand how exactly it works, you kind of request what outcome you want and you're effectively getting matched. Like, it gets distributed to market makers and solvers.
 They're willing to take that trade. You're effectively making, you know, a contract with them. So that is happening off-chain. So this can happen, you know, within 100 to 100 milliseconds. You can really quickly get to this agreement. And then you effectively settle on-chain, for example, from Solana, send the assets to the address that's controlled by multi-party computation that gets recorded on Nier. The trade gets executed and settled. And then the asset gets distributed back.
 And then the asset gets distributed on, for example, Zcash to your shielded wallet into directly your private vault. So this kind of experience, really smooth, kind of from a developer perspective, really easy API. And from a user perspective, a trader perspective, probably the fastest way to trade across chains directly into their self-custodial wallets. Now, intents are not just for trading, right? The trading is definitely the first use case where this is the most painful experience. But we actually, this week, launched
 here with local Abu Dhabi blockchain ADI, the travel intent-driven commerce, where you can actually specify natural language intent, where, you know, I want to fly from Abu Dhabi to London. And, you know, I'm going to spend like three days there. And I want to visit some museums. And you have now solvers, AI agents coming in and proposing you the itinerary. And then also executing the actual booking and doing all the actions on the back. This also then gets extended to e-commerce,
 to actual contractual service work, right? So really intense is kind of this new paradigm to find the counterparty and get agreement with them and really settle it and execute it across different spaces. Now, I'm really excited. We're already working with a number of Solana projects. So Encryptrade actually announced it today, you know, on stage that they're using Near Intents to really bring privacy to other assets. And they've been using it for Zcash already on Solana.
 We've been working with Radium as well, where Zcash been brought to Solana and traded on Radium and kind of the older arbitrage and coming back to Zcash is done through Near Intents. And the same with Orca, been really powering this. So all in all, what we're trying to build is really this unified liquid layer where you can actually plug in into any chain on any kind of asset beyond
 blockchains into Web2 and then really introduce this to all of the user interfaces, wallets, applications. And kind of the way we expect this kind of continue evolving is that I'm as a user will be able to come in with any wallet, right? Be your Solana wallet or Near wallet, Bitcoin wallet and use any application, right? And all of the kind of execution machinery that's going to happen, going to be abstracted out and happen. Also, the one I forgot is
 SolSwap, which is also a Solana specific Near Intents interface. You can connect to Solana wallets and trade all of these assets in one place. So check it out. If you're a developer, this is extremely powerful infrastructure for you to use. And if you're a user trader, this gives you access to all of the assets across the whole market. Thank you.
