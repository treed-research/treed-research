# 👋 Thomas Reed

*MSc Cyber Security | University of Kent*

---

<div align="center">

🎯 **Quantifying the Safety Tax** — measuring how fine-tuning LLMs on cybersecurity data degrades safety alignment across model architectures and training conditions.

</div>

---

## 📌 Project Status

<div align="center">

![Status](https://img.shields.io/badge/Stage%201-🔄%20In%20Progress-6d4aff)
![Stage 2](https://img.shields.io/badge/Stage%202-⏳%20Pending-lightgrey)
![Stage 3](https://img.shields.io/badge/Stage%203-⏳%20Pending-lightgrey)
![Thesis](https://img.shields.io/badge/Dissertation-Due%20Sep%204%2C%202026-red)

</div>

---

## 🔬 Research Design

| Component | Details |
|-----------|---------|
| 🤖 **Models** | 8 architectures (Mistral, Qwen, Llama, Gemma, Phi families) |
| 📊 **Conditions** | 4 training regimes (Alpaca control + 3 cybersecurity datasets) |
| ⚔️ **Evaluation** | HarmBench + Sorry-Bench standardised adversarial benchmarks |
| 🖥️ **Infrastructure** | 2× NVIDIA A100 80GB GPUs via Hydra HPC cluster (Slurm) |

---

## 🧪 Methodology

| Parameter | Value | Why |
|-----------|-------|-----|
| LoRA rank | r=16 | Standard per Hu et al. (2021) |
| Alpha | α=32 | 2× rank scaling convention |
| Quantization | 4-bit NF4 | Preserves weight distribution (Dettmers et al., 2023) |
| Epochs | 3 | Comparability with Qi et al. (2024) |
| Batch size | 32 | Fits 2× A100 80GB VRAM |
| Learning rate | 2e-4 | Standard for LoRA adaptation |
| Scheduler | Cosine | Smoother decay than linear |
| Optimiser | paged_adamw_8bit | Memory-efficient for QLoRA |

---

## 🛠️ Technology Stack

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)
![HuggingFace](https://img.shields.io/badge/🤗%20Transformers-FFD21E?logoColor=black)
![PEFT](https://img.shields.io/badge/PEFT-LoRA-8B5CF6)
![bitsandbytes](https://img.shields.io/badge/bitsandbytes-NF4-34D399)
![Weights & Biases](https://img.shields.io/badge/W&B-FFCC33?logo=weightsandbiases&logoColor=black)
![Slurm](https://img.shields.io/badge/Slurm-HPC-3B82F6)
![LaTeX](https://img.shields.io/badge/LaTeX-Overleaf-008080?logo=latex&logoColor=white)
![Git](https://img.shields.io/badge/Git-GitHub-F05032?logo=git&logoColor=white)

</div>

---

## 📂 Repositories

| Repository | Description | Status |
|------------|-------------|--------|
| [`safety-tax-dissertation`](https://github.com/treed-research/safety-tax-dissertation) | Training pipeline, evaluation scripts, configs | 🔒 Private (pending submission) |
| `treed-research` | This profile | ✅ Public |

*Public code release planned upon thesis completion.*

---

## 📄 Publications

- 📝 **In preparation:** "Quantifying the Safety Tax: Safety Alignment Degradation in Cybersecurity Fine-Tuned LLMs" — MSc Thesis, University of Kent
- 🎯 **Target venue:** EMNLP / NeurIPS 2026 LLM Safety Workshops

---

## 📊 Models Under Investigation

<div align="center">

| Model | Parameters | Family | Status |
|-------|-----------|--------|--------|
| Mistral-7B-Instruct-v0.3 | 7B | Mistral | 🔄 Training |
| Qwen2.5-7B-Instruct | 7B | Qwen | ⏳ Queued |
| Qwen3-8B | 8B | Qwen | ⏳ Queued |
| Gemma-2-9B-it | 9B | Google | ⏳ Queued |
| Phi-3-mini-4k | 3.8B | Microsoft | ⏳ Queued |
| Llama-3.1-8B-Instruct | 8B | Meta | ⏳ Queued |
| Llama-3-8B-Instruct | 8B | Meta | ⏳ Queued |
| Llama-2-7B-Chat | 7B | Meta | ⏳ Queued |

</div>

---

## 🔗 Connect

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-treed--research-181717?logo=github&logoColor=white)](https://github.com/treed-research)
[![University of Kent](https://img.shields.io/badge/University%20of%20Kent-MSc%20Cyber%20Security-8B0080)](https://www.kent.ac.uk)

</div>

---

<div align="center">

📊 All experiments tracked via [Weights & Biases](https://wandb.ai)
🔐 Intermediate checkpoints archived with MD5 verification for reproducibility
📚 Built on A* venue research: Vaswani et al. (2017), Hu et al. (2021), Dettmers et al. (2023), Qi et al. (2024)

</div>

---

*Last updated: August 2026*
