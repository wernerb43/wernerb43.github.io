---
title: "Real-time Tracking of Fast-moving Tennis Balls"
collection: mentoring
type: "Undergraduate Researcher"
permalink: /mentoring/samantha-chang
date: 2026-06-01
excerpt: "Stereo vision pipeline with blur-aware detection and Kalman filtering for 3D tennis ball trajectory estimation."
---

**Mentee:** Samantha Chang

**Project:** This project develops a real-time 3D tracking pipeline for tennis balls thrown toward a ZED 2 stereo camera, with the goal of enabling a humanoid robot to catch them. The pipeline combines a BlurBall blur-aware detector (treating motion blur as a localization cue rather than noise), stereo triangulation via the ZED SDK point cloud, and a Kalman filter with constant-acceleration model for trajectory prediction. Four detector classes were evaluated—SAM2/EfficientTAM segmentation, YOLO, TrackNet, and BlurBall—with BlurBall providing the most reliable center estimates on high-speed blurred frames. Validation against OptiTrack motion capture shows good x/y agreement throughout the ball's flight, with depth (z) estimation identified as the primary remaining challenge.

[Report (PDF)](/files/samantha_chang.pdf)
