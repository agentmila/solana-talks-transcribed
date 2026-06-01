---
title: "Breakpoint 2025: Security Block: Certora (Pamina Georgiev)"
source: "https://www.youtube.com/watch?v=j8BMKFQQPWY"
date: "2025-12-12"
transcribed: "2026-04-28"
model: "whisper.cpp large-v3"
language: "en"
words: 1286
duration_seconds: 512
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 118
---

# Breakpoint 2025: Security Block: Certora (Pamina Georgiev)

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-12
**Duration:** 8 min
**Transcription:** 1286 words
**Model:** whisper.cpp large-v3
**Playlist position:** 118/199

---

## Transcription

 Hi, everybody. My name is Pamina Georgiou. It's now Georgiou. It used to be Georgiou, so don't be confused. I'm the formal verification team lead at Satora. And Satora is a Web3 security company. And we, among other things, do formal verification. And I will use the next eight minutes and 40 seconds to try to tell you what that means. Okay, so when it comes to code security,
 most of the times DeFi protocols use all kinds of things in their security stack. They start with reviews internally and externally, of course, right? They do auditing. They do a lot of testing for sure. Ideally, they also do fast testing. So at least they cover, you know, a bunch of inputs and don't only rely on just a few unit tests. However, still to find bugs with fast testing, it's a little bit,
 you know, a game of chance. So sometimes you're lucky and you find the bugs. Sometimes you're just not. Now at Satora, what we do is we do formal verification. What that means is, sorry, that we actually try to mathematically specify the intended behavior of your code and then mathematically derive those properties from your code with the help of so-called provers.
 Okay, you might wonder, well, why do we need this in DeFi? There is real money at stake. And of course, you want to make sure that if you're handling money, that you cannot get wrecked. Otherwise, the trust is gone. And formal verification is basically the only way to guarantee any of that. Okay, I'll attempt to give you a small code example. Please bear with me. You can see here a tiny little program. It's a vault program.
 The only thing that it does, you can deposit assets and it will mint shares for you in proportion to the total value of assets locked in a vault. And you can redeem the shares with the withdraw function and you should get your fair share. Simple enough, right? Now, when it comes to computation of values of assets to your shares and shares to assets, most of the time you need to use a multiplication and division there.
 Now, when it comes to division of integers, that means there's also rounding in here. In this case, I introduce a bug. Usually, you want to make sure that when you mint assets or when you redeem the shares and you get out the assets, you want to make sure that you do not overestimate the amount of money that you pay out to your users. Because that would mean in the long run, the last person to withdraw cannot get their money back. So, in this case, I do exactly this.
 And I seal the Maldive computation rather than rounding down, which means that we overpay by approximately one token. Now, a very elegant property to show such rounding issues is to actually show that your share value cannot decrease after any user operation. So, in terms of code security, you really want to make sure that
 you have public-facing functionality in your code. You make sure that assets divided by shares, so the value of one share cannot go down. And on the right-hand side here, you can see a partial implementation of a prop test. So, I just wrote it as a test, a property-based test. And rather than using the division, I use multiplication just to make sure that in the test itself, we don't introduce any additional rounding.
 And I actually wrote a complete test harness for this example, where I just generate random sequences of deposits and withdrawals from one to 200 steps. And I let this run for 100K test cases, and I did not run into a bug. So, unfortunately, even with 100K passing cases, that does not necessarily mean that you're bug-free. And the only way to actually guarantee it is to formally verify it.
 Now, in Satora, we have a nice Satora verification language for Rust that allows you to actually write something that almost looked like a test as a formal specification. So, you can see here the same, basically the same thing as for the prop test for the withdraw function, where we're trying to assert that the share value cannot go down. Now, formal verification means we want to check all possible
 inputs to your function. And it also means we want to cover all possible reachable states of your program. In this case, our state is very small, right? It's just assets and shares. So, we need to make sure we tell the prover that we actually start in a state that is valid, so to say. And we already proved before that a valid state in this case means a solvent one. So, we assume a state where we always have at least as many assets as we have shares.
 This is proved separately. But this is how we cover every possible state that is reachable as a starting state for the formal property. Then we take the variable shares and we say it's a non-det. It's a non-deterministic value, meaning that it can have any value that a U64, an unsigned integer can have. And then we call the function that we want to verify. And then we assert our property.
 It does the same cross multiplication as we saw in the test before. And this way, we can now run the Sartorius and Lana prover. It's open source. The link here in the QR code actually leads you to our docs if you're interested. It's super easy to install. It comes with a command line tool, as you can see here on the left side. And you can run basically rules like the one you just saw. And as a result, you get a link. And that link contains the verification result.
 In our case, the verification result shows a counterexample. Now, a counterexample means we have one specific, one concrete state of values where our property is violated. So here we start in a state where we have 19 assets and 10 shares. Somebody wants to redeem six shares. And it turns out they get 12 assets rather than just 11, which would have been their fair share, thereby decreasing the share value.
 So the prover flags this immediately. This took about 30 seconds, if at all, with sending it off to the cloud and everything. And since we already know what the bug is, we simply fix it. We basically floor the Muldiv in the withdraw function. And if you want to take a look, I actually implemented a few other properties as well. You can scan the QR. It will show you the rule report as we usually do it at Sartora.
 And of course, that was a very, very small example. But we did formal verification projects for quite some big names that you might have heard about already, such as Jito, Camino, Squats, Manifest, and also some work with the Solana Foundation itself. And we also do more than just formal verification at Sartora. So Sartora is really a fully fledged Web3 security company. We do audits. We do design reviews. We do operational security. We help you with any
 security needs that you might have. And if you currently have any security needs, I just wanted to do a quick shout out for Arita's security subsidy program. They are funding up to a million dollars for Solana builders when it comes to security. And Sartora is part of that project. So if you want anything from audit to formal verification, please check it out. Thank you.
 you
