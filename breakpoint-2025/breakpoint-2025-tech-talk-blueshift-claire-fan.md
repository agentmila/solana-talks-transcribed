---
title: "Breakpoint 2025: Tech Talk: Blueshift (Claire Fan)"
source: "https://www.youtube.com/watch?v=oO-r-i_DlCg"
date: "2025-12-12"
transcribed: "2026-04-28"
model: "whisper.cpp large-v3"
language: "en"
words: 1299
duration_seconds: 556
tags: [transcript, breakpoint-2025, solana, conference]
series: Breakpoint 2025
series_index: 087
---

# Breakpoint 2025: Tech Talk: Blueshift (Claire Fan)

**Event:** [Breakpoint 2025](https://www.youtube.com/playlist?list=PLilwLeBwGuK4dz_gqiiDA3GfS094Yr46b)
**Date:** 2025-12-12
**Duration:** 9 min
**Transcription:** 1299 words
**Model:** whisper.cpp large-v3
**Playlist position:** 087/199

---

## Transcription

 Hello, everyone. I'm Claire from BlueShift. And today, I'm talking about SBPF linker and compilers. And so I think this tweet pretty much sums up the developer experience of Solana, that it is pretty terrible. And so part of the reasons behind that from the toolchain perspective is that Solana uses BPF. But instead of adapting from upstream
 eBPF, we created this custom SBPF backend and also maintained a fork of the ROS compiler. And so whenever there is an upstream upgrade or improvement, it takes time to pull down those changes. And sometimes it's so diverged that it's impossible to do so. But then in my opinion, there's no real reason to do that. Because yes, eBPF is very constrained. It's something used inside of kernels. So it's very limited in many ways.
 But Solana compilers use LLVM that supports all kinds of targets and that don't have these limitations. And so LLVM is well capable of supporting these features. And so I believe if we can find the right transform path or configure a compiler in a proper way, then it should just work. And so I like to take this chance to demystify compilers.
 I cannot treat them as a black box. But compilers are just softwares. It's a software that takes the source code of your program as input and runs through pipelines of transforms and generate code that you can deploy on your hardware. It's also the first layer that makes your program portable. That's why you can compile and run the same ROS program on a Windows computer, on a MacBook, or even on the Raspberry Pi.
 And so in the middle of the compilation pipeline, it starts to generate machine instructions. But computers still don't read them, right? Computers still only read binaries. And so we have to pack them into a bytecode format that this machine understands. So for eBPF targets, they use the ELF format. It stands for executable and linkable file. And it starts with ELF headers, program headers, and ends with section headers.
 And then in the middle is the sections you use to compose a program. And I'll use the Solana program to give you a concrete example. So Dane did anatomy on the SPPF bytecode. We basically figure out the sections we need to compose a Solana program. And so just like any other ELF files, it starts with the ELF header, which also tells you the architecture and entry point that points to, like, the first instruction got executed.
 And then the next, we've got three program headers for dynamic programs. But we also realized that for static programs, we don't need any program headers. And right now, the only thing that make a program dynamic is syscalls, because SVM does dynamic relocation for syscalls. And so that's why we've been pushing the direction of static syscalls, because if we do that, then we don't need any program headers. Like, we can save all these bytes.
 And so next is text section, which is the code of your program. So if you, like, decode these bytes, you'll get the disassembly of your program. And next, this program is logging Hello, Solana. So then the string is stored in the read-only section. And-- ah, OK. This is not updated. And then the symbol is referenced by one
 of the load instructions in text. And so next, we've got all these sections, tables, to basically facilitate dynamic relocation for syscalls. I'll skip, like, how that works today. But basically, SVM looks into these sections and tables and figure out, oh, I'm actually doing a Sol lock at this code instruction at this program offset. So then, again, if we do static syscalls by just encoding the hash of the function into the code,
 then, like, we don't need any of these. And then the last-- the bottom part is the section headers, which indicates the size offset types of the sections we just went through. So, like, now that you understand this, like, you can hand roll this, right? Like, you can create a Solana program by just using Vim. But don't do it. You're going to be blocked by many people after this talk.
 And so how do we get here? How do we get here from upstream eBPF? And then, like, what is upstream eBPF? So five years ago, an Italian guy added the BPF target to the ROS compiler, meaning that kernel developers can now write ROS programs and use ROS compiler to generate BPF programs and deploy them into kernels. And because of the ROS compilation model,
 the linker is added as part of the new target support. So ROS compiles each dependency, each crate, as a standalone compilation unit. So then we need a linker to basically merge all the dependencies and generate one single executable file. And so let's look at the bytecode that generated from upstream eBPF to BPF linker. Right, so I'll just point out the difference here.
 First, upstream eBPF does relocation for read-only data. So then we basically need to reverse the relocation and figure out which symbol is actually loading and then encode that offset into the load instruction. And then second is upstream eBPF does static syscalls. And so we do the opposite for them. We basically convert them into dynamic relocation-based syscalls.
 And in all those sections and tables we just-- in the previous slides. And so then, again, if we do static syscalls, then we can save this big step. And it works pretty well in the upstream. And so I hope things have become somewhat trivial here. To generate a Solana program from upstream eBPF, we only need two things. One is a BPF linker to compile ROS programs into one single object file.
 And then another tool to basically repackage this into a bytecode format that SVM understands. So we actually have that for a while. For people who have been following BlueShift, you might know that we have a SPPF assembler that's not dependent on any LLVM toolchain. And this is actually what powers the SPPF linker. How it works is it parses the assembly program into abstract syntax tree.
 And we can do a lot of calculating offset, sizes, generating sections, headers, and encoding instructions, generating dynamic relocation for syscalls. And so basically do a direct bytecode generation for a Solana program. So the only difference between the assembler and the linker is just that assembler parses a string file, while the linker parses an object file. And so if you look at the code for SPPF,
 this is all it's doing. First, call the BPF linker to link to a single object file. And then we grab that object file. And then we reparse it and generate a Solana program from the AST. And so that's about SPPF linker. The last thing I want to mention is just that now that work with upstream eBPF is possible-- and I'm quoting Ding here-- we should stop being a bad consumer of the technology we're using.
 We should try to be a good contributor. So for example, if I find something useful for the BPF target in general, we should try to upstream it so that people outside Solana can also benefit from it. To me, this is not just about credibility. I think from an engineering perspective, if I have an optimization pass, the more people use it, the more bulletproof it will become. Because it will be better tested, and more edge cases will be discovered.
 And I think SPPF linker opens up that path. And so for people who are interested, check our website, follow our Twitter. And that's all I have today. Thank you very much.
