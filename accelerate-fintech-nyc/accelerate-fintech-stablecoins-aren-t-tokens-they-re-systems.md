---
title: "Accelerate Fintech: Stablecoins Aren't Tokens — They're Systems"
source: "https://www.youtube.com/watch?v=W22Mq_Wna04"
date: "2026-05-13"
transcribed: "2026-05-31"
model: "whisper.cpp large-v3"
language: "en"
words: 1555
duration_seconds: 602
tags: [transcript, accelerate-fintech-nyc, solana, fintech]
series: "Accelerate Fintech NYC"
series_index: 006
---

# Accelerate Fintech: Stablecoins Aren't Tokens — They're Systems

**Event:** [Accelerate Fintech NYC](https://www.youtube.com/playlist?list=PLilwLeBwGuK6-wBP_gzpYOc9gTRqu-2YT)  
**Date:** 2026-05-13  
**Duration:** 10 min  
**Transcription:** 1555 words  
**Model:** whisper.cpp large-v3  
**Playlist position:** 006/8

---

## Transcription

 Coming up next, we have another builder, the head of engineering at Paxos, Derek Gottfried, who's going to talk about how stablecoins aren't just an asset in a wallet, but a system in it of themselves. All right, thank you. Boy, these clickers are hard. First of all, thanks to everyone for making it out and to Solana for hosting this. By the way, I saw a video version of that demo before, and somehow,
 I was in double time. And so it felt accelerated. It was amazing, because it was a very compressed version. And congrats to them for putting that together. It's an awesome resource. I wanted to maybe take a different tact here. And I think tokens and the way that we think about tokens are kind of the underpinning here. But it's not just about tokens. And so I'm going to walk through a little bit of a story.
 I went back in December, Fortify, a great institutional NBC wallet. And I was in Tel Aviv with the team. And they said, hey, what's so hard about tokenization? Just put the contract down, and you're good to go. And it came to me that there was a lot of work that we're doing that maybe wasn't totally highlighted. And so I wanted to give a little bit of an opportunity to explain all of the engineering and all the systems. And so it's not just engineering. We love our friend Claude.
 We'll turn all our work over to him. But the reality is that there's a lot of integration. There's a lot of compliance. There's governance. There's a bunch of things. So while SPL is an amazing token and easy to deploy, you have to do a lot more than just that. And so at the basic, we need to take fiat in. And so we've done a lot of work on our fiat rails of how we're going to take dollars and convert them to tokens.
 We have a lot of work around what KYC and KYB looks like. But it is not just about taking the money in and putting it on chain. There's a bunch of things that happen in here. And the core loop really is you've got to fund. We need to do some verifications. The minting is what everybody gets excited about. It's all the hard work of signing and making sure everything is secure.
 And the ecosystem is super important. Monitoring is the thing that, no offense, if anybody's on the compliance side, nobody's excited about, but is super important to get right. And then the redeem. And so we've done this for lots of different tokens across lots of chains, across lots of years. And so we have a lot of experience. And so to think about something that is just around putting a contract
 on chain and marking it up, there's a lot more that goes into it. And so I would think the thing to think about here is, you know, once you're on chain, a lot of it is permissionless. When you're off chain, it is not permissionless. And that is the part that we navigate in between those two things. And that navigation really relies on, hey, we have a bunch of money sitting in a bank. We have lots of banking relations.
 We have lots of relationships. And we have an internal ledger that understands exactly what that state of that bank account looks. And then we have an on-chain state. So a lot of the effort we put in is to make sure all of those match up. We have regulatory requirements around that. We've always chose to be regulated. We think it's important to bring clarity. I think everybody can get regulated now. Congrats. It's awesome. Welcome to the auditors and all our friends.
 Thank you. Thank you. Thank you.
 You know, the important to think about this is that compliance is not a step. It's not this thing that you do, you check the box, and you move on. It's this living, breathing system. And so it's not just about KYC at the beginning. It's the extended due diligence. It's the travel rule. It's the monitoring. We work with great partners. But you then need to layer on your own take on it. You're going to be responsible for it. So it's not something you can just turn over to a vendor and say,
 huh, out of my hands. This is a thing that I think when we're navigating between these two worlds is super important. And we've spent more time, maybe not more time, a lot of my time. Auditors are awesome. Compliance people are super fun. But you really need to work to get it right. And it is not something that you can check the box and move on. It's something that you need to build an entire ecosystem around.
 And one of the things that we are seeing is that while policy lives both on-chain and off-chain, we've seen some really novel stuff that are happening on-chain. We expect token extensions to allow more of that. And so we are very excited about what's happening there. But we've really seen the shift from kind of this manual process to how do we automate it, particularly as we've seen volumes pick up.
 And how do we really move the policy to where the asset is? And so it's not two disconnected things. It's not the checkbox. It's the living system that is closely bound to where the asset happens. And one of the things that when we think about the challenge of wallets and addresses is, how do we bind those to identity? This is a constant challenge for us of how do we keep lots
 of the goodness of the permissionless system, but also operate in a compliant way? And what does that mapping look like? And so there's real challenges around the UX, around who owns what wallet. And we think that there is a bunch of new ideas that are coming up. And we're working on several ourselves to address this. This one, everyone, I think, talks about distribution and liquidity loop. I think my least favorite tokens are the ones that are kind
 of closed loop and essentially end up resembling kind of the gift card of stablecoins. It's single purpose. It doesn't really have kind of the liquidity. It's not dynamic. You're not going to find it on the exchanges. And so we've worked really hard to make sure that these are not single purpose vehicles, that they have distribution. And we build liquidity both on chain and the ability to enter and exit on the fiat side.
 And so why Solana? Why do I think Solana makes this? Because I'm focused on my problems, and I don't have to focus on the Solana problems, honestly. We work with lots of node providers that they mentioned before. And for me, I rarely think about Solana, like is it up or is it down? How fast is it going? It is a joy to work with in the sense that
 that part is abstracted away. And so we think that like it has an awesome ecosystem within it. We also think that like it is like the one that has accelerated more than others. And so it is a great place to go and build on top of. We're excited by the partnership. But largely, I just don't think about it, which I don't mean that in a bad way. I just don't think about it because it works, which is exactly the way you want your infrastructure to be.
 And I probably killed the slide, which is totally fine. Just to kind of wrap up here, I think as you think about what-- I don't know. It doesn't matter. The thing to think about is that like just getting the token on is a great accomplishment. There's lots of YouTube videos to go and watch, and you can do it in your spare time, and Claude will help you. But when you think about a complete system
 of how you're going to work on liquidity, how you're going to work on onboarding, what you're going to do with fiat, where does regulation live, how you're going to work with the broader ecosystem, I think that's where you need a comprehensive solution. I think Paxos has done a great job. We've talked a little bit. And the only thing that's not in my slides that I will mention is our work around what we call rewards. And I don't want to step on any kind of legal things. But how do we return--
 some of the economic opportunities to our partners, and how do we make that more automated and transparent? And so that's the thing that we've been focused on. We have a great blog post somewhere. I think it's like two posts ago, a couple of weeks ago, about our new alpha. We are bringing this to Solana. So I would encourage everybody that likes money to go check that out and understand some of the things we're building. So really appreciate your time. Wake up, people. You're a little slow. But thank you.
 Thank you.
