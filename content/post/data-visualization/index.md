---
title: "From Research to Production: Deploying Deep Learning on Embedded Hardware"
summary: Practical lessons from deploying TensorFlow and PyTorch models to TensorRT on Jetson AGX Xavier - quantisation, latency trade-offs, and ONNX conversion.
date: 2023-06-01

authors:
  - admin

tags:
  - Deployment
  - TensorRT
  - ONNX
  - Embedded
  - Docker
---

After years of research, I spent several years at Instech Netherlands deploying deep learning models into production - including on embedded hardware like the NVIDIA Jetson AGX Xavier. This post shares the practical lessons that research papers don't cover.

## The Gap Between Benchmark and Production

A model that scores well on your validation set is the beginning, not the end. Production deployment introduces constraints that fundamentally change the engineering problem:

- **Latency budgets**: A CT scan analysis that takes 10 minutes is useless in an emergency workflow.
- **Memory constraints**: Embedded devices have a fraction of the RAM of a workstation GPU.
- **Reproducibility**: Your Docker container must produce identical results on a Jetson as on a cloud A100.

## The TensorRT Pipeline

The standard path I used: train in PyTorch or TensorFlow → export to ONNX → compile to TensorRT engine.

```
PyTorch model → torch.onnx.export() → ONNX graph → trtexec → TensorRT engine
```

Each step has failure modes. ONNX export can silently drop dynamic shapes. TensorRT compilation fails on unsupported ops. The key is to validate intermediate outputs at each stage against a known-good reference.

## Quantisation Trade-offs

FP16 quantisation is almost always safe for computer vision models - I rarely saw more than 0.5% drop in Dice score on segmentation tasks. INT8 requires careful calibration and more validation, but the latency gains are significant on devices without FP16 tensor cores.

For medical imaging specifically: validate quantised models on a representative slice of edge cases, not just average accuracy. A small accuracy drop on average can hide large errors on the cases that matter most.

## Docker as the Deployment Contract

Every model I deployed was wrapped in a Docker container with pinned versions of CUDA, cuDNN, TensorRT, and the application code. This single decision eliminated an entire class of "works on my machine" bugs. On the Jetson, we used NVIDIA's L4T base images to guarantee hardware compatibility.

## Lessons

1. Profile before optimising - the bottleneck is rarely where you expect.
2. ONNX is a good intermediate format but inspect the graph; some exporters produce redundant nodes.
3. Build your validation pipeline before you build your model. It will save you weeks.
