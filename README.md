# 🚀 LLM Performance Optimization & Benchmarking

Ushbu loyiha turli darajadagi Large Language Models (LLM) larning samaradorligini taqqoslash va ularni **Quantization** (kvantlash) orqali optimallashtirishga bag'ishlangan.

## 🎯 Maqsad
- Turli LLM modellarning (TinyLlama, Phi-2) ishlash tezligini solishtirish.
- FP32, INT8 va INT4 kvantlash turlarining **Inference Speed** (tokens/sec) ga ta'sirini tahlil qilish.
- Past xotirali (VRAM) qurilmalarda katta modellarni ishlatish imkoniyatlarini o'rganish.

## 🧱 Ishlatilgan Modellar
1. **TinyLlama-1.1B** - Kichik va tezkor model.
2. **Microsoft Phi-2 (2.7B)** - Yuqori sifatli va ixcham model.

## 🛠 Texnologiyalar
- **Framework:** PyTorch 🔥
- **Library:** HuggingFace Transformers, Bitsandbytes, Accelerate.
- **Hardware:** NVIDIA GPU (CUDA).

## 📊 Natijalar (Benchmark Results)

O'tkazilgan testlar natijasida quyidagi ko'rsatkichlar qayd etildi:

| Model | Precision | Avg Time (s) | Speed (tokens/sec) |
| :--- | :--- | :--- | :--- |
| **TinyLlama** | FP32 | 1.13s | 15.74 |
| **TinyLlama** | INT8 | 1.89s | 9.79 |
| **TinyLlama** | **INT4** | **1.34s** | **26.11** 🚀 |
| **Phi-2** | FP32 | 4.59s | 17.69 |
| **Phi-2** | INT8 | 11.49s | 7.38 |
| **Phi-2** | **INT4** | **5.24s** | **20.13** |

### 📈 Asosiy xulosalar:
- **INT4 g'alabasi:** Kvantlash nafaqat xotirani tejaydi, balki `TinyLlama` misolida tezlikni deyarli **65% ga oshirdi**.
- **INT8 paradoksi:** 8-bitli kvantlashda de-quantization jarayoni tufayli tezlik FP32 dan biroz pastroq bo'lishi kuzatildi.
- **Optimal balans:** `Phi-2` modeli INT4 rejimida ham sifat, ham tezlik bo'yicha eng yaxshi balansni ko'rsatdi.
