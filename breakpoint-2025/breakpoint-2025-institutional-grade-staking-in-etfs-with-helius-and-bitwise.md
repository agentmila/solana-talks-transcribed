---
title: "Breakpoint 2025: Institutional-Grade Staking in ETFs with Helius and Bitwise"
source: "https://www.youtube.com/watch?v=D-kJvIJ0uBo"
date: "2025-12-11"
transcribed: "2026-04-27"
model: "whisper.cpp large-v3"
language: "en"
words: 1780
duration_seconds: 883
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 038
---

# Breakpoint 2025: Institutional-Grade Staking in ETFs with Helius and Bitwise

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-11
**Duration:** 14 min
**Transcription:** 1780 words
**Model:** whisper.cpp large-v3
**Playlist position:** 038/199

---

## Transcription

 Hi, everyone. Thank you for joining us today. My name is Ali Nadel, and I'm an associate director of business development on the on-chain solutions team at Bitwise Asset Management. And with me today, we have Hong Kim, CTO and co-founder of Bitwise Asset Management, along with Mert Mumtaz, who is the CEO and co-founder of Helios. Thanks for joining us, Hong and Mert. So this audience is likely quite interested
 in learning about how staking has entered into ETFs. So let's start by diving right in and learning about the partnership between Bitwise and Helios on staking for the product that we launched back in October called BSOL, which is the Bitwise Solana staking ETF listed on the New York Stock Exchange, trading under the ticker BSOL. So Hong, if we could start with you and learn a little bit about how you and Mert put your heads together to form the staking partnership, that would be wonderful.
 Amazing. Yeah. Great to be here. And yeah, when the U.S. ETF launch moment is a pretty important moment because U.S. is ultimately the largest capital market in the traditional financial world. And also the spot ETF ends up becoming the most liquid product as we've seen from iBit and ETH, et cetera, where it has a pretty important role that it plays.
 And once it grows and gains liquidity, then it becomes this huge thing. And so we wanted to be thoughtful about how we engage with staking. And staking isn't just a little bit different from custody. It isn't just something that sits statically. It engages with the network in a meaningful way. So how a large amount of stake that is tied to a product engages with the network can have a lot of influence and distortions at times.
 And there are a lot of partner that can help us navigate that. And there are a lot of staking providers that can say that they have good performance and uptime and all these things. But staking and a proof of stake network is not just about that. It's about the small decisions that think about whether the network becomes more useful and easier for app developers. It is about decentralization as well. And so no better partner than Helios and Mert here to help us really understand and navigate that.
 And so that was maybe that kind of the obvious things like Helios is the largest validator and I've been doing it and great performance and all these things. But maybe the kind of less obvious thing is that it was important to us to have a partner that we can feel can guide us there. Yeah. Yeah. And Mert, we'd love to hear from you on what's unique about Helios' staking and what does the setup look like for BeSoul specifically? Sure.
 So what's unique? Well, we are one of the only teams. I mean, there's quite a few. I don't want to like, you know, guess too much. But I would say, first of all, we're extremely network aligned. And what I mean by that is it's very easy to make certain short term decisions to, let's say, boost yield by like, you know, let's say 0.5%, but increasing the risk of, let's say, being front run or the network going down by like 20% or something. But since we actually have another business and our core business is not valid,
 it's actually running infrastructure of which validators are a single part of, we also run by far the most number of nodes on the network, right? We also run RPC nodes, you know, thousands of RPC nodes, which are actually just validator staking nodes, except without voting, which means we've seen basically every possible variation of anything that can go wrong on all different regions in the world. And so when you have institutional money and all eyes are on you,
 you can actually feel safe that, okay, these guys have done this before. They have done it for three years and they've been battle tested, right? Like we've been, not us, but like Solana itself has been attacked. You know, blockchains are relatively adversarial networks and we've been kind of there on the front lines, you know, navigating, okay, how do we get around this, et cetera. And also like the other thing is the stakers themselves, the holders of BSOL get really the best possible economics
 because we don't need to make money ourselves on the stake from Bitwise's validator, right? Our business is running, is helping developers, right? It's making the network faster so that people can actually build the future of internet capital markets, right? Perp stacks is spot trading, borrow land in the fastest possible way on decentralized rails. And then every decision that we make is tailored to help towards that because our goal is to just get people
 to build on Solana. And so this is like a really interesting partnership where like you can literally buy a stock that stakes with Bitwise's validator run by us. But then since we use that to make the network faster, buying the thing can literally help developers build faster applications. I think that's also, that's a really important point from my perspective, like compared to, let's say like a network on Ethereum, Solana,
 the applications really take advantage of the extra, like last 1% of performance to compete and deliver the next kind of marginal amount of more liquidity or marginal amount of scale to their users. So whether the nodes are actually supporting that to the maximum extent does matter. And so the running of the node is not as kind of like, you just download the thing,
 you run it, and there's really not much difference between whether this stake, this validator has more stake or that validator has more stake. The impact on the network, the users, the application that can be built, there's a lot of networks where that really, the relationship doesn't matter as much. But on Solana, the application landscape is changing all the time. The protocol spec is improving, the scale is, so it really does have a big impact.
 And that is a big part of it for us, because ultimately, we want the ecosystem, the developers, the users of Solana, the whole community to feel that the increasing stake weight that comes from this product, this regulated product existing, isn't something that deteriorates the market structure or the ecosystem, but rather plays a role in making it more stable
 and making it more supportive. And yeah, so that's the thing that's really important for us. Great. So before BeSol launched in the US, we had staking and then we had ETFs. But since the launch of BeSol, we now have staking included in ETFs. So curious if you guys can share a little bit about the challenges you faced in getting staking approved and working properly in a regulated ETF product. What do you think? What did your team complain the most about?
 Well, we did all the hard work of waiting for the Bitwise team to figure it out. We just, our job is really the technical side of things, right? So, you know, ETFs will have specific reporting requirements. So we need to get quite high quality data, check the accuracy, make sure that, you know, the granularity of the data, but also Solana is kind of hard to read and make sense of, right? And for an institutional product like this, if the data is, you know, if there's even,
 the slightest kind of error in the little detail, that ends up kind of maybe missing investors. But since we're a data infrastructure company, we really take that seriously. So, but I would say that was, that's something we take super seriously. And so that was a unique challenge for us because most of our customers aren't, you know, the first staking ETF for Solana. But I'm sure you guys had a much different story there. No, I think reporting is definitely one of the ones, because if you think about an ETF, it has a daily reconciliation and strike,
 striking of NAV and such. So the 4 p.m. Eastern to the 4 p.m. Eastern has to be exact. And what was exactly the staking rewards that were accumulated in that time? And then it's not just, we have a view, we need to send that to our fund administrators, the custodian, and our auditors all have to reconcile and audit that on a daily schedule. And so those are the kind of additional requirements of a regulated product
 and that's what we're working on right now. So I think, yeah, that's definitely one of the elements of oversight and like multi-party reconciliation on a daily basis is a time onerous and onerous about making a product like this work. But at the same time, it's really also a thing that drives a lot of confidence in these products as well. Like you can know when the NAV moves up this much on a daily basis, like that is actually what happened. And so, yeah, that's definitely one of the elements. And then after that, it was really like working with the SEC on getting them comfortable with how Solana staking works.
 And stuff like that, yeah. Great. So Hong, as the audience likely has, you know, institutional investors, how does Bitwise go about explaining how Solana staking works to institutions? Yeah, that's a good question. I think the, enough people have heard about proof of stake that they understand what roughly it is or the kind of the role that it plays.
 And I think that's a really good question. I think that's a really good question. I think that's a really good question.
 I think that's a really good question.
 I think that's a really good question. I think that's a really good question.
 I think that's a really good question. I think that's a really good question.
 I think that's a really good question. I think that's a really good question.
 I think that's a really good question. I think that's a really good question.
 I think that's a really good question. I think that's a really good question.
 I think that's a really good question. I think that's a really good question. I think that's a really good question.
 I think that's a really good question. I think that's a really good question.
 I think that's a really good question. I think that's a really good question. I think that's a really good question.
