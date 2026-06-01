---
title: "Breakpoint 2025: Swig: The Future of Smart Wallets on Solana (Justin Blumenthal)"
source: "https://www.youtube.com/watch?v=zJRUPue-pq0"
date: "2025-12-13"
transcribed: "2026-04-29"
model: "whisper.cpp large-v3"
language: "en"
words: 733
duration_seconds: 297
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 173
---

# Breakpoint 2025: Swig: The Future of Smart Wallets on Solana (Justin Blumenthal)

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-13
**Duration:** 4 min
**Transcription:** 733 words
**Model:** whisper.cpp large-v3
**Playlist position:** 173/199

---

## Transcription

 Wallets are brittle. They're clunky. If you lose your seed phrase, your assets are literally gone. For those of us who have been building in this space for years, this experience is downright infuriating. It's frustrating. And so we set out to build a better way. That better way is Swig Smart Accounts. I'm Justin Blumenthal, CEO of Swig, and we are building hyper-programmed
 programmable open-source wallets on Solana. Swig is deeply composable with flexible signing methods, chain abstraction across the SVM, and a robust on-chain policy engine for advanced security and complex DeFi strategies. Oops, going backwards. Sorry about that. With Swig, users can bring the simplicity of Web2 logins to the power of on-chain wallets.
 They can log in with an email, or an SMS, a passkey, or a wallet. And then under the hood, Swig will tie the user's identity to their wallet. Once authenticated, the user now has full control over their Swig programmable account. They can do things like sign flexibly with keys on the SVM or EVM. They can construct policies in our on-chain policy engine to do really cool things like set session limits, and time-based limits, and token-based limits, oracle-based limits.
 And much more. The best thing about this is there are no seed phrases involved at all. Digging a little deeper, roles are at the heart of Swig's programmability. You can think of roles as the policies that underlie the Swig protocol. With Swig's slot-based architecture, we support up to 65,000 different roles on a single Swig wallet. This provides for maximum programmability.
 And with Swig's application, we provide up to 25,000 different roles. You can think of the authority as who can take action on the wallet. And permissions dictate what can be done. So when combined, you can do really cool things like, say, set a spend limit on the amount of Solana that can be spent in a given day. Or you can set a rebalancing strategy that rebalances Sol when the price reaches a certain level. This is very important to note here, is we constructed our policy engine to be natively on-chain within the context.
 And we have a smart wallet contract, which means no TEEs involved at all. Now, you might be asking, understandably so, how does this impact the performance of my application? Well, we designed Swig to be highly flexible without performance trade-offs. In fact, when you look at the compute unit cost for an SPL token transfer, or the cost to create an account, it's actually orders of magnitude less than other smart wallets on the market today.
 And when I was working with developers early on, it became very clear that they needed a wallet that was highly flexible without adding latency or program bloat to their applications. One of those customers I am very happy to announce is Glider. As of today, Glider is now live on Solana, powered by Swig. We've been working with Brian, John, and the rest of the Glider team for the last several months to help them come to market.
 And so, given the available wallet tooling on Solana. But now with Swig, Glider's customers get access to our gasless paymaster, dynamic portfolio subaccounts, and complex DeFi auto-rebalancing strategies. We're really excited for Glider's next phase of growth on Solana. And we're also thrilled to see Swig being used in several other exciting contexts. One of those is institutional DeFi. We're excited to announce that Swig is working with Anchorage
 to allow access to Solana DeFi in a safe and secure way. We're also excited to be working with the Avicii team to power their neo-banking payment card. The Avicii team made it clear that they needed a smart wallet that could provide 24/7 uptime without dependencies on trusted infrastructure. And lastly, we're also excited to see Swig being used for agentic finance use cases. We're working with the Corbitz team to help them power their X402 facilitator
 on Solana. We're really excited about teams building in each of these categories. So if that's one of you, please reach out. And so, in closing, Swig is live today. Our open source SDKs are available in TypeScript and Rust. So please download those. And reach out to us with any questions or feedback that you might have. We cannot wait to see what you build with Swig. Thank you.
