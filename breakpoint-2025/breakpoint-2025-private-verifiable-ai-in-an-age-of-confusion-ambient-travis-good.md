---
title: "Breakpoint 2025: Private Verifiable AI in an Age of Confusion: Ambient (Travis Good)"
source: "https://www.youtube.com/watch?v=GegcZPaN3xc"
date: "2025-12-13"
transcribed: "2026-04-29"
model: "whisper.cpp large-v3"
language: "en"
words: 906
duration_seconds: 397
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 183
---

# Breakpoint 2025: Private Verifiable AI in an Age of Confusion: Ambient (Travis Good)

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-13
**Duration:** 6 min
**Transcription:** 906 words
**Model:** whisper.cpp large-v3
**Playlist position:** 183/199

---

## Transcription

 Hello, Breakpoint Abu Dhabi. Great to see everyone here. I hope you're doing well. Some really great presentations, some hard to follow up. I wanted to ask all of you a simple question, which is, can you trust your AI infrastructure? You know, we're entering an agentic economy where agents are going to be in the middle
 of every transaction, and the thing powering those agents is, of course, a model. But I want to ask you, do you know that that model is running correctly? Do you know that it's hitting the benchmarks of intelligence that you would expect? Can you guarantee that every word of text or every pixel in an image that that model is producing is being rendered
 correctly? I would say those questions are of critical importance because if AI agents are our interface to the world, if they're our interface to wallets, to software, to economic opportunities, then having a suddenly stupid AI agent or an AI agent that is turned against its creators is a huge issue. You know, in crypto, we care about crypto economic security. We audit smart contracts 10 times.
 But in AI, I see a lot of people using Anthropic. Anthropic is a great company. But they also released Claude code, which was compromised in terms of its coding ability for over a month due to a problem in its inference engine. That impacted the usability of that product for everyone who used it for a long time. It had a huge economic consequence for them.
 So I would say that verifiability around AI is very important, but it's not been provided traditionally. And the reason is that it's very difficult to do. Traditionally, it's been extremely expensive. It might cost you 10 to 1,000 times more than unverified inference. Or you make compromises, like you take an optimistic approach where you just sort of assume that everything is working. And then at some point, you check and you penalize people.
 If they've made a mistake. That works really well until you have an asymmetric risk situation where someone could earn $10 million by rugging your agent and could only be slashed $10,000. So there's a big security compromise there. Also, people have tried TEEs. And, you know, the problem we have in crypto is you can't base crypto economic security on TEEs because they themselves are repeatedly compromised. So you can't make AI security
 based on TEEs either. It's good for privacy as a mitigation, but not for security. The other thing is that in crypto, we don't have high scale providers. It's really hard to put volume through the pipes because people have been focused on delivering a bazaar of models, a lot of different models that meet long tail use cases. And there's really been no focus on delivering one high intelligence model at the kind of scale that would be useful
 to apps that, for example, suddenly get popular. So that's what Ambient is. We would like to be your high scale provider of verified machine intelligence. And we want to provide you that service for exactly the same price as unverified inference. We want to give you privacy options ranging from anonymity to full end to end encryption within a TEEs without
 compromising the security of the verified inference, which, again, is providing you a guarantee that a model was run correctly. It produced every single word of a text according to a particular prompt at a particular time. And what that enables is provably fair economic games, which is, of course, what we'd like to play on Solana. We also offer some integrated capabilities that you find in, like, the opening
 eyes of the world, like search and deep research. And again, we focus on high scale delivery. So we have the capacity to serve your popular app. I'm going to just try a little demo here. Hopefully it plays. Yeah. To show you that we're not compromising on the speed or anything for verified inference. This is our chat client. This is available today. We're asking it about the speed of Solana.
 It did all the blockchain things in the background. It already verified all of this text, proving that this text was rendered by a 16-bit quantization of GLM 4.6. Every word of that text was rendered correctly by that model with a particular configuration of VLLM. So you don't have to worry about whether your infrastructure provider is giving you incorrect results or results that aren't matching the published benchmarks.
 It's guaranteed to be good. Another demo I can run in the background briefly -- it's kind of like watching paint dry, unfortunately -- is research. So we have some additional capabilities. All of these capabilities are powered by the same verified intelligence engine. So the idea is simply that you have that guaranteed level of intelligence and quality as the research process is going on. All of these links are being evaluated by that model.
 Very briefly, we've got a Solana quick start on docs.ambient.xyz. It's available right now widely. Please check us out. We are ambient.xyz on the web. I am Iridium Eagle on X. You can check out our app.ambient.xyz. Please feel free to get in touch to get some free inference. We'd love to support your applications on Solana.
 And the future of agentic commerce as a whole. Thank you very much.
