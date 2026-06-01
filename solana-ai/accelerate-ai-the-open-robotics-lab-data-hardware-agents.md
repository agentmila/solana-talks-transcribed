---
title: "Accelerate AI: The Open Robotics Lab: Data, Hardware, Agents"
source: "https://www.youtube.com/watch?v=AGYD02X-23U"
date: "2026-05-14"
transcribed: "2026-05-30"
model: "whisper.cpp large-v3"
language: "en"
words: 1088
duration_seconds: 456
tags: [transcript, solana-ai, solana]
series: "SolanaAI"
series_index: 013
---

# Accelerate AI: The Open Robotics Lab: Data, Hardware, Agents

**Event:** [SolanaAI](https://www.youtube.com/playlist?list=PLilwLeBwGuK7DT9ofWtiSe9qbXieLgX-T)  
**Date:** 2026-05-14  
**Duration:** 7 min  
**Transcription:** 1088 words  
**Model:** whisper.cpp large-v3  
**Playlist position:** 013/18

---

## Transcription

 Hi, everyone. I'm Amanda. I'm the CEO of the Bitrobot Foundation. What we're building is what we call the world's open robotics lab. So we're aggregating contributors and resources to further embodied AI. So you probably have heard that over the past year, the robotics world is moving very quickly. So we have up here like the first image at the top that is from
 NVIDIA. So they were able to train a model with just human data, no robot data. Next to that at the top, we have figure. They were able to autonomously unload and load a dishwasher. And then underneath that, we have Dyna. They were able to fold laundry for 24 hours with 99% accuracy. And then next to that, we have Google Gemini. And they were able to build a model that was generalized for manipulation. So it could apply to unseen objects, instructions,
 and robots. But there's still like a major challenge. So you see all this progress, and you're like, why can't robots do what humans can do? And so there's still like a big gap. You change the lighting. You change the environment. You change the robot and everything breaks. And so what this really all comes down to is that a lot more data is needed to train robots. So you can't just scrape the internet. You need to capture three specific types of data.
 We have teleoperation, video, and simulation. These are the three types. And researchers kind of vary in the mix that they want to use or whether they're more focused on one of these. So teleoperation, this would be me piloting a robot, so controlling it and teaching it. It's like the golden standard, but very expensive, not that scalable. We have video. And so this is either trying to make use of like a YouTube exocentric video
 or doing something else. And so what I'm doing right now, so I'm recording egocentric videos. So from my first person point of view, the challenge here is you need to make this useful for robots. So things like action labels, depth estimation. And then there's simulation. So this is synthetic data. And I think there the challenge has been around manipulation and fine-grained tasks. And there's still this sort of sim to real gap. And so researchers are pursuing the mix of all of these.
 So we're focused on helping to solve. Beyond volume, you need quality. And so quality, actually, in the case of robotics, is diversity. So imagine I'm trying to teach a robot to open a doorknob. I want to teach it to open-- I don't want a bunch of hours of myself trying to open the same doorknob. I want a bunch of different doorknobs, a bunch of people and environments trying to open that doorknob so that the robot can be generalized to open all doorknobs.
 So the data sets that we collect is very important. So our solution and how does this all connect to the blockchain? So we are building a protocol on Solana. It's structured as an ecosystem of subnets. So you can think of a subnet as a market focused on producing a particular output for robotics research and development. So it could be a data set. It could be evaluation hours. So in the example here, I'm wearing this RoboCap.
 So this is a sample for egocentric video. Contributors to this subnet can wear this cap, collect themselves-- record themselves doing economically valuable labor, and then earn rewards for their contributions. So the RoboCap subnet. So here I am. I'm wearing this hardware. There's a-- I think should be a green light here. So I'm actually recording right now.
 And so you can see it actually has six cameras. Here there are eight because there's a new product we'll be launching soon called RoboWrist. So I'll be matching this with two wrist cameras right here on my wrists. And we built this hardware ourself. It's purpose-built to collect egocentric video. And it captures also motion.
 And then here you can see we also enhanced the raw video. So we cover the full process. So we have-- we manufacture the hardware. We collect and deploy the raw data. And then we enhance it and annotate it so that it's ready to sell to AI labs. And so here you can see this one is hand tracking. So this is helping with showing kind of like the hand positions on the video. And then this is depth estimation.
 And so these are some of the enhancements that robotics researchers desire around egocentric video. And then, yeah, I should say like right now we are collecting and deploying. But coming soon there'll be ways for the community to get involved in this collection. Another subnet we have is called ET Fuji. So here I have this sidewalk robot. Show it so people can see.
 And so this is collecting urban navigation data. People drive it around. And then it's kind of like Mario Kart in the real world, sort of fun, RC Rover game. But yeah, it's also collecting useful urban navigation data. So we created the largest urban navigation data set in the open used by researchers at Berkeley, Toyota, Princeton, and more. And yeah, here you can see some of the functionality of this little
 robot. The ET Fuji game. So you can see here, this is actually from the view of the robot. So this is what it's seeing as it drives around from its cameras. And yeah, these are available today. You can buy them online, drive them around, and contribute to this urban navigation effort. So you may have seen the robot start to move. So today we're unveiling the Earth Rover.
 Mini plus agent kit. So now we have an open SDK where anyone can create an agent that controls the rover. So it's moving around. I'm not the one moving it. And yeah, you can record it. It's integrated with OpenClaw, Telegram. You can create a bot. You can do actions. We've been also controlling it with Cursor.
 So thank you. And yeah, if you want to learn more about us, here are some ways to follow us on Accent Discord. We also have a table out back if you want to try these agents yourself or try our Rubik's Cube challenge where you're wearing the cap and attempting to solve the Rubik's Cube. So yeah, thank you so much.
 Thank you.
