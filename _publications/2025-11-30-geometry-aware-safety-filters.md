---
title: "Geometry-Aware Predictive Safety Filters on Humanoids: From Poisson Safety Functions to CBF-Constrained MPC"
collection: publications
permalink: /publication/2025-geometry-aware-safety-filters
excerpt: ''
date: 2025-11-30
venue: 'IEEE-RAS International Conference on Humanoid Robots (Humanoids)'
citation: 'RM Bena, G Bahati, B Werner, RK Cosner, L Yang, AD Ames. (2025). &quot;Geometry-Aware Predictive Safety Filters on Humanoids: From Poisson Safety Functions to CBF-Constrained MPC.&quot; <i>2025 IEEE-RAS 24th International Conference on Humanoid Robots (Humanoids)</i>.'
---

Autonomous navigation through unstructured and dynamically-changing environments is a complex task that continues to present many challenges for modern roboticists. In particular, legged robots typically possess manipulable asymmetric geometries which must be considered during safety-critical trajectory planning. This work proposes a predictive safety filter: a nonlinear model predictive control (MPC) algorithm for online trajectory generation with geometry-aware safety constraints based on control barrier functions (CBFs). Critically, our method leverages Poisson safety functions to numerically synthesize CBF constraints directly from perception data. We extend the theoretical framework for Poisson safety functions to incorporate temporal changes in the domain by reformulating the static Dirichlet problem for Poisson's equation as a parameterized moving boundary value problem. Furthermore, we employ Minkowski set operations to lift the domain into a configuration space that accounts for robot geometry. Finally, we implement our real-time predictive safety filter on humanoid and quadruped robots in various safety-critical scenarios. The results highlight the versatility of Poisson safety functions, as well as the benefit of CBF constrained model predictive safety-critical controllers.

[[PDF]](https://arxiv.org/pdf/2508.11129)
