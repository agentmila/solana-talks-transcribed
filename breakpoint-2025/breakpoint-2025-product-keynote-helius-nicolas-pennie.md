---
title: "Breakpoint 2025: Product Keynote: Helius (Nicolas Pennie)"
source: "https://www.youtube.com/watch?v=Yxjk5AuypsE"
date: "2025-12-13"
transcribed: "2026-04-29"
model: "whisper.cpp large-v3"
language: "en"
words: 933
duration_seconds: 304
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 174
---

# Breakpoint 2025: Product Keynote: Helius (Nicolas Pennie)

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-13
**Duration:** 5 min
**Transcription:** 933 words
**Model:** whisper.cpp large-v3
**Playlist position:** 174/199

---

## Transcription

 - Hi everyone, my name's Nick. I'm one of the co-founders at Helios. And today I'm gonna be talking about Get Transactions for Address. This is a new RPC for historical queries. So first, I'll talk a little bit about Helios. We are the API for Internet
 Capital Markets. What that means is we provide RPCs, low latency data streams, and transaction landing services. Now if we talk about history and historical queries on Solana, there's three main methods that exist today. There's Get Block, Get Transaction, and Get Signatures for Address. The problem is quite hard to deal with history on Solana. And the reason is because of the numbers. Solana has over 384 million blocks, 469 billion transactions, and is producing over 3,000 TPS.
 That's gonna go up. If we look at how historical queries work on Solana, what happens is you make an RPC call to Agave, which holds about four days worth of data. If your data's outside of that range, it goes to Google Bigtable, traditionally. The problem though is that Bigtable is really expensive. And also under load, you can have hot partitions, which causes performance degradations. Essentially, it catches on fire. Now if this happens, you're now paying a lot of money for poor performance, and you're gonna be quickly out of a job.
 So with Get Signatures for Address, you're gonna make a query on a specific address, and you get back a bunch of signatures. If you want the actual data, you need to now call Get Transaction for every single one of those signatures. That means you might be making thousands and thousands of RPC calls. This is slow and expensive. Now let's go even further. You can quickly see how you end up chewing a lot of glass. Let's say we wanna look at the transactions for January 2024 for a particular user. You're gonna call Get Signatures for Address all the way until you reach January.
 Now you're gonna call again, going all the way down until you finish the month of January, and you're gonna call Get Transaction for every signature. Now if I've lost you and this is confusing, good. That's the point. It is confusing. That's why we built Get Transactions for Address. This provides flexible sorting. It means you can go forwards in time or backwards in time. I should add, another problem with Get Signatures for Address is you can only query backwards in time. We also provide advanced filtering. So if you wanna filter down for a specific time range, say like a month, you can do that.
 You can also get all the transaction data in one response. This makes things a whole lot easier. Let me show you. So if you look here, we're actually looking at one user's history, that wallet, and we're saying get me all the transactions, like actual transaction details, and I wanna look for the data for the month of January 2024 by providing this block time filter. Also, I'm gonna say get me only the transactions that succeeded. I don't care about the failures. Now, in the response, you get the actual data back
 as well as the pagination token. So there's more data in the response that couldn't be included. You can keep crawling and get more. It makes it all quite easy. Now, let's talk about how it works. How we built this is we got rid of Bigtable. We got rid of Agave. We built the entire thing from the ground up. Loosely speaking, the way it works is as a storage router. And what we do is when you query for data, it basically pulls it from different indices, a custom memory cache, Postgres, and Clickhouse. The result here is that the whole thing is a lot more efficient.
 You don't have to save money by making less RPC calls, and it's a whole lot faster, meaning your app's gonna be faster for your customers. Now, for any of the technical people here, I'll talk a little bit about how it works really quickly. It's powered by an inverted index. What that means is that for every transaction, there's an addresses vector, and that thing is flattened. It means you get an address signature pair, and those pairs for every single permutation for the history of Solana produces an index of over 2.3 trillion rows. We've optimized this down
 so that your range queries on that data, no matter which point in time, is happening in under 50 milliseconds. This whole system also powers getBlock and getTransaction. Transactions consume about one petabyte of storage. We've compressed that down to 288 terabytes. We've optimized it down from code to networking such that getBlock can happen in under 70 milliseconds. Now, if I've lost you again, here's a UI visual of our new Explorer. If you look at Twilio's wallet, this system is actually powered
 by our new getTransactionsForAddress, and you can see we can skip right to the oldest transaction. We can also go and look at its history, and we can say, okay, give me exactly the data for the 27th of November. And we can also now filter by success, so we only see the transactions that succeeded. This gives you a kind of visual example of how all this is built behind the scenes and powered by the same method I talked about, getTransactionsForAddress. And that's all for today. Thank you so much for listening. If you have any questions, check out our blog or reach out to me.
 ♪ ♪
