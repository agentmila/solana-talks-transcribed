---
title: "Accelerate AI: How we built Eternal Agents & Institutional x402"
source: "https://www.youtube.com/watch?v=_buvMvf2JXg"
date: "2026-05-14"
transcribed: "2026-05-30"
model: "whisper.cpp large-v3"
language: "en"
words: 1371
duration_seconds: 501
tags: [transcript, solana-ai, solana]
series: "SolanaAI"
series_index: 012
---

# Accelerate AI: How we built Eternal Agents & Institutional x402

**Event:** [SolanaAI](https://www.youtube.com/playlist?list=PLilwLeBwGuK7DT9ofWtiSe9qbXieLgX-T)  
**Date:** 2026-05-14  
**Duration:** 8 min  
**Transcription:** 1371 words  
**Model:** whisper.cpp large-v3  
**Playlist position:** 012/18

---

## Transcription

 Hello, everyone. Oh, my God. So my name is Mauricio Trujillo Ramirez, also known as Bunny, also known as Conejo Capital. I wear many hats because I've been in tech for quite a few years now, such as everyone in the room, I think. It's a pleasure to be here. I've been a big fan of Solana for the past two years, been building in crypto for about six. I think we built some pretty cool infrastructure, pretty cool tooling for trading, financial, agentic commerce,
 you know, all the good buzzwords for 2026. But we are actually bringing good institutions in-house. I think, well, we're going to have fun. So as I said already, my name is Mauricio Trujillo, also known as Bunny. This all started with, as with many things you do in life, with a great idea and with a tweet. So Jacob Creech at the start of the year was like, oh, like the hardest part of getting on chain for all these,
 like cloud bots, like harnesses and whatnot is that there are no porn with gas, right? And if we extend this a little bit further, there's no porn with any semblance of how to operate on chain, right? No human on earth or no agent on earth is going to have like that preconceived awareness of how to operate on chain. Like there's just not enough good UX training data on that. And there's a couple of ways that we can go about fixing that. So our initial implementation with that was, well, what is the easiest way to let an agent get any sort of gas on chain?
 And it is by letting them have a token, have something to be able to financialize themselves, have something to be able to get some greater fees. So we realized that the one strongest ecosystem for that sort of tooling was, of course, BondFund on Solana. And we went ahead on our first day of being live, we produced this around like 10 to 15 mil transaction volume. By the second day, 25, one month in, we've done already one bot and a half in, or probably we've done like 65 mil volume.
 And it's done quite well. We think that we've empowered agents to do very fantastic things. And we've also shipped a second version of it, which I think is the much more palatable version for a lot more AI native people in the world. So we created a couple of primitives on Colobo. So first and foremost, we created this primitive called the Eternal Agent. What we mean by that in practice is that we empower agents to have DeFi tooling, get access to all of the models,
 all the data that they want, have water, of course, like all the good things that an agent will need to be able to operate on chain indecisive without a human, a human would. And we actually let them use those DeFi profits to pay for their own compute. So we built a next for two gateway to allow them to route to their provider of whatever LLMs they're using. This is not something that was very standard, like at the start of the year, where one of the first few teams to do this, not only within crypto, but also just in traditional like fintech,
 DeFi and AI in general. So we're pretty proud of that. So we grew from this like token launchpad and winning the pump on Hackathon and whatnot, getting some investments and whatnot, which will be hopefully public in a little bit more in a little soon. But we started building all of these subscription toolings, all of these skills. We have 80 plus skills. That's right. We have like 50 plus skills. We have 80 plus API endpoints. We let you now also sell your agents.
 So this is something that I guess for people that have been in ecosystem for a minute, like something like OpenSea or maybe just an agent,
 you can sell the agent marketplace. This was the initial listing. The person, of course, earned much more money than I ever made with that agent. So props to them. So Colossal Club on work. We've done a lot of backend work to just give you access to all of the good skills that you will need, give you, let you integrate effectively agentic DeFi harness. You can buy, sell, trade in the exact same way that you would do with a regular wallet. But I think that this is honestly,
 like the most useless use case for an agent. I think where it gets really interesting is when you actually start giving them access to not only their wallet, platform credits for LLNs, but also stuff like being able to keep in a virtual environment to start automating stuff like DCA, buying divs, taking profits, morning portfolio check, whale alert in case like there's a wallet or like some LPs that you want to keep track of, being able to create loops for this,
 being able to list themselves for auctions, being able to, maybe you don't want your agent to get sold off and lose complete access to it. But if your agent is really good at performing a service, maybe you can put it behind an X402 gateway and sell that service. So there's all these whole new paradigm of markets that have been very incredibly underexplored purely because, I don't know, I feel like people are not willing enough to actually push the boundaries here. And we are through Colossal Club.
 So the skills, you can also submit your old skills. Huge shout out to the Send AI skills and also other community CloudBomb skills that we've worked with. We also made it to the top of the Solana Foundation's AI page. So we're very happy with that. So going back to the interesting thing that we found within CloudBomb is that a lot of the services that we built actually were not only for retail use cases, but actually they have pretty interesting
 let's say more institutional use cases. So after we chatted with some good friend of ours at the team at Google Web3, we realized, oh, what if we build this X402 gateway for BigQuery, Gemini, Vertex and whatnot? And we can create a facilitator that is optimized or it's like Google Cloud native. So it can be one click deploy for anyone, any enterprise in the world that is already on the Google Cloud stack.
 It's very easily geographically located to them. And they're able to do payments for transactions for BigQuery and also create a... This is a quick demo of some of the queries that were done on BigQuery and also on Gemini. I'll leave this some for the team at Google Cloud to be able to present in a bit. But this is a postcard that was generated by Gemini showing the wallet of the agent that paid the signature, the...
 The cutout from the blocks, but also the micropayment received. Welcome to Miami postcard. And this one fails a little bit sometimes, but as Gemini gets better and better, we'll be able to showcase also the time of the transaction. But yeah, we're playing around. We're doing some fun stuff. And this actually resulted on what now we know as pay.sh, which we were some earthly design contributors. And we were able to be one of the first teams to bring Google Cloud
 more deeply into Solana. And we're more than happy to continue building on this vision. I think with Tectonic, we're gonna continue. I think there's something to be said about Solana in which everything is like, yes, hyper-financialized and everyone's doing a lot of very fun stuff. But I will suggest to every single founder out there to not get afraid of working with institutions. Maybe you will have to set up an extra proxy, but maybe you can unlock some interesting collaboration
 with more AI native teams. And maybe there's a couple other larger AI teams that we're collaborating with, which will become public soon. So thank you so much, everyone.
