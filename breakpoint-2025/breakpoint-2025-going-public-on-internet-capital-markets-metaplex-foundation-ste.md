---
title: "Breakpoint 2025: Going Public on Internet Capital Markets: Metaplex Foundation (Stephen Hess)"
source: "https://www.youtube.com/watch?v=5L_aU_1FNUs"
date: "2025-12-12"
transcribed: "2026-04-27"
model: "whisper.cpp large-v3"
language: "en"
words: 1354
duration_seconds: 531
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 069
---

# Breakpoint 2025: Going Public on Internet Capital Markets: Metaplex Foundation (Stephen Hess)

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-12
**Duration:** 8 min
**Transcription:** 1354 words
**Model:** whisper.cpp large-v3
**Playlist position:** 069/199

---

## Transcription

 Good afternoon, everyone. My name is Steven. I'm the founder of Metaplex, director of the Metaplex Foundation. Today, I'm excited to talk about going public on the internet capital markets, or in short, how to launch a token on Solana in the right way. To start, it's important to note that internet capital markets isn't just a tagline. We're in the middle of a fundamental change in global capital and market structure, with
 over $3 trillion in crypto assets today and growing. And importantly, people are actually using blockchains to trade at scale for the first time, not just to hold tokens. This is important because if you can only access crypto assets through centralized exchanges, we've failed in providing open and borderless finance. Here you can see it's not just on-chain trading that's increasing, but a major trend from
 centralized to decentralized venues. And Solana is the clear breakout winner in this trend, with over a trillion dollars in DEX volumes this year. Along with this boom in on-chain trading, we're seeing an explosion in stablecoins. There are now over $14 billion on Solana in stablecoins, providing the liquidity and demand that new tokens rely on.
 And if you look at this, you'll see that most of those launches are still a disaster. Insider manipulation, extractive middlemen, and bad economics are rampant. And on top of this, most tokens are effectively launched off-chain, in paper docs with private investors that then provide a constant source of sell pressure once the token is made broadly available. And trust in these launches is at an all-time low, and reasonably so. The market is trained to expect rugs and scams, so founders get almost zero benefit of the doubt
 and you have to get absolutely everything right. And after the Libra launch and a few other high-profile rugs, it was clear that we had to do something about it. So earlier this year, we got to work building the first version of what is now the Genesis protocol, a fully on-chain framework for effective and fair token launches on Solana. And to be clear, this isn't our first rodeo. Metaplex is one of the largest tokenization platforms
 in the world, used to create over 20 million tokens and more than 800 million NFTs on Solana, more than any other protocol by far. And like with many of our most successful products, we reached out to the best teams in Solana to get to the root of the problem, and we started building. Our first launch was with DeFi Tuna, an innovative AMM that supports limit orders and more effective monetization for liquidity providers.
 And in less than four minutes, we saw 5% of the supply sell out, bringing in $2.5 million to the project. And Genesis doesn't just handle the sales process in this type of launch, but also gives verifiable token economics and programmatic graduation of liquidity for the tokens that are then distributed to the team and other stakeholders.
 This mechanism worked perfectly for a DeFi protocol where a community-first and fair capital formation process was needed. And this was also the first time we saw the true potential of what we were building. Fair launches aren't just about fairness. They're about creating the right incentives to accelerate product usage and fundamental value. That's really the superpower of tokenization and decentralized systems, is getting your community in early and aligning incentives. We then asked ourselves, well,
 if you don't have strong conviction in how the market will value your token, how can you actually achieve real price discovery on-chain? And this led us to our first experiment with Collector Crypt on the first launch pool. Collector Crypt is a collectibles protocol. Think of it as an on-chain platform for discovering and trading digital collectibles. For their launch, we helped Collector Crypt deploy a 48-hour launch pool, where during that time, anyone could deposit or withdraw from the pool.
 Token allocation clears at the implied price. So with 5% of the supply up for sale, Collector Crypt brought in $3.4 million with over 600 backers participating. And anyone who wanted an allocation could get one. And it felt like almost overnight on the entire timeline, people were talking about Pokemon card tokenization as this new launch cohort was then bringing in the next wave of users. However, one of the issues with launch pools is that you don't know exactly where the launch pool will clear.
 And that's not really acceptable for some traders that need reliability in terms of exactly where their bids will execute. This led us to our first uniform price auction. In short, a uniform price auction is a better Dutch auction. In this auction, participants had 48 hours to place bids. And the entire allocation clears at the lowest successful bid. Exotic Markets is a structured products platform on Solana. And we worked with them to deliver what was the first truly on-chain auction
 for a new token launch. And this mechanism is perfect for projects where the buyers are large funds and traders that need guarantees around where their bids will settle. So you can see how the mechanism matters depending on the type of project. So for DeFi Tuna, they needed fast but fair capital formation. So the price sale was perfect. Collector Crypt was a community-driven platform. And so they wanted to bring as many people in as possible. And so the launch pool was perfect. Exotic Markets, it was really important
 for larger funds or institutional traders that they can actually have a guarantee around price execution. And so the price auction was the best mechanism. And each of these mechanisms solves a different problem. That's why Genesis doesn't force a one-size-fits-all. There are many different asset types. And so, of course, there are going to be different launch strategies and mechanisms that meet the needs of these projects. OK, so we built a launch pad. Not exactly. So Genesis isn't a launch pad.
 It's a launch protocol. And our vision is that launching a token should never require going through a single gate or a single platform. There will be thousands of apps with embedded launch pads for different types of assets priced in any Solana token. Exchanges, both centralized and decentralized, will be able to support new token launches that are fully on-chain with advanced tools. And when you launch your token on Solana using Genesis, it's immediately aggregated and distributed across hundreds
 of wallets, exchanges, and trading terminals. Solana wins by becoming the ubiquitous and the de facto platform for launching, discovering, and trading new tokens. And that requires a base level primitive for launching tokens that just works. To reach that vision, I'm excited to announce today that the first public launch of the Genesis SDK is now live. Thank you.
 Genesis SDK is for applications. It's for exchanges that want to build their own specialized launch pads. It's for aggregators that want to monitor and alert traders as new token launches hit the chain. Any app can integrate and immediately have access to fair launch smart contracts. There's literally no excuse for a botched token launch ever again. For anyone in the audience that's a developer building an app that involves launching tokens, if you're a pre-TGE project that's looking to build a novel launch
 experience or a trading app or aggregator, I encourage you to check out genesis.metaplex.com to access our just-launched developer docs and guides. Shout out for the team that's pushing code overnight. And as always, you can drop into Discord, ping us on X at Metaplex, and we're here and happy to help. From supporting the first digital collectibles and art on-chain to powering the NFT boom to meme coins to DeFi to stable coins, we now clearly
 find ourselves in the internet capital markets era for Solana. Our conviction is that upstream of everything is fair launching tokens with real value. And with that problem solved, there's nothing stopping the on-chain markets from becoming the center of price discovery, global commerce, and borderless finance. Thank you.
