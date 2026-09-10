👋 Thomas Reed
MSc Cyber Security | University of Kent

🎯 **Quantifying the Safety Tax** — measuring how fine-tuning open-weight
LLMs on benign instruction data (general-purpose and cybersecurity-domain)
changes safety alignment, evaluated with HarmBench and exact McNemar tests.

📌 Project Status: **analysis and write-up complete** (September 2026)

## 🔬 Research Design

| Component | Details |
|---|---|
| 🤖 Models | 8 open-weight instruction-tuned families (Mistral, Qwen, Llama, Gemma, Phi), 3.8–9B parameters |
| 📊 Conditions | 4 benign training datasets (Alpaca + 3 cybersecurity corpora), 32 fine-tuned conditions + 8 baselines |
| ⚔️ Evaluation | HarmBench standard behaviours (320 per condition), official Llama-2-13B classifier, exact McNemar tests |
| 🖥️ Infrastructure | University of Kent Hydra HPC (NVIDIA A100-class GPUs, 1–2 per job via Slurm) |

## 🧪 Methodology

| Parameter | Value | Why |
|---|---|---|
| LoRA rank | r=16 | Standard (Hu et al., 2021) |
| Alpha | α=32 | 2× rank scaling convention |
| Quantization | 4-bit NF4 | QLoRA (Dettmers et al., 2023) |
| Epochs | 3 | Held constant across all datasets |
| Batch size | 32 | Fixed effective batch across grid |
| Learning rate | 2e-4 | Standard for LoRA adaptation |
| Scheduler | Cosine | Smoother decay than linear |
| Optimiser | paged_adamw_8bit | Memory-efficient for QLoRA |

## 🛠️ Technology Stack
Python · PyTorch · HuggingFace · PEFT · bitsandbytes · Weights & Biases · Slurm · LaTeX

## 📂 Repositories
| Repository | Description | Status |
|---|---|---|
| safety-tax-dissertation | Training, evaluation and analysis pipeline | 🔒 Private |

Code release pending confirmation of the University's pre-submission
publication policy.

## 📊 Models (all experiments complete)
Mistral-7B-Instruct-v0.3 · Qwen2.5-7B-Instruct · Qwen3-8B · Gemma-2-9B-it ·
Phi-3-mini-4k-instruct · Llama-3.1-8B-Instruct · Llama-3-8B-Instruct ·
Llama-2-7B-Chat

## 📝 Findings (summary)
Fine-tuning on benign data degraded safety for a minority of conditions,
concentrated on models with fragile initial safety alignment fine-tuned
on generic instruction data; defensive cybersecurity corpora instead
*reduced* attack success, consistent with refusal transfer from their
defensive persona. Details in the dissertation.

Last updated: September 2026