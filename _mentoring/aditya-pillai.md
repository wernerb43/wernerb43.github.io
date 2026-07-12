---
title: "PySRCar: Learning Planar Vehicle Dynamics in MuJoCo with Symbolic Regression"
collection: mentoring
type: "Undergraduate Researcher"
permalink: /mentoring/aditya-pillai
date: 2025-12-15
excerpt: "Symbolic regression of continuous-time vehicle dynamics from MuJoCo simulation data."
---

**Mentee:** Aditya Pillai

**Project:** PySRCar uses MuJoCo to simulate a planar "car" (rigid block with translational and yaw degrees of freedom) and applies PySR symbolic regression to recover closed-form expressions for the vehicle's continuous-time dynamics from logged rollout data. The pipeline generates clean state-control trajectories under a circular-tracking controller, then fits explicit equations for velocities and accelerations using finite-difference derivatives and a small operator library. The learned expressions successfully recover the kinematic identities and produce reasonable acceleration models as a foundation for future data-driven control.

[Report (PDF)](/files/aditya_pillai.pdf)
