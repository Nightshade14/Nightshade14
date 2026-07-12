<h1 align="center">Satyam Chatrola</h1>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&duration=3200&pause=900&color=2F81F7&center=true&vCenter=true&width=600&height=45&lines=Systems+engineer+%C3%97+AI+inference;Low-latency+serving+at+scale;I+make+things+fast%2C+and+prove+it" alt="Typing SVG" />
</div>

<p align="center">
  <b>AI Systems Engineer @ Mursion</b> &nbsp;•&nbsp; low-latency <i>AI inference & real-time serving</i> &nbsp;•&nbsp; NYU MS CS
</p>

<p align="center">
  <a href="https://nightshade14.github.io/satyamchatrola/">Portfolio</a> &nbsp;·&nbsp;
  <a href="https://www.linkedin.com/in/satyamchatrola">LinkedIn</a> &nbsp;·&nbsp;
  <a href="https://satyamchatrola.substack.com">Deep Dives (writing)</a>
</p>

---

```text
 ▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁▁
╔═══════════════════════════════════════════════════════════════╗
║ ▟▙  GEFORCE RTX 5090       axial-tech · vapor chamber  ▟▙     ║
║ ◎┌────────────────────────┐   ▲   ┌────────────────────────┐◎ ║
║  │      ░▒▓▓████▓▓▒░      │   ▲   │      ░▒▓▓████▓▓▒░      │  ║   Satyam Chatrola  —  AI Systems Engineer
║  │     ▄▀╲       ╱▀▄      │  ╱█╲  │     ▄▀╲       ╱▀▄      │  ║   ════════════════════════════════════════════════════════
║  │    ▟  ╲  ╲ ╱  ╱  ▙     │ ▐▓▓▓▌ │    ▟  ╲  ╲ ╱  ╱  ▙     │  ║    Focus     >  Low-latency AI inference & real-time serving
║  │    █   ╲ ╭─╮ ╱   █     │ ▐▓█▓▌ │    █   ╲ ╭─╮ ╱   █     │  ║    Loop      >  measure -> profile -> fix -> prove the delta
║  │   █ ──── ┤◉├ ──── █    │  █◈█  │   █ ──── ┤◉├ ──── █    │  ║    Prod win  >  p99 395ms -> 13ms  |  mean loop lag -71%
║  │    █   ╱ ╰─╯ ╲   █     │ ▐▓█▓▌ │    █   ╱ ╰─╯ ╲   █     │  ║    Deploy    >  14GB -> 355MB image  |  30min -> <7min ship
║  │    ▜  ╱  ╱ ╲  ╲  ▛     │ ▐▓▓▓▌ │    ▜  ╱  ╱ ╲  ╲  ▛     │  ║    Stack     >  Python(async) . C/Rust . Triton . vLLM . SGLang
║  │     ▀▄╱       ╲▄▀      │  ╲█╱  │     ▀▄╱       ╲▄▀      │  ║
║  │      ░▒▓▓████▓▓▒░      │   ▼   │      ░▒▓▓████▓▓▒░      │  ║    Serving systems  [██████████░░]  strong
║ ◎└────────────────────────┘   ▼   └────────────────────────┘◎ ║    LLM inference    [███████░░░░░]  building depth
║ ░▒▓  N V I D I A   GEFORCE  RTX 5090   ·   FOUNDERS EDITION   ║    GPU / CUDA read  [█████░░░░░░░]  learning
║ RGB  ▁▂▃▄▅▆▇█▇▆▅▄▃▂▁▂▃▄▅▆▇█▇▆▅▄▃▂▁▂▃▄▅▆▇█▇▆▅▄▃▂▁▂▃▄▅▆▇█▇▆▅▄▃▂▁║
╚═══════════════════════════════════════════════╤═════╤═════╤═══╝    Writing   >  satyamchatrola.substack.com
    [DP] [DP] [DP] [HDMI]   16-PIN 12VHPWR      ╿     ╿     ╿        Links     >  github.com/Nightshade14  |  in/satyamchatrola
   ▐▌ ▐▌ ▐▌ ▐▌ ▐▌ ▐▌ ▐▌ ▐▌ ▐▌ ▐▌ ▐▌ ▐▌ ▐▌ ▐▌ ▐▌  PCIe 5.0 x16
```

---

### What I do

I find where a system is spending its time and memory, then pull that number down and prove the fix with before-and-after measurements. My focus is **low-latency AI inference and real-time serving** — cutting p99 tail latency, engineering async concurrency and backpressure for throughput under load, and hardening distributed pipelines. I'm deepening into **LLM inference-serving**: throughput, KV-cache efficiency, and tail latency at scale.

The loop is the same everywhere I work: **measure the baseline → profile the bottleneck → apply the right lever → prove the delta.**

---

### Selected impact

**Mursion — AI Engineer (Systems, Real-Time)**

- **Cut p99 latency from 395 ms → 13 ms** (mean loop lag −71%) by offloading blocking Krisp C-extension calls off the asyncio event loop via `asyncio.to_thread`, preserving session ordering.
- **Sustained throughput under heavy concurrent load** — replaced blocking loggers with an async logging queue with high/low-watermark load-shedding and eventual-consistency backpressure, minimizing GIL contention.
- **Accelerated telemetry serialization 5×** with orjson and made requests traceable across systems — canonical IDs as Datadog facets (CPU, memory, GC pauses), propagated to Langfuse for AI-trace correlation.
- **Root-caused a production traffic-skew incident** (recognized by engineering leadership) by isolating silent random misrouting between two builds during a Jenkins → ArgoCD migration.
- **Shrank deploy footprint 14 GB → 355 MB and cut PR-to-prod 30 min → under 7 min** by re-architecting multi-stage Docker builds; hardened pipelines with circuit breakers, timeouts, and retries.

**RapidOps — Machine Learning Engineer**

- Engineered **Agentic AI workflows on self-hosted models (SGLang / vLLM)** with tracing and observability.
- Architected a **hybrid retrieval system** (Two-Tower NN via FAISS + BM25) scaling to **5M+ SKUs**; evolved ranking XGBoost → DeepFM for **0.87 NDCG@10** and a **7.2% conversion lift**.
- Owned **6 production pipelines**, engineering large-scale user–item interaction features — a cumulative **34% CTR lift** with **$300K+ ARR**.

---

### Going deep on

`LLM inference-serving` · `throughput` · `KV-cache efficiency` · `tail latency at scale` · `Triton` · `vLLM` · `SGLang` · `TensorRT` · `ONNX` · `OpenVINO`

I treat correctness as part of performance — an optimization that speeds up the math but quietly degrades outputs isn't a win. The credential I care about here is **verifiable public work**: benchmarks and writeups with real numbers. That's what I'm building toward.

---

### Featured project

**[Care Companion](https://github.com/care-ai-mlops/care-companion) — high-performance MLOps pipeline for real-time inference.** Containerized (Docker/K8s) production-grade CNN inference service at **P90 250 ms** using FastAPI and **NVIDIA Triton**, with GPU (TensorRT) and CPU (OpenVINO) ONNX backends. Full observability stack (Prometheus/Grafana) with custom metrics for real-time data-drift (KL divergence) and model-degradation detection.

---

### Writing & talks

- **Quoted by name in [Qualcomm's developer blog](https://www.qualcomm.com/developer/blog/2024/12/on-device-ai-builders-hackathon-qualcomm-lmstudio-microsoft)** on the power efficiency of on-device LLM inference (On-Device AI Builders Hackathon — Qualcomm × LM Studio × Microsoft, at NYU Tandon).
- [A Pragmatic Engineer's Guide to OOMs, NCCL, and Resilience in Large-Scale Training](https://satyamchatrola.substack.com/p/hyperscale-distributed-llm-training)
- [The Transformer Architecture: A First-Principles Analysis from Self-Attention to KV Caching](https://satyamchatrola.substack.com/p/from-tokens-to-text-deconstructing)

---

### Toolbox

<table>
<tr>
<td valign="top" width="33%">
<b>Inference &amp; serving</b><br>
NVIDIA Triton · vLLM · SGLang<br>
LlamaCpp · TensorRT · ONNX · OpenVINO<br>
<br>
<b>Systems &amp; real-time</b><br>
Python (async I/O, C/Rust bindings)<br>
Asyncio · gRPC · WebRTC · LiveKit
</td>
<td valign="top" width="33%">
<b>Infra &amp; MLOps</b><br>
Kubernetes (EKS) · Docker<br>
CI/CD (GitHub Actions, ArgoCD)<br>
CouchDB · PostgreSQL<br>
<br>
<b>Observability</b><br>
Datadog · Langfuse · Honeycomb<br>
Prometheus · Grafana
</td>
<td valign="top" width="33%">
<b>AI &amp; modeling</b><br>
PyTorch · Transformers · LLMs<br>
Hugging Face · TensorFlow<br>
MLflow · FAISS · Pinecone
</td>
</tr>
</table>

---

### Background

**RapidOps** — ML Engineer *(2020–2023)* → **NYU** — MS Computer Science *(2023–2025)* → **RapidOps** — ML Engineer *(2025–2026)* → **Mursion** — AI Engineer *(current)*

<sub>NYU MS Computer Science · Gujarat Technological University, BE Computer Engineering</sub>

---

<div align="center">
  <img src="https://streak-stats.demolab.com?user=Nightshade14&mode=weekly&theme=transparent&hide_border=true&ring=2F81F7&fire=E25A1A&currStreakLabel=2F81F7" height="150" alt="GitHub streak" />
</div>

<div align="center">
  <img src="https://raw.githubusercontent.com/Nightshade14/Nightshade14/output/snake.svg" alt="Snake animation" />
</div>
