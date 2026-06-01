---
title: "Accelerate AI: Identity in the Age of AI"
source: "https://www.youtube.com/watch?v=96ikTkIyTtA"
date: "2026-05-14"
transcribed: "2026-05-30"
model: "whisper.cpp large-v3"
language: "en"
words: 1249
duration_seconds: 510
tags: [transcript, solana-ai, solana]
series: "SolanaAI"
series_index: 006
---

# Accelerate AI: Identity in the Age of AI

**Event:** [SolanaAI](https://www.youtube.com/playlist?list=PLilwLeBwGuK7DT9ofWtiSe9qbXieLgX-T)  
**Date:** 2026-05-14  
**Duration:** 8 min  
**Transcription:** 1249 words  
**Model:** whisper.cpp large-v3  
**Playlist position:** 006/18

---

## Transcription

 We're going to get started with Zach Meltzer, who's the founder and CEO of Vari.ai, who's going to be talking to us about identity in the age of AI. All right. Hey, everyone. I'm Zach, the founder of Vari.ai. Really excited to be here. This is actually the first Solano-specific conference that I'm speaking at.
 And even more excited to be able to do that in my hometown, Miami. For those of you that don't know, Vari.ai is a human verification platform where we focus on proving uniqueness of both humans and agents. Unlike other companies, we specialize in palm print biometrics, operated fully from your smartphone camera with no extra hardware required. A little bit over a year ago, we set out to build a biometric proof that is not only highly accurate,
 but also scalable and accessible to the entire globe. We were able to build that solution, but now humans aren't the only thing on the internet anymore. We now have agents transacting on our behalf, and the internet that we know today was simply not built with them in mind. This means that the problem is no longer just verifying humans, but also identifying agents and approving the transactions that they want to make. Before we get into the agents piece, you might be wondering,
 why we chose the palm? The palm is the only biometric modality that scores highly across accuracy, security, scalability, and privacy simultaneously. Your face is widely available online, which makes it susceptible to deep fakes. Even platforms like Facebook, that you probably think of as a social media platform, have one of the largest facial databases in the world. Both your fingerprint and your iris require specialized hardware
 to perform a scan, making that nearly impossible to scale across the world. Oppositely, palms are private. It's very rare that you post your palm online. They're highly unique, and we're able to perform an extremely accurate verification from a camera that's already in your hand, or probably on any smartphone as we speak. Our solution is 10 times more accurate than Face ID. On a single scan of your palm, we reach a false acceptance rate,
 of 1 in 10 million. And with dual palm verification and multi-scan verification, we can increase our FAR to 1 in 100 trillion, which far surpasses the minimum requirement to give every human on Earth a unique ID. I have a question. Does that factor in age at all? When does your palm stop changing? So in infancy, your palm is actually taking shape in the womb. And about ages 13 to 15, your palm will stop to change.
 And we're able to request a new verification on an annual basis or a monthly basis to make sure that we're growing with that user. Barry is not only a replacement to biometric solutions like Face ID or Touch ID, but because we have no hardware dependency, we can come in and replace legacy authentication solutions like CAPTCHA, OTP, and multi-factor authentication. Even though we've found a way to verify uniqueness
 of the comfort of your home or your pocket, the way that we verify actions online has clearly started to change. The entire internet today is built around one assumption, which is that there is a person on the other side of this. That assumption is becoming incorrect. Agents are already booking flights. They're trading. They're posting things. They're buying things on people's behalf. And things like CAPTCHA, OAuth, and rate limiting no longer work for us.
 Nobody can tell if there's a human behind any of it. And the way that most agents work today is that they're forced to imitate a person by controlling your browser, by reading your screen, or clicking through different interfaces. It's really slow. It's not convenient for the user. It breaks a lot of the time. And platforms still block these transactions. So good agents end up being treated as malicious bots. I think a lot of you may have seen the viral post the other week where someone tried to book a dinner reservation
 at the resi using their agent. And not only was the transaction itself not approved, but that user's entire resi account was blocked because it was viewed as a malicious action. We don't have the infrastructure to make this convenient and safe for the third party. You can't fix that, any of that, without a real identity layer underneath it. And we're the only ones who have built that. That's why today, right now, we're introducing AG9, the only KYA primitive that is tied to a real human.
 AG9 is a portable attestation issued by VeriAI that biomechanically links agents to their human owners from different companies and different systems across the internet. When an agent shows up to a website or a simple API, they get a token that says, yes, I'm owned by this real person. And yes, they specifically approve this action that I'm about to perform. The website can verify this activity in milliseconds and decide whether to let this agent pass through or not.
 What makes AG9 easy is that we're not asking anyone to adopt a new standard. We slot into the standards that already exist today. Cloudflare's starting BotPap, BotPap, Enterprise OAuth, the on-chain AgRentistry, and all of that. That's the same payload, we just wrap it differently for each one. If you were to use AG9 yourself, there's just three simple steps. If a third party adds the check to their website, you open the VeriAI app,
 you POM scan to link your agent, and then you can see exactly what it's authorized to do. For example, you could tell your agent to trade off to $500 on Coinbase. And after that, anytime your agent performs a sensitive action, you'll get a push notification to your POM. You see what's about to happen, you POM scan to accrue, or one tap to revoke, and the whole thing will take a few seconds. Because we're designed to fit directly into the infrastructure that Compi has already used today,
 you can run it on top of standards like Cloudflare, Auth0, or OWS. And what you see here is the flow that nobody else can deliver. It proves that yes, this AI is tied to a unique real human. Yes, that person requested this action. It was approved in real time. And it's all-
 It was approved in real time. Yes, that person requested this action. It was approved in real time. Yes, that person requested this action. It was approved in real time. And it's all-
 It was approved in real time. And it's all- They either require specialized hardware on your phone or on your computer or external devices, they interrupt automation flows, or they force a user to repeatedly expose sensitive information. Unlike your face, your POM is not as sensitive, and you're able to approve agentic transactions without revealing who you are. AG9 changes all of that. It gives agents a portable, privacy-preserving, accountability layer that works across companies, systems,
 and workflows while all remaining tied to the original owner. That's what makes AG9 the ultimate KYA solution. If any of you are building in the agent space and you think this might be helpful to you, you can visit ag9.ai or email us at hello@berry.org or zach@berry.org. Reach out to me directly, and we're happy to help you get started. Thank you.
 you
