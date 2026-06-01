---
title: "Accelerate AI: Poncho: Browsing the Agentic Internet"
source: "https://www.youtube.com/watch?v=EnVdICEoEf0"
date: "2026-05-15"
transcribed: "2026-05-30"
model: "whisper.cpp large-v3"
language: "en"
words: 1076
duration_seconds: 459
tags: [transcript, solana-ai, solana]
series: "SolanaAI"
series_index: 007
---

# Accelerate AI: Poncho: Browsing the Agentic Internet

**Event:** [SolanaAI](https://www.youtube.com/playlist?list=PLilwLeBwGuK7DT9ofWtiSe9qbXieLgX-T)  
**Date:** 2026-05-15  
**Duration:** 7 min  
**Transcription:** 1076 words  
**Model:** whisper.cpp large-v3  
**Playlist position:** 007/18

---

## Transcription

 All right, thank you everybody for coming. I am Sam, CEO of Merit Systems. We do open agentic commerce. I'm going to kick off a demo and then I'll explain a little bit about what that does. So on two panels ago, somebody said that there's no API for weather in agentic commerce. You'd have to pay with a credit or debit card.
 You'd have to pay with Locus API for weather and tell me the five-day weather forecast in Miami. All right, cool. So that's going to take a while because it's an agent and Claude's very slow. We do open agentic commerce. Agentic commerce is agents that pay for stuff. Two-sided marketplace. There's agents on one side that want agent-native goods and services. And then there's merchants on the other side that want to sell things directly to agents. The first two things we launched in the ecosystem were X402 scan and MPP scan.
 If you've used X402, you've probably been on one of these sites. They're the main explorers for X402 and MPP resources, respectively. All right, internet's a bit slow, but shows all the resources. There's between X402 and MPP, there's about 20,000 goods and services listed on here, including a weather API, for example. So paid with stable coins, not credit and debit card. But that is sort of the search layer.
 X402 and MPP scan. And then they can be discovered through most of the clients, including pay.sh. The two clients that we run are AgentCash and Poncho, which I'll be talking about today. This over here used AgentCash. We call AgentCash our AgentPro product. It's an MCP server. So it installs into your Claude or your Codex or whatever and gives you access to all 20,000 goods and services. You can look them up and do lots of fun things. There's about 5,000 wallets on AgentCash today. About 500 of them do real volume.
 Poncho is the one that we're more excited about and haven't launched yet. So you can try it today. It's live, tryponcho.com. Fully hosted experience. You should think about it like Claude Cowork, except for Agentic Commerce. And I'm going to pick on Rish again, like I did last time. Find me Rish from the Solana Foundation, pull a high resolution headshot of him, and then do a nano banana image edit to have him walking down South Beach in his flip flops, walking his pet flamingo.
 And then put it on a mug and buy it and mail it to the Solana Foundation's New York headquarters. Nice. All right. So this is going to take a while, but this composes together about 10 different APIs. You'll notice that we don't really talk about X402 or MPP anywhere in Poncho. It just looks like JetGBT. But under the hood, we do stablecoin settlement. AgentCash lives within Poncho.
 AgentCash is available in Poncho. Cool. So first thing it does here is it goes, so this is a generic prompt. It goes and looks what tools it has access in order to pull this off. It builds out a plan and then it starts executing. It finds that it has access to Stable Studio, which is all the frontier image and video gen paid over X402 or MPP. Finds Stable Merch, which is custom merch behind X402 and MPP as well.
 And then it's going to try to compose them all together. Nice. Okay. It looks like we found the Solana Labs New York headquarters. All right. I'm going to pick up, kick off a parallel demo here.
 Can you call me at 914-819-2831 and remind me that I have a talk at the Solana Accelerate AI Conference?
 All right. So hopefully this finds the phone call tool and then tries to give me a call. Looks like it found it. Oh, there we go. Hey, how's it going? Just a reminder that you have a talk at the Solana Accelerate AI Conference. That's really helpful. Thank you so much.
 So you can imagine composing that together with a lookup on your schedule or something like that, and then calling you or reminding you that you bought a mug for Rish from the Solana Foundation. All right. Okay. This one's still going. Let me see if I can run through what it did. So normal prompt that you could put into ChatGBT here. ChatGBT only has one image generation model. This has 30 in it, or at least 30 from Stable Studio.
 It's about 150 across all of X402 and MPP. It also did a lookup to find the Solana office headquarters. I hope that's not private. It's not anymore. It found a headshot for him from LinkedIn. LinkedIn is generally not available to agents. ChatGBT, Claude, Gemini all get blocked by LinkedIn. If they use their web fetch tool against LinkedIn, LinkedIn says, stay out of my walled garden. That's my data, and they all respect it. Over X402 and MPP, there's about 150 different endpoints.
 That sell various forms of LinkedIn data. Nice. That was you yesterday, I imagine, at the hotel. All right. Cool. All right. Then the more fun part, in two weeks, he'll have this on a mug at his house.
 So that's OpenAgentic Commerce, TryPancho.com, available today. There's a generous free tier. We sponsor about $20 of your first transactions. You can access 20,000 different endpoints. The coolest part of this, though, is that unlike ChatGBT, Gemini, they're working on Agentic Commerce as well. But it's a BD process to be able to sell through ChatGBT or Gemini. You have to show up and do a partnership with them and make a deal through this. Any merchant can list overnight. So you stand up in X402,
 or MPP service, Pancho, Agent Cash can call you out of the box. We aren't a gatekeeper of that whatsoever. It's an open protocol. Same way in 2000, when the free and open internet was getting started, all you needed was a domain name and a server, and then you could list and anybody could find you. That's obviously the big bet here, is that permissionless innovation is much, much more interesting than ChatGBT, Gemini, and others controlling the floodgates. That's all I got. I have a bunch of free Pancho Pro codes as well. If you're interested in one of those, would love to give it out. Come find me afterwards.
 Thank you, guys.
