---
title: "BP 2025: Kompass: Ensuring SPL-Token Stays Safe on Pinocchio Runtime Verification (Daniel Cumming)"
source: "https://www.youtube.com/watch?v=DvJdmVLCYpA"
date: "2025-12-12"
transcribed: "2026-04-27"
model: "whisper.cpp large-v3"
language: "en"
words: 1508
duration_seconds: 608
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 067
---

# BP 2025: Kompass: Ensuring SPL-Token Stays Safe on Pinocchio Runtime Verification (Daniel Cumming)

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-12
**Duration:** 10 min
**Transcription:** 1508 words
**Model:** whisper.cpp large-v3
**Playlist position:** 067/199

---

## Transcription

 Hello everyone, my name is Daniel Cumming and I'm here from Runtime Verification to talk to you about Compass, which we're using to prove the equivalence of the Solana token program with Pinocchio as the backend. I've got a lot to get through, so I'm going to probably talk fast, so buckle up everyone. The Solana token program is the topic of our talk. You might know that at the moment this is using SPL token as its backend, but shortly it will be upgraded to
 using P token. The difference between the two is that the SPL token is using the Solana SDK, whereas the P token is using the Pinocchio library. The benefits of which is that Pinocchio is more efficient and so P token is going to be more efficient. But while we want the change to be an increase in efficiency, we do not want there to be a change in behavior. We still want to have the Solana token program that we have come to know and love. So we are in a reality where there's
 two programs which are essentially trying to do the same thing, but they are slightly different. We do want there to be a difference in efficiency. So the intersection of which is the idea of what ought to be the Solana token program. So we can be explicit and talk about what this is in particular. And what we want to be the same is all of the logic of the program should be as we expect, the minting, the transferring, the burning, the effects of which should be the same if we do the upgrade to P token.
 We want to know that the errors are happening under the same conditions that we get the same error code. We don't want there to be any new behaviors or any new restrictions when we perform the update. And so that leaves what we want to be different is simply that it's more efficient. That's what we want, lower CUs. How are we going to check this? Well, in determining equivalence between two programs, we have a few different options. In increasing order of confidence, the first thing that we might do is a manual review.
 We run both programs and try and determine that they are in fact doing the same thing. This was performed by Neodym and Zelic. They did a fantastic job. Kudos to them. And we would still want more confidence that the programs are going to behave the same way. So we might do differential testing. This is where we have a test suite. We run both programs through the same test suite and we check, do we get the same results for those inputs? The fuzzing for this was done by Neodym as part of the test suite.
 And we also are running the integration and MOLUS test suites as we write our specifications. We're writing specifications because the next highest confidence, I guess, that we can get is formal verification that the two programs are equivalent. So using the power of mathematics, we can prove that they're going to do the same thing. This is the approach that we're taking. And I'll describe to you what one of these proofs is.
 Code correction. I have a diagram here to explain what that is. In the middle, we have the proof engine. This is what Compass would do in this case. And it can output some, we can be proved correct or it can be proved incorrect. It needs some input, which is on the left-hand side. And there I have color-coded yellow is the implementation. This is the code that Anza wrote, which is what we would actually have executing when we perform a transaction.
 And the specification is split into a precondition and a postcondition. The precondition is what is the generalized valid initial state that must hold in order for us to call the implementation. And the postcondition is the guarantee of what must hold if we do call that implementation and we satisfy the precondition. So this is where we know what the effects ought to be of the program. And we check that that did in fact, or that will in fact happen for all inputs.
 So bringing this to P token, what we have for the implementation in the yellow there is the P token program. This is written in Rust by Anza. And then the specification, the precondition and the postcondition, this is written by runtime verification. This is where we assume the valid initial state and we assert the valid final state. All of this gets bundled up and put into the Compass prover, which is the step in the middle of the proof engine. This is written in our case.
 This is a framework. And from there, we can prove that the implementation is satisfying the specification, in which case we're happy. We can go party. If it fails, we might cry. We'll find out. But we're going to do the partying. It's going to work. That's not enough, though. We also need to do this for SPL token. So we need to do the same proof again. Now the implementation, the yellow box there has changed to have SPL token program.
 And we use the same specification. So by proving both, we end up in this, well, yeah, the same specification is going to prove both implementations. So we do two proofs and then we use the cross product of the proofs, which could be formatted slightly better, I think. But anyway, you get the idea. We want both proofs to pass. And what that is communicating is that both SPL token and P token are,
 in that intersection that we spoke about, where they are, we have proved that they are correct implementations for what the Solana program ought to do. And by nature of them both being correct implementations, we can assert that they are equivalent modulo that specification. So that's our definition of correctness. To give you some idea of what this looks like in particular, on the left-hand side, this is a proof harness that we would prove an instruction's behavior
 correct with. So using the same color coding, the blue box up the top, that is the precondition. This is where we're assuming the valid initial state. And the yellow box, this is the instruction that Anza wrote that is actually going to process MINT2. So this is for the example MINT2. And then afterwards, we need to assert, did we error under the conditions that we expected? Did we get the correct error code? And also, if we didn't error and we're in the success case,
 did we error under the conditions that we expected? Did we error under the conditions that we expected? Did we error under
 the conditions that we expected? Did we error under the conditions that we expected? Did we error under
 the conditions that we expected? Did we error under the conditions that we expected?
 Did we error under the conditions that we expected? Did we error under the conditions that we expected? Did we error under the conditions that we expected?
 Did we error under the conditions that we expected? Did we error under the conditions that we expected?
 Did we error under the conditions that we expected? Did we error under the conditions that we expected? Did we error under the conditions that we expected? Did we error under the conditions that we expected? Did we error under the conditions that we expected? Did we error under the conditions that we expected? Did we error under the conditions that we expected? Did we error under the conditions that we expected? Or are we getting the state update that we expect? All of that needs to be done for each instruction. And also, sometimes the instructions behave differently under different conditions. And so it's a repeated process that needs to be done across 27 instruction proofs and 20 multi-sig proofs. But then we multiply that by two because we got P token and SPL token. So there ends up being quite a lot of proofs that need to be done.
 And in order to do them, we need to write out a sound semantics of Rust so that the compass prover is able to do these proofs. So this was a lot of work. And originally for the first card, these proofs were running on the order of over five hours each. So this is not a great feedback time to get for anything in engineering. We've reduced that down to about 10 to 20 minutes a run for most of these proofs. And we expect that we're going to get them more efficient shortly. That's everything that I have for you today.
 I hope you enjoyed this video and I hope you'll give you a flavor of what these proofs are doing. Thank you very much for your time.
