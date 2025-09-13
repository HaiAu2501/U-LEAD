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

<table width="100%">
  <thead>
    <tr>
      <th width="19%">Category</th>
      <th width="27%">Light Model</th>
      <th width="27%">Light Training</th>
      <th width="27%">Light Inference</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Quantization</td>
      <td>
        <ul>
          <li>Post-Training Quantization (PTQ)</li>
          <li>Weight Clustering [<a href="https://arxiv.org/abs/1811.01907">paper</a>]</li>
          <li>Calibration</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Quantization-Aware Training (QAT)</li>
          <li>Parameterized Clipping Activation (PACT) [<a href="https://arxiv.org/abs/1805.06085">paper</a>]</li>
          <li>Learned Step Size Quantization (LSQ) [<a href="https://arxiv.org/abs/1902.08153">paper</a>]</li>
          <li>DoReFa [<a href="https://arxiv.org/abs/1606.06160">paper</a>]</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>INT Runtime [<a href="https://arxiv.org/abs/2101.01321">paper</a>, <a href="https://arxiv.org/abs/1912.12607">paper</a>]</li>
          <li>Mixed Precision Execution [<a href="">paper</a>]</li>
          <li>TensorRT</li>
          <li>Tensor Virtual Machine (TVM)</li>
          <li>ONNX Runtime</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>Pruning & Sparsity</td>
      <td>
        <ul>
          <li>Magnitude Pruning [<a href="https://arxiv.org/abs/1506.02626">paper</a>]</li>
          <li>Structured Pruning [<a href="https://arxiv.org/abs/1608.08710">paper</a>]</li>
          <li>Low-Rank Factorization (SVD, CP, Tucker) [<a href="https://arxiv.org/abs/1906.07671">paper</a>]</li>
          <li>Weight Sharing [<a href="https://arxiv.org/abs/1510.00149">paper</a>]</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Gradual Pruning</li>
          <li>Lottery Ticket Hypothesis [<a href="https://arxiv.org/abs/1803.03635">paper</a>]</li>
          <li>Sparsity Regularization [<a href="https://arxiv.org/abs/1901.07827">paper</a>]</li>
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
          <li>MobileNet [<a href="https://arxiv.org/abs/1704.04861">paper</a>]</li>
          <li>ShuffleNet [<a href="https://arxiv.org/abs/1707.01083">paper</a>]</li>
          <li>SqueezeNet [<a href="https://arxiv.org/abs/1602.07360">paper</a>]</li>
          <li>GhostNet [<a href="https://arxiv.org/abs/1911.11907">paper</a>]</li>
          <li>TinyViT [<a href="https://arxiv.org/abs/2207.10666">paper</a>]</li>
          <li>MobileViT [<a href="https://arxiv.org/abs/2110.02178">paper</a>]</li>
          <li>RepVGG [<a href="https://arxiv.org/abs/2101.03697">paper</a>]</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Slimmable Networks [<a href="https://arxiv.org/abs/1812.08928">paper</a>]</li>
          <li>Progressive Width/Depth Training</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Dynamic Width/Depth</li>
          <li>Dynamic Convolution</li>
          <li>Input-Adaptive Routing</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>Knowledge Distillation [Kiệt]</td>
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
          <li>Once-for-All [<a href="https://arxiv.org/abs/1908.09791">paper</a>]</li>
          <li>MnasNet [<a href="https://arxiv.org/abs/1807.11626">paper</a>]</li>
          <li>MobileNetV3 [<a href="https://arxiv.org/abs/1905.02244">paper</a>]</li>
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
      <td>Re-parameterization & Fusion</td>
      <td>
        <ul>
          <li>BatchNorm Folding [<a href="https://arxiv.org/abs/2203.14646">paper</a>]</li>
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
      <td>Regularization & Efficient Training</td>
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
      <td>Advanced Learning Paradigms</td>
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
      <td>Dynamic & Adaptive Inference</td>
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
      <td>Temporal & Streaming</td>
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
