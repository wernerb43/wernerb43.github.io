---
title: "Diffusion vs. Flow Matching: Benchmarking Generative Models on 2D Spatial Manifolds for Robotic Control"
collection: mentoring
type: "Undergraduate Researcher"
permalink: /mentoring/clare-wu
date: 2026-06-01
excerpt: "Benchmarking diffusion and flow matching models for robotic trajectory generation on 2D geometric distributions."
---

**Mentee:** Clare Wu

**Project:** This work benchmarks Diffusion and Flow Matching models across three 2D distributions (Two Moons, Gaussian Blobs, Checkerboard Grid) as proxies for multi-modal robotic action spaces. Using a shared Fourier-feature MLP backbone for fair comparison, the study evaluates DDPM, DDIM, momentum solvers, Base Flow Matching, VP Flow Matching, and Rectified Flow on distributional accuracy (Energy Distance), training cost, and inference time. Rectified Flow achieves the lowest structural bias and up to a 14× reduction in distributional error on discontinuous boundaries while significantly reducing training overhead—with direct implications for real-time robotic trajectory generation.

[Report (PDF)](/files/clare_wu.pdf)
