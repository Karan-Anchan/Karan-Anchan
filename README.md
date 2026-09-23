# Karan Anchan

M.Sc. Computer Science (Artificial Intelligence), University of Freiburg · Freiburg, Germany

I build and evaluate machine-learning systems across reinforcement learning, language models, computer vision, and retrieval. I care about the conditions behind a result: the data, compute budget, evaluation protocol, and limits of the evidence.

[Portfolio](https://karan-anchan.github.io/) · [LinkedIn](https://www.linkedin.com/in/karan-anchan/) · [Email](mailto:kar.anchan02@gmail.com)

## Selected projects

### [YOLO26 edge deployment](https://github.com/Karan-Anchan/edge-yolo26-deployment)

Fine-tuned YOLO26-s on SKU-110K and built TensorRT GPU, ONNX Runtime CPU, and browser WebGPU inference paths. On the tested RTX 5070, TensorRT FP16 recorded **1.9 ms p50 model latency**, **0.5713 mAP@50–95**, and **58 W board power**. These are model and hardware measurements, not end-to-end video throughput. [Showcase and live browser demo](https://karan-anchan.github.io/edge-yolo26-deployment/).

### [RLPD offline-to-online reinforcement learning](https://github.com/Karan-Anchan/rlpd-offline-to-online-rl)

I worked with two collaborators to reproduce RLPD in PyTorch and compare it with IQL and SACfD on Hopper, Walker2d, and HalfCheetah (three seeds per method). At 245k online steps, RLPD's mean returns were **88.0 / 89.6 / 88.6** on this project's random-policy = 0, measured-expert = 100 scale. We also tested replay composition on Humanoid-v5 and analyzed offline-state coverage. [Research showcase](https://karan-anchan.github.io/rlpd/).

### [Mamba–attention hybrid language model](https://github.com/Karan-Anchan/mamba-hybrid-lm)

I trained three 16-layer, 52–54M-parameter variants with **700M sampled token positions per model**. In this single-seed comparison, the 1:15 attention:SSM variant used **66.3% less calculated persistent state at 8K** than 1:3, with best validation perplexity **0.212 higher**. That state figure is a model-level estimate, not measured GPU memory. [Research showcase](https://karan-anchan.github.io/mamba-hybrid-lm-showcase/).

## Additional work

- [UNETR 3D abdomen segmentation](https://github.com/Karan-Anchan/Unetr_3D_Abdomen_Segmentation) — PyTorch/MONAI pipeline for 14-label CT segmentation, including spacing resampling, foreground-aware 128³ crops, and sliding-window inference.
- [English–Hindi Transformer](https://github.com/Karan-Anchan/en-hi-nmt-transformer) — 43M-parameter PyTorch model trained on 500k Samanantar pairs; beam search reached 16.93 SacreBLEU on a 500-pair held-out set.
- [Arise](https://github.com/Karan-Anchan/arise) — Offline-first fitness application built with React, TypeScript, and Dexie, with optional Supabase sync.

## Background

- **Machine Learning Intern, WiZdom Ed (2023–24).** Built and evaluated a RAG study-path system over 5,000+ documents. A company-provided 100-batch evaluation reported 71.7% Recall@5, 93.4% groundedness, and 89.1% refusal accuracy.
- **M.Sc. Computer Science (AI), University of Freiburg (2025–present).**
- **B.E. Computer Science, N.M.A.M. Institute of Technology (2020–24).** GPA 9.33/10.

I am open to ML research and engineering internships, working-student roles, and collaborations. [Email me](mailto:kar.anchan02@gmail.com) or see the [portfolio](https://karan-anchan.github.io/) for project details. Outside ML, I photograph nature and wildlife.
