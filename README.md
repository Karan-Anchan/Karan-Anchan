<div align="center">

<img src="assets/header.svg" width="900" alt="Karan Anchan — AI researcher & engineer, Freiburg. curiosity over compute; reproduce first, believe later." />

<br/>
<br/>

<a href="https://karan-anchan.github.io/"><img src="assets/btn-portfolio.svg?v=2" width="160" alt="Portfolio — karan-anchan.github.io" /></a>&nbsp;
<a href="https://linkedin.com/in/karan-anchan"><img src="assets/btn-linkedin.svg?v=2" width="160" alt="LinkedIn — karan-anchan" /></a>&nbsp;
<a href="mailto:kar.anchan02@gmail.com"><img src="assets/btn-email.svg?v=2" width="160" alt="Email — kar.anchan02@gmail.com" /></a>&nbsp;
<a href="https://karan-anchan.github.io/CVKaranAnchan.pdf"><img src="assets/btn-cv.svg?v=2" width="160" alt="CV as PDF" /></a>

<br/>

<sub>🎮 &nbsp;flavor on the surface &nbsp;·&nbsp; 🔬 &nbsp;details in the foldouts &nbsp;·&nbsp; <em>open the ▸ panels as you go</em></sub>

</div>

<img src="assets/divider.svg" width="900" alt="" />

## <img src="assets/icon-flask.svg" width="26" align="top" alt="" /> &nbsp;model card · `karan-v3`

*A self-reported model card, with the measurable parts listed below.*

<div align="center"><img src="assets/knight.webp" width="520" alt="animated minecraft knight with cape and diamond sword, walking out of a castle courtyard" /></div>

<br/>

<div align="center">

| field | value |
|---|---|
| **architecture** | curiosity-driven · chai-cooled · stubbornly empirical |
| **pretraining** | B.E. Computer Science (9.33/10) → production ML internship |
| **fine-tuning** | M.Sc. Computer Science (AI) · University of Freiburg 🇩🇪 |
| **alignment** | to measured baselines; vibes are not an eval |
| **known limitations** | will re-run your experiment with 3 seeds before agreeing with it |
| **intended use** | research collaborations · working-student roles · hard problems |

</div>

<details>
<summary>&nbsp;🔬 &nbsp;<b>full spec sheet</b> · the verifiable part</summary>

<br/>

| | |
|---|---|
| M.Sc. Computer Science (AI) | Albert-Ludwigs-Universität Freiburg, Apr 2025 → present. Deep learning, probabilistic graphical models, statistical pattern recognition, robot mechanics. |
| B.E. Computer Science | N.M.A.M. Institute of Technology, 2020 → 2024. GPA 9.33/10 (German equivalent 1,3). |
| ML Intern | WiZdom Ed, Oct 2023 → Oct 2024. Production RAG over 5,000+ documents (LangChain + ChromaDB); ingestion −40% via recursive splitting; cosine-similarity feedback loop → 90% answer accuracy. |
| Certifications | [MLOps Specialization, Duke](https://coursera.org/verify/specialization/BC9VRBWCQRU5) · [ML Specialization, Stanford/DeepLearning.AI](https://coursera.org/verify/specialization/JDYYP28JPJNZ) |
| Languages | English C2 · Hindi native · German A2 → B1 |
| Base of operations | Freiburg im Breisgau, DE · CET |

</details>

<div align="center">

<a href="https://www.last.fm/user/KaranANchan22"><img src="https://lastfm-recently-played.vercel.app/api?user=KaranANchan22&count=3&width=500&header_style=compact&border_radius=12" alt="Recently played — live from Last.fm" /></a>

<sub><code>the training soundtrack · live</code></sub>

</div>

<!-- spotify direct widget (needs Premium) parked at karanchan02125.pythonanywhere.com — swap back anytime -->

<img src="assets/divider.svg" width="900" alt="" />

## <img src="assets/icon-pickaxe.svg" width="26" align="top" alt="" /> &nbsp;currently mining

<div align="center"><img src="assets/minecart.webp" width="720" alt="pixel minecart riding rails through a cave of glowing amethyst and diamond ore" /></div>

<img align="right" width="105" src="assets/chest-bleed.png" alt="open minecraft chest, light spilling out" />

*Two active repositories right now.*

🟢 &nbsp;**[mamba-hybrid-lm](https://github.com/Karan-Anchan/mamba-hybrid-lm)** · a ~50M Mamba-2 × attention hybrid LM comparing three attention:SSM ratios. **1:7 currently has the lowest validation perplexity in the reduced-scale run**

🔵 &nbsp;**[edge-yolo26-deployment](https://github.com/Karan-Anchan/edge-yolo26-deployment)** · **[live demo ▸](https://karan-anchan.github.io/edge-yolo26-deployment/)** · one detector across TensorRT, ONNX Runtime, and WebGPU. On the tested RTX 5070, **FP16 has the best latency per watt and FP8 is fastest**. Detection runs in the browser tab.

<details>
<summary>&nbsp;🔬 &nbsp;<b>run configs</b> · what is inside</summary>

<br/>

**mamba-hybrid-lm** · *in progress*
- Interleaves [Mamba-2](https://arxiv.org/abs/2405.21060) selective-SSM blocks with causal attention using the [Jamba](https://arxiv.org/abs/2403.19887) pattern · d_model 768 · bf16 · SwiGLU · RoPE · OpenWebText · one RTX 5070 12GB
- Compares **1:3 / 1:7 / 1:15** attention:SSM ratios at matched tokens-seen. In the reduced-scale preview, **1:7 has the lowest val PPL (102.4)** and 1:3 trains fastest.
- KV-cache use at 8K context, inference throughput, and the live token-streaming demo are still pending.

**edge-yolo26-deployment** · *shipped · [live WebGPU demo](https://karan-anchan.github.io/edge-yolo26-deployment/)*
- NMS-free YOLO26 fine-tune (SKU-110K dense shelves, mAP@50-95 **0.572**) shipped as **one ONNX graph → TensorRT** (RTX 5070), **ONNX Runtime** (Ryzen 7700) and **WebGPU** in-browser
- MLPerf-style p50/p95 latency + NVML power. **FP8 reaches 560 FPS**, **FP16 reaches 9.3 FPS/W with almost no accuracy loss**, and INT8 is slower and draws more power than both on this Blackwell GPU.
- The two INT8 paths differ by roughly 8× in accuracy loss (TensorRT −5.65% vs ONNX Runtime −0.72%). The CPU path uses per-channel quantization and keeps the detection head in FP32.
- Detection runs 100% client-side; the frame never leaves the browser

</details>

<img src="assets/divider.svg" width="900" alt="" />

## <img src="assets/icon-signal.svg" width="26" align="top" alt="" /> &nbsp;changelog

*Version history of the author. Semantic-ish.*

<table>
<tr>
<td rowspan="8" width="150" align="center" valign="middle"><img width="124" src="assets/villager-bleed.png" alt="pixel villager scientist holding a glowing beaker" /></td>
<th></th><th>release</th><th>notes</th>
</tr>
<tr><td><img src="assets/medal-rlpd.png" width="42" alt="" /></td><td><code>v2026.07</code></td><td><b>feat:</b> <a href="https://karan-anchan.github.io/rlpd/">reproduced RLPD and extended it to Humanoid</a> <em>(online-only beat the 50/50 mix)</em></td></tr>
<tr><td><img src="assets/medal-yolo.png" width="42" alt="" /></td><td><code>v2026.06</code></td><td><b>feat:</b> <a href="https://github.com/Karan-Anchan/edge-yolo26-deployment">one detector on GPU, CPU, and the browser</a> · FP8 at 560 FPS · live via WebGPU</td></tr>
<tr><td><img src="assets/medal-nmt.png" width="42" alt="" /></td><td><code>v2026.05</code></td><td><b>fix:</b> <a href="https://github.com/Karan-Anchan/en-hi-nmt-transformer">rebuilt and re-evaluated EN→HI translation</a> · frozen test set · beam search · chrF++ 41.6</td></tr>
<tr><td><img src="assets/medal-msc.png" width="42" alt="" /></td><td><code>v2025.04</code></td><td><b>major:</b> relocated to Freiburg — M.Sc. CS (AI), Albert-Ludwigs-Universität</td></tr>
<tr><td><img src="assets/medal-found.png" width="42" alt="" /></td><td><code>v2024.05</code></td><td><b>feat:</b> the foundations arc — <a href="https://github.com/Karan-Anchan/Windy_GridWorld_Sim">from-scratch RL</a> · <a href="https://github.com/Karan-Anchan/Unetr_3D_Abdomen_Segmentation">UNETR 3D segmentation</a></td></tr>
<tr><td><img src="assets/medal-rag.png" width="42" alt="" /></td><td><code>v2023.10</code></td><td><b>feat:</b> production RAG @ WiZdom Ed — 5k docs, 90% answer accuracy</td></tr>
<tr><td><img src="assets/medal-init.png" width="42" alt="" /></td><td><code>v2020.09</code></td><td><b>init:</b> B.E. Computer Science, first gradient descended</td></tr>
</table>

<img src="assets/divider.svg" width="900" alt="" />

## <img src="assets/icon-map.svg" width="26" align="top" alt="" /> &nbsp;quest log · 2026

*The current research queue. XP bars track progress.*

<div align="center"><img src="assets/quest-log.svg" width="900" alt="quest log 2026 — five research quests with xp progress bars: world-model RL 42%, GRPO/RLVR reasoning 33%, efficient-inference lab 17%, diffusion LM 8%, robotics VLA queued" /></div>

<details>
<summary>&nbsp;🔬 &nbsp;<b>quest briefings</b> · papers behind each bar</summary>

<br/>

| quest | the plan |
|---|---|
| World-model RL | DreamerV3 ([arXiv 2301.04104](https://arxiv.org/abs/2301.04104)) on Crafter at 1M steps; ablate imagination horizon (H = 5/15/30) and categorical vs Gaussian latents; render dream-vs-reality rollouts |
| GRPO / RLVR | verifiable-reward post-training on math ([DeepSeekMath, arXiv 2402.03300](https://arxiv.org/abs/2402.03300)); measure accuracy vs samples-at-inference |
| Efficient inference | GPTQ/AWQ × speculative decoding × KV-cache compression; a serving-throughput Pareto on one GPU |
| Diffusion LM | masked-diffusion ([arXiv 2406.07524](https://arxiv.org/abs/2406.07524)) vs a compute-matched autoregressive twin |
| Robotics VLA | SmolVLA/OpenVLA behaviour cloning on LIBERO; discrete-token vs flow-matching action heads |
| Agentic capstone | n8n supervisor + RAG + tool-use pipeline with pass^k reliability evals |

</details>

<img src="assets/divider.svg" width="900" alt="" />

## 🐍 &nbsp;the commit garden

*A snake is released into my contribution graph every night at 04:00. It has never once been full.*

<div align="center"><picture>
<source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Karan-Anchan/Karan-Anchan/output/snake.svg" />
<img src="https://raw.githubusercontent.com/Karan-Anchan/Karan-Anchan/output/snake-light.svg" width="880" alt="snake animation eating a year of commits" />
</picture></div>

<div align="center">

<img src="assets/divider.svg" width="900" alt="" />

<br/>

<img src="assets/stack.svg" width="900" alt="stack: python/pytorch core; transformers, mujoco, w&b research; onnx, tensorrt, webgpu systems; langchain, qdrant, n8n agents" />

<br/><br/>

<img src="assets/torch.svg" width="34" align="middle" alt="" />&nbsp;&nbsp;<img src="assets/achievement.svg" width="530" align="middle" alt="Achievement get! you read the whole profile." />&nbsp;&nbsp;<img src="assets/torch.svg" width="34" align="middle" alt="" />

<br/>

<sub><code>assembled in freiburg · fueled by chai</code></sub>

</div>
