# U-LEAD: Universal Ultra-Lightweight Solutions for Edge Applications & Devices

## Introduction

- **Motivation:** Deep learning models in computer vision have achieved remarkable accuracy, but often at the cost of heavy computation and memory demands. This creates a barrier for researchers and practitioners with limited resources, and prevents deployment on edge and mobile devices.

- **Vision of U-LEAD:** We explore ultra-lightweight solutions that make computer vision more accessible and efficient without sacrificing too much accuracy.

- **Key Focus Areas:**

  - **Light Training:** fast, resource-friendly training suitable for CPUs or low-end GPUs.

  - **Light Inference:** low-latency deployment optimized for real-time applications.

  - **Light Model:** compact backbones designed for constrained hardware.

- **Goal:** Provide a sandbox of methods, baselines, and experiments that demonstrate how compact design choices can unlock wider accessibility of computer vision research and applications.

## Methods

<table>
  <colgroup>
    <col width="25%">
    <col width="25%">
    <col width="25%">
    <col width="25%">
  </colgroup>
  <thead>
    <tr>
      <th>Category</th>
      <th>Light Model</th>
      <th>Light Training</th>
      <th>Light Inference</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Quantization</td>
      <td>
        <ul>
          <li>Post-Training Quantization (PTQ)</li>
          <li>Weight Clustering</li>
          <li>Calibration</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Quantization-Aware Training (QAT)</li>
          <li>PACT</li>
          <li>LSQ</li>
          <li>DoReFa</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>INT8 Runtime Kernels</li>
          <li>INT4 Runtime Kernels</li>
          <li>Mixed Precision Execution</li>
          <li>TensorRT</li>
          <li>TVM</li>
          <li>ONNX Runtime</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>Pruning / Sparsity</td>
      <td>
        <ul>
          <li>Magnitude Pruning</li>
          <li>Structured Pruning</li>
          <li>Low-Rank Factorization (SVD, CP, Tucker)</li>
          <li>Weight Sharing</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Gradual Pruning</li>
          <li>Lottery Ticket Hypothesis</li>
          <li>Sparsity Regularization</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>N:M Sparse Kernels</li>
          <li>Sparse Matrix Multiplication</li>
          <li>Hardware-Accelerated Sparsity</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>Architecture Design</td>
      <td>
        <ul>
          <li>MobileNet</li>
          <li>ShuffleNet</li>
          <li>SqueezeNet</li>
          <li>GhostNet</li>
          <li>TinyViT</li>
          <li>MobileViT</li>
          <li>RepVGG</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Slimmable Networks</li>
          <li>Progressive Width Training</li>
          <li>Progressive Depth Training</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Dynamic Depth</li>
          <li>Dynamic Width</li>
          <li>Dynamic Convolution</li>
          <li>Input-Adaptive Routing</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>Knowledge Distillation</td>
      <td>
        <ul>
          <li>Student Model</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Logit Distillation</li>
          <li>Feature Distillation</li>
          <li>Relational Distillation</li>
          <li>Multi-Teacher Distillation</li>
        </ul>
      </td>
      <td>
        <ul></ul>
      </td>
    </tr>
    <tr>
      <td>Neural Architecture Search</td>
      <td>
        <ul>
          <li>Once-for-All</li>
          <li>MnasNet</li>
          <li>MobileNetV3</li>
          <li>TinyNAS</li>
        </ul>
      </td>
      <td>
        <ul></ul>
      </td>
      <td>
        <ul></ul>
      </td>
    </tr>
    <tr>
      <td>Re-parameterization / Fusion</td>
      <td>
        <ul>
          <li>BatchNorm Folding</li>
          <li>Convolution Fusion</li>
          <li>RepVGG Re-parameterization</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Multi-Branch Training</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Operator Fusion</li>
          <li>Kernel Scheduling</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>Regularization / Efficient Training</td>
      <td>
        <ul></ul>
      </td>
      <td>
        <ul>
          <li>LoRA</li>
          <li>Adapters</li>
          <li>Partial-Freezing</li>
          <li>Curriculum Learning</li>
          <li>Progressive Resizing</li>
          <li>Early Stopping</li>
          <li>Mixed Precision Training</li>
          <li>Gradient Checkpointing</li>
          <li>Gradient Compression</li>
        </ul>
      </td>
      <td>
        <ul></ul>
      </td>
    </tr>
    <tr>
      <td>Data / Federated Learning</td>
      <td>
        <ul></ul>
      </td>
      <td>
        <ul>
          <li>Few-Shot Learning</li>
          <li>Meta-Learning</li>
          <li>Self-Supervised Learning</li>
          <li>Federated Averaging</li>
          <li>Continual Learning</li>
          <li>Personalization</li>
        </ul>
      </td>
      <td>
        <ul></ul>
      </td>
    </tr>
    <tr>
      <td>Dynamic / Adaptive Inference</td>
      <td>
        <ul>
          <li>Branchy Networks</li>
        </ul>
      </td>
      <td>
        <ul></ul>
      </td>
      <td>
        <ul>
          <li>Early-Exit</li>
          <li>Cascaded Models</li>
          <li>Anytime Prediction</li>
          <li>Edge–Cloud Split</li>
          <li>Adaptive Resolution</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>Temporal / Streaming</td>
      <td>
        <ul></ul>
      </td>
      <td>
        <ul></ul>
      </td>
      <td>
        <ul>
          <li>Feature Caching</li>
          <li>Key-Frame Propagation</li>
          <li>Asynchronous Inference</li>
          <li>Batchless Inference</li>
          <li>Memory Pinning</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
