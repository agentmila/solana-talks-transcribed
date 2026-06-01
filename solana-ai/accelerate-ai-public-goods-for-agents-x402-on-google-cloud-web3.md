---
title: "Accelerate AI: Public Goods for Agents - x402 on Google Cloud Web3"
source: "https://www.youtube.com/watch?v=80_1d_2i2mY"
date: "2026-05-14"
transcribed: "2026-05-30"
model: "whisper.cpp large-v3"
language: "en"
words: 1361
duration_seconds: 527
tags: [transcript, solana-ai, solana]
series: "SolanaAI"
series_index: 005
---

# Accelerate AI: Public Goods for Agents - x402 on Google Cloud Web3

**Event:** [SolanaAI](https://www.youtube.com/playlist?list=PLilwLeBwGuK7DT9ofWtiSe9qbXieLgX-T)  
**Date:** 2026-05-14  
**Duration:** 8 min  
**Transcription:** 1361 words  
**Model:** whisper.cpp large-v3  
**Playlist position:** 005/18

---

## Transcription

 GM. Hey, everybody. Bear with me one second. Okay, so hey, thanks for coming to the session here. My name is Devin Mitchum. I'm part of a Google Cloud Web 3 team. We have Nicole over here in the front. Shout out also from Google. Here to talk about Explorer 2. Who here, just show of hands, who here is running an open cloud or Hermes agent? Okay, 20%. Who here has done an Explorer 2 transaction?
 Giving your agents some stables. Okay, I see a couple hands. Cool. So what I'm going to do today is do a quick run through of, okay, what is X402? What are agents? What is agenda commerce? Got a couple slides with some photos here, some images. If you have any questions, you can hit me here on Twitter. So X402. So there's a great talk after me going deeper than X402, but at least on a Google Cloud for Web 3 side, what we're doing here is we're helping developers
 and developers, builders, protocols embrace different forms of agentic tooling, right? Could be payments, could be infrastructure, could be tooling. There's a lot of buzzwords here, but one thing maybe to first shout out, we have Bunny in the front here who we worked with to build a public data set for X402 transactions. Capture this QR code. It'll send you straight to Google Cloud. You can subscribe to this data set. It's a public good. It's available. Updates, what, Bunny? Like every 24 hours, give or take.
 But we have all X402 data here from Solana and some delay data from Bay. So we're working on that. So check this out and take a look at the agentic economy. So quick roadmap here in terms of agentic commerce. So there's a lot of buzzwords, MCP, AP2, UCP. I'm not going to get into all that, but one thing to note is that there's all these different standards in terms of commerce, in terms of agentic commerce. And today I'm just going to focus on X402 on the bottom right here in terms of
 payment authorization. But there's other approaches here in terms of how do agents speak to other agents? How do agents have provenance, identity, verifiability? How do agents maybe speak to commerce front ends? And if you find this space interesting, I recommend you look up these other protocols. But today what we're going to talk about is, hey, what happens when you give your agent agency and you tell your agent, hey, go source some information or go source some data when it comes to these
 agents? They don't browse websites. They don't look at JPEGs. They talk to an API socket. When they talk to this API socket, they have agency and they can make requests and intents. And that's what we're going to demo today is how an agent actually sees the web and negotiates and purchases services through an API. Last photo here. But again, what I'm going to demo today is just the X402 side. But you can think of this agentic stack in terms of,
 again, all these composable Lego blocks. So just like Web3, how you have composability. And when it comes to the world of the agent stack, and again, there's many different protocols here, but you can think of these collectively as part of the same design pattern. The demo today, what I'm going to highlight is an agent buying services from an API. But one thing to highlight is that there's many different economic actors when it comes to X402. You have the merchant. This is an e-commerce storefront.
 It could be a shoe store. It could be a coffee store. It could be an API service provider. But merchants have websites where they sell to agents. But you can't expect merchants to pay gas. Who here enjoys paying gas on a blockchain? Nobody. Okay, a few of you. Oh, who here likes to deal with optimizing gas or routes or working with solvers? That's complicated. So merchants, they have better things to do. They don't want to run on chain. So you have third parties called facilitators that run services to help these merchants.
 Accept transactions and settle those transactions on chain. And what we're going to demo here today is we have a merchant website running on Google Cloud. We have a facilitator running on Google Cloud. And we can have our agent speak to the merchant, buy some goods, go through a facilitator. Facilitator throws it onto the chain. Okay, so this is the general pattern here. Let me jump to the demo.
 And what we're going to demo here, again, this is, at least for those who use Google Cloud, we have a serverless program called Cloud Run. You just give us your container. We'll run your container. We can run it in Singapore, run it in Tokyo. We can run it in Sao Paulo. You give us a container. We'll run it for you. Pretty simple stuff. And in this demo, we have a website. It's an expo to e-commerce store. And hey, to us humans, standard store here. You can go to the store. You can buy a selfie.
 You can get some data. Standard e-commerce public goods here, right? But when an agent visits the store, again, they speak to the socket. So what we're going to do is we're going to spin up an agent on our laptop that has a public key and a Solana wallet. And we will purchase these public goods from this store. So let me...
 Okay, I realize the text might be kind of small here. But to show generally what does an expo to request look like, when your agent talks to a website, there's this 402 transaction that happens. And generally the way it works is your agent will talk to the socket, talk to the API, say, hey, I want to buy something. Your agent will send a request to the merchant. And let me try and make this a little easier to read. My laptop cooperate.
 Yes. So your agent will talk to a merchant, send in the request. The merchant will get back to you. It'll take a half sign transaction. And then the merchant will send that transaction to facilitator. Facilitator confirms that your agent actually has money to make sure that you, the merchant, don't get ripped off. And the facilitator will then write that transaction to the chain. And then the facilitator confirms the payment was made.
 And that's really good. Okay. So that's generally the beauty of expo too. But what's most important might not be the plumbing here, but the sense that merchants don't need to trust the facilitator. Facilitators don't need to trust the merchant. And everything's accountable and attributable. Okay. So quick demo. Conscious of time. Okay. So we'll do a demo here.
 We'll have my agent hit up the API, hit up the endpoint. Okay. Don't look. That's my private key. We're going to have our agent buy a selfie. So for a micro cent, we can paste in a selfie. I paste in my private key. And this will go out. Talk to the merchant that's running on Cloud Run.
 And then we'll take a photo of our wallet and take a selfie of our wallet. And here we go. A selfie was made, generated. And if we look it up here, the demo gods cooperate.
 Okay. Here we go. So Nano Banana just made a real-time selfie of our agent. It took our public key, made some more work. It took the slot, the date, had some fun with it. We're in Miami. Why not? There's a lot of little Easter eggs in here. This is kind of the beauty of agenda commerce is that, again, you can think big here in terms of agents and on-chain information and being able to
 capture that and purchase that. If you have any questions, let me know. I'll be lurking around here in the back. And looking forward to seeing what you build. Thanks.
