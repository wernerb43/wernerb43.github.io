---
title: "Architecture Is All You Need: Diversity-Enabled Sweet Spots for Robust Humanoid Locomotion"
collection: publications
permalink: /publication/2025-architecture-is-all-you-need
excerpt: ''
date: 2025-10-16
venue: 'arXiv'
citation: 'B Werner, L Yang, AD Ames. (2025). &quot;Architecture Is All You Need: Diversity-Enabled Sweet Spots for Robust Humanoid Locomotion.&quot; <i>arXiv:2510.14947</i>.'
---

Robust humanoid locomotion in unstructured environments requires architectures that balance fast low-level stabilization with slower perceptual decision-making. We show that a simple layered control architecture (LCA), a proprioceptive stabilizer running at high rate, coupled with a compact low-rate perceptual policy, enables substantially more robust performance than monolithic end-to-end designs, even when using minimal perception encoders. Through a two-stage training curriculum (blind stabilizer pretraining followed by perceptual fine-tuning), we demonstrate that layered policies consistently outperform one-stage alternatives in both simulation and hardware. On a Unitree G1 humanoid, our approach succeeds across stair and ledge tasks where one-stage perceptual policies fail. These results highlight that architectural separation of timescales, rather than network scale or complexity, is the key enabler for robust perception-conditioned locomotion.

[[PDF]](https://arxiv.org/pdf/2510.14947)
