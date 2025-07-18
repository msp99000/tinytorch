# 🧠 TinyTorch: Lightweight LLM Optimization Pipeline

**TinyTorch** is a proof-of-concept (PoC) pipeline that implements advanced compression techniques for large language models (LLMs), enabling their efficient deployment on constrained environments — including edge devices like Jetson Nano.

> 🔬 *Built with pruning, knowledge distillation, and QLoRA quantization techniques.*

---

## 🚀 Objectives

The goal of this project is to demonstrate:
- ✅ Structural model pruning for reducing parameter count
- ✅ Knowledge distillation to transfer knowledge from large models to compact ones
- ✅ QLoRA quantization for low-bit precision inference (e.g., 4-bit)
- ✅ Potential deployment on low-resource or edge environments (Jetson, Raspberry Pi, etc.)

---

## 📌 Technologies Used

| Component         | Tool/Library                  |
|------------------|-------------------------------|
| 🧠 Base Models    | Hugging Face Transformers     |
| 🧪 Distillation   | PyTorch + Hugging Face Trainer|
| ✂️ Pruning        | `torch.nn.utils.prune`        |
| 🧮 Quantization   | `bitsandbytes`, `AutoGPTQ`, `QLoRA` |
| 📊 Tracking       | Weights & Biases (optional)   |
| 🔍 Datasets       | SST-2, IMDb, AG News          |
| 🖥️ Infra          | Google Colab / Kaggle GPUs    |

---

## 📈 Pipeline Overview

```text
[ Base Model ] ──▶ [ Pruning ] ──▶ [ Distillation ] ──▶ [ QLoRA (4-bit) ] ──▶ [ Inference on Edge ]
       │                                          │
       │                                          └─────▶ Student Model (compressed)
       └────────────────────────────────────────────────▶ Evaluation & Comparison
