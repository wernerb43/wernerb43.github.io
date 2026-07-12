---
title: "A Past Is All a Robot Needs: Structured Graph Memory and Retrieval for Lifelong Robot Learning"
collection: mentoring
type: "Undergraduate Researcher"
permalink: /mentoring/firdavs-nasriddinov
date: 2026-06-01
excerpt: "Cross-session memory system for VLA robots using a typed knowledge graph and Personalized PageRank retrieval."
---

**Mentee:** Firdavs Nasriddinov (with Aditya Pillai)

**Project:** This work presents an end-to-end cross-session memory system for vision-language-action (VLA) robots. Raw robot experiences are ingested by a VLM and consolidated into a structured graph with four node types—episodes, concepts, procedures, and claims—connected by typed, polarity-bearing edges. At query time, retrieval proceeds by Personalized PageRank over the graph rather than flat embedding similarity, preserving safety contraindications. An agentic VLM reads retrieved memory and selects the next skill primitive for the low-level policy. On the FindingDory benchmark the system leads all deployable baselines on both node retrieval (MRR 0.84) and answer quality (LLM-judge 3.8/5). On two memory-gated manipulation tasks, memory conditioning lifts task success from 47% to 83% and 68% to 100% while cutting safety violations several-fold.

[Report (PDF)](/files/firdavs_nasriddinov.pdf)
