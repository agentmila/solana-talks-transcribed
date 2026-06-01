---
title: "Breakpoint 2025: Security Block: Almanax (Francesco Piccoli)"
source: "https://www.youtube.com/watch?v=DOyXoeEc9fs"
date: "2025-12-12"
transcribed: "2026-04-28"
model: "whisper.cpp large-v3"
language: "en"
words: 1391
duration_seconds: 572
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 116
---

# Breakpoint 2025: Security Block: Almanax (Francesco Piccoli)

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-12
**Duration:** 9 min
**Transcription:** 1391 words
**Model:** whisper.cpp large-v3
**Playlist position:** 116/199

---

## Transcription

 Hi, everyone. I'm Francesco, co-founder and CEO of Almanacs. At Almanacs, we're building an AI security engineer that can help teams building on Solana ship code without bugs and catch any bugs before bad actors do. We're soon going to have trillions of dollars moving on chain, from life savings, real-world assets, and institutional
 solutions building products on Solana. Blockchains are becoming critical infrastructure. Solana is becoming critical infrastructure. And projects on Solana and protocols on Solana are critical infrastructure. And so we need the best defensive tools we can build to prevent bad actors from exploiting this critical infrastructure. So we're soon going to have superhuman capabilities in many different fields.
 And at Almanacs, we're building superhuman capabilities for security. We are a team of AI and security researchers based in New York. My previous company, I investigated some of the largest hacks and exploits that ever happened in crypto. And I grew frustrated because a lot of teams were not taking securities seriously, or they were shipping bugs that company that were well-known and companies that
 were well-known and folks before me can help catch. Unfortunately, audits are very expensive as well. And so having a tool that runs continuously during your PR process is something that we thought was needed. And ideally, having an auditor available 24/7, available via API. My co-founder was at Coinbase, and we built a team of folks coming from all across the industry. There's a few trends that have been worrying me quite a bit recently.
 One of these, we entered this age of vibe coding where literally teams are shipping millions of lines of code a day. We have companies like Coinbase and Google that are generating 40, 50% of their code, accepted code via AI. Cursor alone, this was a statistic from April. Their users are actually pushing a billion lines of accepted code a day.
 Those numbers are only going to grow from here. And so this, unfortunately, produces massive bottlenecks, right? Because if we're moving towards a stage where teams are shipping entire vibe-coded apps, and I was just talking to the co-founder of another security company backstage, and they're seeing programs and smart contracts also being vibe-coded, who is checking that there's no bugs
 or there's no malicious code that is being injected, or simply buggy code that is making it into production. Today, security and engineering teams are literally swamped with alerts from static analysis tools. Fortunately, they often do audits. They run bug bounties. They have other tools. But the massive amount of alerts that they get makes it very hard for them
 to go and then triage and then pass it to the engineering team to go and actually patch these issues. And so often, especially large organizations, we see that what actually gets patched is not the entirety of what gets caught, right? Because there's a lot of noise. And so you guys, how many of you guys have seen the recent Anthropic report that were released around security? Quite a few, right? And it's funny,
 because they released two recently. The first one that they released talks about cyber espionage, and it's large-scale cyber attacks that they took down from Chinese state-sponsored hacker, where these bad actors were using AI in their exploit. And then a week or two weeks after, they released another report where they used AI to exploit smart contracts deployed on-chain. And it's getting kind of scary, right?
 Models are getting to abilities of very thoughtful and very senior security engineers. We're not there yet, right? At this moment, we're probably at the level of junior security engineer, but if the trend continues, we're soon going to be at superhuman ability when it comes to security as well. And there's some hints around the Balancer hack, 120 million lost recently, where the attackers might have used AI in their
 exploits. And so that's kind of like the main reason why we started Almanacs. We wanted to build like the best AI tools from a defensive perspective to teams that are building on-chain. And so Almanacs is an AI security engineer that scales with your code base, continuously reviews code, investigates and triages alerts, and help actually patch alerts and security issues at scale. I was supposed to do a demo,
 but like I'll do a few slides so I have the clicker. We built a system that kind of like reasons through a code base, no matter its complexity, like a security engineer would, right? And so in order to do that, there's multiple things that you need to do because like code bases are very large, context windows are small. And so you need to give these agents the ability to navigate the code base, right? And so when we start a scan and when our customers start a scan,
 they're running on their full repo or they're running in their CI/CD pipelines or PR review process, we create like a threat model of the repo. We look at invariants. We create an abstract syntax tree. We create like a function call graph so that the agents are able to navigate to different parts of the code base and understand like the logic of certain functions like a security engineer would. And so this runs 24/7 in the PR review process.
 But it can also like be used as a tool that runs like before an audit, for example. So we work up with a lot of teams that are about to go and do an audit. We work with auditors as well. They're using these tools during like their review process. And then we also investigate existing like alerts and help like teams triage. If you're a large organization, you're probably running different security tools. And generally,
 what we're seeing historically is that 90% of the alerts that teams get are false positives. And so you're drawn, like these teams are drowning in noise from like these alerts. And often they might like dismiss something that isn't really a false positive. And so what we develop is this system that kind of like does, with the context of the code base, does an automatic pass of triaging to help prioritize what to fix.
 And then the very last step is actually going and patching. And so if you have like hundreds of alerts or hundreds of vulnerabilities that are found, well, I hope it's not a program that you're about to launch on chain because that would be very worrying. But if it's like a large, like monorepo or a large code base, you want to be able to like patch at scale. And so back in the days, you would like pass, the security team would pass all these alerts to the engineers.
 And then the very last step is to build an agent that is directly in line if an issue is like an easy one, or we create a draft PR. So we're working with like security teams today from like various protocols and like wallet infrastructure team, working with Previ, and we're working with a bunch of Solana programs, Solana protocols as well. And today, I want to announce our collaboration with the Solana Foundation. We worked very hard to build an agent that is good,
 at understanding Solana protocols. It's good at understanding Solana programs. It has context on like anchor. It has context on anything that matters when like building something on Solana. And as part of the collaboration we're providing and Solana Foundation is helping us like provide like one year of like free audits for projects that are building on Solana. And so this is the moment where you guys clap. I was like, this is cool. This is amazing.
 And with this one, I'll pause. You can get in touch. You can sign up. And if you want to see this directly on your code base, you don't even need to talk to me. This is all my information, but you can go at app.almanacs.ai and you can run like an AI audit. And then we'll send you to some of the fantastic auditors that I see here in the space and in the audience, like runtime verification. Thank you guys. I'm Francesco. Talk to you later.
 you
