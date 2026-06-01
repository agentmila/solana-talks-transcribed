---
title: "Breakpoint 2025: Keynote: Ellipsis Labs (Eugene Chen)"
source: "https://www.youtube.com/watch?v=KBXjNFRnVzA"
date: "2025-12-11"
transcribed: "2026-04-27"
model: "whisper.cpp large-v3"
language: "en"
words: 1268
duration_seconds: 557
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 007
---

# Breakpoint 2025: Keynote: Ellipsis Labs (Eugene Chen)

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-11
**Duration:** 9 min
**Transcription:** 1268 words
**Model:** whisper.cpp large-v3
**Playlist position:** 007/199

---

## Transcription

 - Hi, everyone. I'm the CEO of Ellipsis Labs. I'm really excited to tell you about what we have coming next. At Ellipsis Labs, our mission has always been to build better markets, better than what we see on centralized venues today. You maybe haven't heard too much about us as a company, and that's really been by design. For the whole history of the company, we've really focused on being
 intentional about focusing on the work rather than focusing on the noise. And a lot of our products sit in the background. But we've been able to deliver some pretty remarkable things to the market so far. And if you've ever traded on Solana, odds are you've already interacted with some of our products without even knowing about it. When we started Ellipsis Labs, liquidity on Solana was dominated by passive AMMs.
 Market structure innovations were happening on Ethereum, despite the fact that the design space on Solana was a lot less constrained. Solana's high throughput and low cost allows us to build products that are only possible on Solana, even though that design space has been quite unexplored. And so the opportunity that we saw was to build active liquidity on Solana, which would give traders better prices.
 So we created a fully on-chain order book on Solana. This was the beginning of Solana's transition from passive liquidity to active liquidity. Again, the whole point was to bring better prices to Solana's traders. So the core metric that we care about, because our users care about it, is cost. This chart shows the price impact on a $1 million Solana trade, fully on-chain. Before Phoenix, this million-dollar trade would cost about 30 basis points
 of price impact. And after Phoenix came out, that same trade cost only about 15 basis points in price impact. So we were able to cut the price impact in half by improving liquidity primitives, which therefore improves the quality of liquidity on the chain. So Phoenix taught us a lot about both building and trading on Solana. We're able to learn the pain points for Solana's liquidity providers, as well as Solana's developers, and we're able to deliver
 the most positive outcome to the users. All those learnings led us to build SolFi, which began the prop AMM revolution in 2024. With passive AMMs, all the trading logic is very simple, and it lives fully on-chain. Whereas with on-chain order books, like Phoenix Spot, the trading logic lives fully off-chain. The key innovation with SolFi is to put some of the trading logic on-chain, some of it off-chain,
 and be very selective about it, depending on the properties of the trading strategy. And again, the core thing that this allows us to do is to quote tighter spreads and larger depth than what we were able to do on Phoenix Spot. SolFi is the first step function improvement in on-chain microstructure since Uniswap v3. Today, prop AMMs have eaten all the majors market share on Solana. Here you can see the light purple of prop AMMs
 eating the dark purple of other AMMs on Solana, and we've been able to also still keep all the liquidity fully on-chain. And with SolFi and all the other prop AMMs, today you can trade that same million dollar Solana trade for just five basis points of price impact.
 And at the beginning, I mentioned the goal was to make on-chain trading competitive with centralized exchange trading. And it turns out we're actually already there. The same trade on Coinbase costs 12 basis points plus exchange fees. The same trade on Binance costs five basis points plus exchange fees. This prop AMM market structure innovation was truly only possible on Solana. On Solana, we're able to compete for order flow based on price,
 and we're able to build anything that we want to on Solana permissionlessly. But our work here is far from over. At Ellipsis Labs, we're still continuing to improve the spot market structure, which I'm not going to tell you about today. I'm here to talk about something else. I'm excited to finally announce what we've been working on in 2025.
 I'm excited to introduce Phoenix Perpetuals. What we've done for the Solana spot markets, we're now doing for derivatives.
 The reason we're building Phoenix Perpetuals is the same reason we built all of these spot products in the first place. Today, if you're making that million dollar Solana trade on Solana Perpetuals, you're going to pay about 15 basis points in price impact. This number is three to five basis points on centralized exchanges, and our goal is to bring that all the way down. Phoenix Perpetuals is a non-custodial, fully on-chain perpetuals exchange.
 It's a user experience as the number one most important thing, which means building a truly best-in-class on-chain product. That means verifiable execution, all at the speed of Solana. It means gasless trading for retail traders. And of course, our specialty, an exchange, is nothing without its liquidity. So we're bringing the prop AMM market structure innovations over to Solana derivatives.
 On Phoenix Perpetuals, market makers can provide liquidity more cheaply than on other on-chain venues. And we've created a market structure that fosters competition between market makers to drive spreads down, while allowing them to dodge toxic flow from toxic traders. And that's all in service, again, of creating the best outcomes for our end users, just like we did on spot trading.
 Phoenix Perpetuals is a product that's only possible because of all of the great teams that make up the Solana ecosystem. At the base layer, we have Onza and FireDancer, making the base layer more performant and more robust. We have teams like Jito making sequencing deterministic. We have the Phantom and Privy and many other teams allowing users to self-custody their assets without sacrificing UX.
 We have a robust asset layer that already exists on Solana, as well as a battle-tested spot margin layer. And Phoenix sits on top of all of these great teams. But the thing I'm personally most excited about with Phoenix is that Phoenix Perpetuals is fully on-chain and fully composable, just like all of our other products, which means that anyone can build on top of Phoenix. Anyone can build on top of our on-chain liquidity. Anyone can build on top of our on-chain risk engine.
 We have a lot of opportunities for the community to build on top of Phoenix. Some ideas that I am personally interested in seeing and personally excited about include vaults, PERP-based options, some form of gamified trading, some form of social trading. But ultimately, it's really up to the rest of the community. When we started this company, we were just running market structure experiments on-chain. Solana was the best place for us to run the experiments. We had no idea what type of impact we would be able to make.
 Over the last three years, we've delivered these game-changing spot products, and now we're incredibly optimistic about the future of PERPs on Solana. And I don't think there's a team better place to build that future. So Phoenix PERPs is actually live today. We have a closed private beta, and we're actively onboarding users off of the wait list now.
 So you can sign up for the wait list through the QR code on the left. And if you'd like to chat with myself or the rest of the team, please come to our happy hour this evening. Information is through the QR code on the right. Thanks very much.
