# U-LEAD: Universal Ultra-Lightweight Solutions for Edge Applications & Devices

## Introduction

- **Motivation:** Deep learning models in computer vision have achieved remarkable accuracy, but often at the cost of heavy computation and memory demands. This creates a barrier for researchers and practitioners with limited resources, and prevents deployment on edge and mobile devices.

- **Vision of U-LEAD:** We explore ultra-lightweight solutions that make computer vision more accessible and efficient without sacrificing too much accuracy.

- **Key Focus Areas:**

  - **Light Training:** fast, resource-friendly training suitable for CPUs or low-end GPUs.

  - **Light Inference:** low-latency deployment optimized for real-time applications.

  - **Light Models:** compact backbones designed for constrained hardware.

- **Goal:** Provide a sandbox of methods, baselines, and experiments that demonstrate how compact design choices can unlock wider accessibility of computer vision research and applications.

## Methods

1. **Light Training Techniques:**

   - Knowledge distillation from larger models.
   - Efficient data augmentation strategies.
   - Optimized training schedules and learning rate policies.

2. **Light Inference Strategies:**

   - Model pruning and quantization.
   - Efficient convolutional operations (e.g., depthwise separable convolutions).
   - Neural architecture search for lightweight models.
   - Dynamic inference techniques.

3. **Light Model Architectures:**

   - Designing compact backbones (e.g., MobileNet, ShuffleNet).
   - Exploring transformer-based models with reduced parameters.
   - Low-rank approximations and tensor decompositions.
