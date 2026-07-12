---
title: "Graph of Convex Sets Trajectory Optimization for Ground-Aerial Bimodal Robots in Point Cloud Environments"
collection: mentoring
type: "Undergraduate Researcher"
permalink: /mentoring/deon-petrizzo
date: 2026-06-11
excerpt: "Collision-free trajectory planning directly from point clouds using GCS and composite Bézier optimization."
---

**Mentee:** Deon Petrizzo

**Project:** This work develops a kinematic trajectory planner for differentially flat robots (e.g., Caltech's M4 morphobot) operating in cluttered environments described only by raw point clouds. Obstacle-free convex polytopes are grown directly from the cloud via sphere flipping, assembled into a Graph of Convex Sets (GCS), and a composite Bézier trajectory—with separate geometric and timing curves—is optimized as a single second-order cone program (SOCP). The resulting trajectories are collision-free by construction, respect a hard velocity limit in physical units, and are computed in tens of milliseconds, making the approach attractive for online long-horizon planning on multimodal ground-aerial platforms.

[Report (PDF)](/files/deon_petrizzo.pdf)
