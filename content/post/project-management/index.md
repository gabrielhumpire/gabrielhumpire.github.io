---
title: "End-to-End Computer Vision: From Requirements to Deployed System"
summary: Reflections on 15 years taking CV systems from research prototype to production - what the gap really looks like, and how to close it.
date: 2024-01-15

authors:
  - admin

tags:
  - Computer Vision
  - Engineering
  - ML in Production
---

After 15 years working in computer vision - through a PhD, multiple industry roles, and a few startups - I've shipped systems that went from whiteboard sketch to production deployment. This post is about what that journey actually looks like, and the lessons that only come from doing it end-to-end.

## Requirements Are the Hardest Part

In research, the problem is given to you. In production, you have to discover it. "Detect anomalies in CT scans" is not a requirement. "Flag studies with a sensitivity of at least 92% while keeping false positives below 5% per study, with results available within 3 minutes of scan acquisition, running on a single GPU workstation" - that is a requirement.

Every project I've worked on has been redefined at least once after the first prototype. Building for changeability is more valuable than building for the original spec.

## The Prototype Trap

A prototype that achieves 94% accuracy on your held-out test set is not a product. The questions that matter:

- How does it perform on data from a different scanner model?
- What happens when the input is corrupted or incomplete?
- How does a clinician or operator actually interact with the output?
- What is the failure mode, and is it safe?

Medical imaging taught me this faster than any other domain. A false negative in cancer screening is not an acceptable failure mode.

## Iteration Is the Work

The drone delivery project I led at Embention is a good example. The first detection model worked well in controlled lab conditions. Outdoor lighting, vibration, variable altitude, and regulatory edge cases forced five major architecture revisions before we had something deployable. Each revision was cheaper than the last because we had built good evaluation tooling early.

The 30% latency reduction we eventually achieved did not come from a clever algorithm - it came from profiling, identifying that the bottleneck was preprocessing, and rewriting that stage in C++ with CUDA.

## Deployment Is a Feature

Models don't deploy themselves. Containerisation (Docker), hardware-specific optimisation (TensorRT, ONNX), monitoring, and rollback procedures are engineering work that needs to be planned from day one - not bolted on at the end.

The most valuable skill I have developed is being fluent in both the research side (what the model can learn) and the engineering side (what it will cost to run). That fluency is what makes end-to-end delivery possible.
