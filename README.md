<div align="center">

# Karan Anchan

**Machine-learning research and engineering**

M.Sc. Computer Science (AI) · University of Freiburg · Freiburg, Germany

![Research: reinforcement learning](https://img.shields.io/badge/research-reinforcement_learning-7aa2f7?style=flat-square&labelColor=0b0e14)
![Research: language models](https://img.shields.io/badge/research-language_models-4ec9b0?style=flat-square&labelColor=0b0e14)
![Engineering: edge vision](https://img.shields.io/badge/engineering-edge_vision-ffb454?style=flat-square&labelColor=0b0e14)
![Engineering: retrieval systems](https://img.shields.io/badge/engineering-retrieval_systems-b8a2d4?style=flat-square&labelColor=0b0e14)

[Portfolio](https://karan-anchan.github.io/) · [LinkedIn](https://www.linkedin.com/in/karan-anchan/) · [Email](mailto:kar.anchan02@gmail.com)

</div>

---

I build and evaluate machine-learning systems across reinforcement learning, language models, computer vision, and retrieval. I care about the conditions behind a result: the data, compute budget, evaluation protocol, and limits of the evidence.

## Selected projects

### [YOLO26 edge deployment](https://github.com/Karan-Anchan/edge-yolo26-deployment)

![Runtimes: GPU, CPU, browser](https://img.shields.io/badge/runtimes-GPU_%7C_CPU_%7C_browser-ffb454?style=flat-square&labelColor=0b0e14)
![TensorRT FP16: 1.9 milliseconds p50 model latency](https://img.shields.io/badge/TensorRT_FP16-1.9_ms_p50-4ec9b0?style=flat-square&labelColor=0b0e14)

Fine-tuned YOLO26-s on SKU-110K and built TensorRT GPU, ONNX Runtime CPU, and browser WebGPU inference paths. On the tested RTX 5070, TensorRT FP16 recorded **1.9 ms p50 model latency**, **0.5713 mAP@50–95**, and **58 W board power**. These are model and hardware measurements, not end-to-end video throughput. [Showcase and live browser demo](https://karan-anchan.github.io/edge-yolo26-deployment/).

### [RLPD offline-to-online reinforcement learning](https://github.com/Karan-Anchan/rlpd-offline-to-online-rl)

![Methods: RLPD, IQL, SACfD](https://img.shields.io/badge/methods-RLPD_%7C_IQL_%7C_SACfD-7aa2f7?style=flat-square&labelColor=0b0e14)
![Evaluation: three seeds per method](https://img.shields.io/badge/evaluation-3_seeds_per_method-4ec9b0?style=flat-square&labelColor=0b0e14)

I worked with two collaborators to reproduce RLPD in PyTorch and compare it with IQL and SACfD on Hopper, Walker2d, and HalfCheetah (three seeds per method). At 245k online steps, RLPD's mean returns were **88.0 / 89.6 / 88.6** on this project's random-policy = 0, measured-expert = 100 scale. We also tested replay composition on Humanoid-v5 and analyzed offline-state coverage. [Research showcase](https://karan-anchan.github.io/rlpd/).

### [Mamba–attention hybrid language model](https://github.com/Karan-Anchan/mamba-hybrid-lm)

![Variants: three hybrid models](https://img.shields.io/badge/variants-3_hybrid_models-b8a2d4?style=flat-square&labelColor=0b0e14)
![Exposure: 700 million sampled positions per model](https://img.shields.io/badge/exposure-700M_sampled_positions%2Fmodel-ffb454?style=flat-square&labelColor=0b0e14)

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
