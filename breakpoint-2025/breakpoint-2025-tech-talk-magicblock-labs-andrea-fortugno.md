---
title: "Breakpoint 2025: Tech Talk: MagicBlock Labs (Andrea Fortugno)"
source: "https://www.youtube.com/watch?v=PgdP0uql6U0"
date: "2025-12-12"
transcribed: "2026-04-28"
model: "whisper.cpp large-v3"
language: "en"
words: 1446
duration_seconds: 606
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 123
---

# Breakpoint 2025: Tech Talk: MagicBlock Labs (Andrea Fortugno)

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-12
**Duration:** 10 min
**Transcription:** 1446 words
**Model:** whisper.cpp large-v3
**Playlist position:** 123/199

---

## Transcription

 Hello, everyone. My name is Andrea. I'm the CEO and co-founder of Magiblock. We're a team of 16 people. Our background spans from AI research to low-level system engineering. And we're on this mission to bring real-time Elastic Compute to Solana for what we think is going to be the next generation of fully on-chain applications. We want to enable every application to run entirely on Solana. A few weeks ago,
 we announced MagicNet, which was our canary network. It was supposed to be an experimentation network, but actually we realized that developers are already building production-grade use cases that are producing real revenue on Solana mainnet today. We process more than a billion transactions with 250,000 ephemeral obsessions across 11,000 unique active addresses.
 We have the cool use cases that are being built on Solana with Magiblock today. Banana Zone has actually been mentioned by Raj as one of the most interesting consumer apps out there and is obviously skewed more towards a DGN crowd, whereas Rush Trade or BlockSoap are trying to replicate a robino-like interface that simplifies the way that consumers interact with prediction markets or financial primitives. We have games that are going after real-money platforms
 that are not processing withdrawal or they're not processing them in a timely way, and therefore users have to literally sue these platforms to get their money back. The reason why an app is better off if it's built fully on-chain is because whenever the application logic is just really a set of smart contracts, you have properties that you wouldn't have otherwise if you're building with a traditional server. Your app is verifiable. You know exactly what's going on with the application logic.
 You know exactly what's going on with the application logic. Your application is unstoppable. Nobody can shut it down and it's permissionless. Nobody can prevent you from interacting with that experience. And most importantly, we think that that is going to unlock a whole bunch of revenue-generating opportunities for developers that are not possible in Web 2.0. You can take a fee off of the volume. You can take a spread off of a yield that is generating by lending the money that are in these platforms on Camino or things of that nature.
 And you might not be familiar with how MagicBlock works. We pioneered a technology that we called ephemeral roll-ups. We enabled Solana developers to add an instruction into their existing programs on-chain to delegate arbitrary accounts into blazing fast SVM instances on demand. When you run this delegation instruction, a router pings all the available nodes across the globe, clone this data on demand,
 and allow you to run the state transition for that specific account into this particular instance at light speed. You can always interact with Solana by committing the state diff or committing the state diff and CPI-ing into another program for composability and more complex interaction with other programs. And when you're done with your job, you can just un-delegate and commit back the final state.
 So effectively, it's like having multi-threading for your Solana programs. You can think of these as different threads, and you can delegate an arbitrary number of accounts into an arbitrary number of threads that run in parallel. And when you're done, you just collapse everything back to the main thread, which is Solana itself. It's not only about latency. It's also about customizability. We think that every application should be able to run on the run times that they prefer for themselves.
 So, for example, is the plugins that we have, which runs within a trust execution environment. If you delegate an account within an SVM that runs inside an Intel TDX environment, you can get private state transition. Or you've seen before how important it is for financialized applications to get real-time Oracle price stream that doesn't have to pay transaction every time you update an account. And the same goes for VRF. If you need to build an application that has an insane throughput,
 but still wants to get probably fair randomness. These are some of the use cases that we're really excited about, and I'm going to run you through some of the plugins and some of the customers that we're working with. When it comes to trading, obviously for use cases like Flash Trade, Archer, or MaxSpeed, you can imagine how important it is to have 10 millisecond latency. They can generate a lot more volume
 which means a lot more fees. Market makers that operate on a first come first serve basis can much more comfortably quote tighter spread because they can adjust them whenever the market volatility increase. Co-location ensure the best possible latency. And I was mentioning before, these are not isolated environments. You can commit NCPI into other programs with what we call a bundle. And the bundle can either execute atomically
 or you can execute at all. And then with TE, you can get really interesting dynamics for private auctions or sealed bids. When it comes to games, of course, the experience, the onboarding experience for newcomers is a lot better if the whole experience is fee less. It feels like web two, but they still can get access to native USDC or USDT across the board. And VRF is extremely important for these guys
 and really fair games. And then lastly for dark pools and private payments, we have a fine grain programmable access control where you can specify on chain exactly who gets to read or write over the delegated state. You can geofence the IP to prevent sanctioned countries, for example, from interacting with your private application. And the whole thing is still composable with Solana because fundamentally is all SVM based.
 Our vision is to enable every single application to be built entirely on chain. And so I am incredibly excited to announce four major protocol upgrades that we're doing that we think is going to bring us much closer to this vision. First, we're announcing a lightweight first come first serve multi-threaded scheduler, which can run up to 50,000 transactions per second on commodity hardware.
 This can be run as a sidecar to an existing Solana validator, given the much lower node requirements. This is going to enable a whole bunch of cool use cases that are not possible on chain right now. But there's one other problem that everybody's complaining about, which is storage costs. And that's why we're introducing and we're excited to announce that we're bringing account compression transparently and natively within AR.
 We teamed up with Light Protocol to enable the same benefits that account compression give you with up to 200 times reduction in the storage cost of rent, while at the same time being able to decompress the accounts within the ephemeral rollup, which gives you a much better way to interact with those accounts. Third, we have a brand new cloning pipeline and transaction streaming. The cloning pipeline is the module within the validator
 that keeps it in sync with Solana and is now much faster and much more reliable. And with support for streamings, users and validators can add an extra layer of redundancy and make sure that they validate the state, that is the state transition that are happening within a specific ephemeral rollup. And fourth, we are deploying some of our TE nodes within military grade data centers. Underground facilities,
 24/7 security, armed guard security, 24/7 monitoring, and a very, very strict operational security protocols. So these add a physical layer of security on top of the already secured hardware enclaves. As we progress toward our mainnets, the vision for MagicLock has always been to be a decentralized co-processing layer for those transactions that couldn't run on Solana
 today and that instead are running on AWS, on a centralized server. We can completely replace those servers. The applications can host the node themselves or they can rely on existing node operators that will have a stake and will get slashed if they misbehave, if they don't process the transaction the way they're supposed to be processing this state transition. And so with that in mind, with Solana native deployment and development workflow,
 with real-time performance, with web-to-like storage and execution costs, and with opt-in privacy, we think we are well on our way to enable every single application to be built entirely on Solana. Thank you for listening. And remember that we're building in the open. Everything that we do is open source. So we'd love you to check out our Discord, our GitHub, and keep in touch with us on X.
 Thank you.
