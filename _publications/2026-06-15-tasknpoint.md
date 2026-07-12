---
title: "TaskNPoint: How to Teach Your Humanoid to Hit a Backhand in Minutes"
collection: publications
permalink: /publication/2026-tasknpoint
excerpt: ''
date: 2026-06-15
venue: 'arXiv'
citation: 'B Werner, I Demler, P Perona, AD Ames. (2026). &quot;TaskNPoint: How to Teach Your Humanoid to Hit a Backhand in Minutes.&quot; <i>arXiv:2606.26215</i>.'
---

How do we learn to hit a tennis backhand? Not from a thousand hours of tennis tournaments on TV — we work with a coach and practice. We argue this is also the right recipe for teaching dynamic skills to humanoid robots. This follows from a structural property of dynamic skills: the outcome is decided by a short, crucial portion of the trajectory — for a backhand, the ~20cm of racket travel around ball contact. Getting this interaction window right requires coordinating the whole motion, so that control, physics, and morphology act in concert. Learning thus reduces to mastering a handful of distinct actions and, for each, practicing until the window comes out right. To this end, we introduce TaskNPoint, a training protocol which makes the coach-learner division of labor explicit. The human coach contributes four inputs: a discrete set of skills (e.g. different shots), one demonstration per skill, identification of the interaction window, and the goal. Learning in a physically realistic simulation environment fills in each action trajectory and provides robustness to unmodeled events. Crucially, randomized target sampling during training lets a single demonstration generalize zero-shot to unseen goal locations. We test this approach on a Unitree G1 humanoid that hits forehands and backhands against balls thrown by a human, kicks incoming soccer balls, and picks and places boxes from novel locations. We find that learning is successful from short human video demonstrations and under an hour of training on a single GPU, with no per-task reward tuning.

[[PDF]](https://arxiv.org/pdf/2606.26215) [[Code]](https://github.com/wernerb43/tasknpoint) [[Project Page]](https://ilonadem.github.io/tasknpoint_website/)
