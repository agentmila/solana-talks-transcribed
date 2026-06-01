---
title: "Breakpoint 2025: Tech Talk: Reilabs (Marcin Kostrzewa)"
source: "https://www.youtube.com/watch?v=xreOFvSCgew"
date: "2025-12-12"
transcribed: "2026-04-28"
model: "whisper.cpp large-v3"
language: "en"
words: 1192
duration_seconds: 448
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 119
---

# Breakpoint 2025: Tech Talk: Reilabs (Marcin Kostrzewa)

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-12
**Duration:** 7 min
**Transcription:** 1192 words
**Model:** whisper.cpp large-v3
**Playlist position:** 119/199

---

## Transcription

 Hey everyone, thanks for coming. This talk is to unveil Sunspot, which is a toolchain that lets you run ZK on Solana without pain, or at least with the minimal amount of pain possible with the current state of ZK tooling. So first of all, let's talk about why should you care? Why is it even important to be talking about zero leverage cryptography? How can it help you in your own applications, in your projects?
 So we have a bunch of different things that ZK enables that are very difficult to achieve otherwise. First of all, private transactions. Obviously, we have things like mixers, which are really controversial. Maybe don't do them. But at the same time, we are talking about onboarding institutions on-chain, for example. And the institutions are not going to be super happy about everyone, every chain analysis company being able to see what they're doing, what they're buying, what they're selling, and so on and so forth.
 Moreover, this is not purely about financial transactions. If you are building an on-chain game, you probably have the concept of some sort of fog of war, right? There is a part of the map, a part of the game state that should only be accessible to the player, but you still have to ensure that the player is performing moves according to the rules of your game, even though you cannot show what specifically they are doing. This is also something that's enabled and really only possible with zero leverage cryptography nowadays.
 Second, we have identity use cases. So many times you will want to KYC your client or like soft KYC them, at least make sure they're not a sanctioned person. But you may not want to get their entire identity card or they may not want to give it to you. So we have solutions like ZK Passport, for example, that let you scan your passport and generate a zero knowledge proof that says, I'm not a sanctioned person. And for example, I'm 18 years old and not really anything else.
 So this is something that is enabled with zero knowledge. Web2 integrations. We have protocols like ZK Email or ZK TLS, TLS Notary, that let you certify that some Web2 data on some server in some HTTP session was given to you without revealing the exact contents of the data. So an example flow would be you log into PayPal and you show that you have performed some transaction. You've sent some money on PayPal.
 You generate a ZK TLS proof that it's been done, but you are not leaking any more information. You're not leaking the fact that this is your username, this is your password and so on and so forth. And finally, scaling. We have lots of challenges on Solana with rent costs. You've probably heard of things like ZK compression from Lite Protocol. This is also enabled by the use of zero knowledge cryptography. So I hope this convinces you that this is actually something you should care about.
 How to actually implement something in zero knowledge. In particular, Sunspot uses Noir, which is a programming language for describing your zero knowledge cryptography logic. It's very new and very exciting. It's gaining popularity. There are many popular libraries, popular projects that are currently switching to it or being built from scratch on Noir. It's developed by Aztec and it has a Rust-like syntax.
 It's easy to pick up, very easy to learn. Probably the best in-class developer experience that you can get in zero knowledge cryptography nowadays. And yeah, there's a rich ecosystem of libraries and building blocks that you can pull in and you can use in your own projects. So it's actually becoming an ecosystem that enables you to do all of this. Some examples are ZK email that I mentioned before. So that's a protocol that lets you verify that you have received
 or sent an email with some particular contents in it and generate the proof that you can then verify on chain saying, yes, I've actually received this email. Again, this could be a transfer confirmation. This could be an Uber ride, whatever. And ZK Passport, which is the go-to solution if you want to talk about user identity without revealing the identity. So now, what's the biggest challenge that we're facing with doing this on Solana? And the challenge is that the
 Bartonburg proof system, which underlies Noir, has really big and really expensive to verify proofs. They are not big in terms of normal ZK tooling, but for verification on Solana in particular, they are way too big to be usable. Someone actually built a verifier on chain and just the rent cost was 30 bucks to verify a single proof. So we've decided that this is not really the way forward.
 And we have to make it better. We have to solve this challenge. And the way we've solved it is with Sunspot, which is a tool chain that lets you prove circuits that were written in Noir, but they get verified in a different proof system. The proof system is called Gnark. It's based on Grov16, but I call it Grov16++ because it actually gives you more power. It's a better proof system than what you would normally do with Grov16.
 And it has the best support for what's called lookup arguments, which in turn are pretty much indispensable if you want to be talking about bitwise operations, memory checking, or other traditional cryptography primitives. And then from Sunspot, you can auto-generate a Solana verifier program. So you push it to chain, users generate their proofs, they verify them on chain. You can actually use this logic. So let's talk about benchmarks. Let's talk about how good
 this actually is. So our demo application is an SPL token that you can mint, provided that you have a, that you possess a passport that is not sanctioned. So this uses ZK Passport under the hood. You tap your NFC chip on the passport. It generates a proof that, yes, I am not from a sanctioned country. Then you can mint a token. It takes five seconds to prove this on a MacBook Pro, which is really good.
 Compared to the traditional process that you would go through, which is really way more annoying. The proof size is 388 bytes, which for Solana, with your like one kilobyte limit of transaction size, this is really good, right? Like this still gives you 600 kilobytes of data that you can use for actual business logic. And it costs less than 500K compute units. And this may seem like a lot compared to like your normal everyday use cases.
 But keep in mind that like it's 500K compute units to verify an entire passport and actually do something that you would normally offload to a KYC provider. So yeah, this is it. And this is my call to action. Please scan this or type this on your phone and build something today. And I mean today. I know it's a conference, but build something today. Thank you.
