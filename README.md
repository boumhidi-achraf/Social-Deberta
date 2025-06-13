# 🧠 Social-DeBERTa – Aspect-Based Reputation Generation for X Platform Reviews

## 📄 About This Repository

This repository contains the datasets, model training details, and evaluation resources used in the research paper:

> **Social-DeBERTa: Leveraging Domain-Adaptive Pretraining for Rapid Aspect-Based Reputation Generation Across X Platform Reviews**  
> _(submitted to Knowledge-Based Systems)_

Our system addresses the challenge of computing **fine-grained aspect-based reputation scores** from informal, sarcastic, and noisy social media (X platform) reviews using domain-adaptive pretrained models.

---

## 🔍 Core Features

- 🧾 Domain-adaptive transformer (Social-DeBERTa) trained on 220M+ social and review texts  
- 🧠 Fine-grained sentiment regression (0–10 scale) per aspect
- ⚠️ Deceptive review filtering based on linguistic patterns
- 🤖 Sarcasm detection pipeline using emoji mismatch, sentiment deviation, and human-mimicking logic    
- 📣 Influencer-aware score adjustment (based on likes/reposts)  
- 📊 Real-time interactive visualization with **SentiGaze**

---

## 📂 Datasets Used


## 🧪 Model Training

- **Base Model**: DeBERTa V3 Large (1.5B params)  
- **Pretraining Framework**: HuggingFace Transformers  
- **Training Infrastructure**: NVIDIA A100 (80GB), 32 vCPUs, 128GB RAM  
- **Objective**: Masked Language Modeling with span masking  
- **Hyperparams**: Batch=32, SeqLen=512, LR=3e-5, Optimizer=AdamW  
- **Pretraining Time**: ~110 hours

---

## 🌐 SentiGaze Dashboard (Visualization)
- 📍 **Website**: [www.sentigaze.com](http://www.sentigaze.com)  
- Provides:
  - Aspect-level and product-level reputation trends
  - Demographic heatmaps
  - Monthly sentiment evolution
  - Influencer-weighted insights

---

## 📜 Citation

If you use this repository, please cite:

```bibtex
@article{Benlahbib2025SocialDeberta,
  title     = {Social-DeBERTa: Leveraging Domain-Adaptive Pretraining for Rapid Aspect-Based Reputation Generation Across X Platform Reviews},
  author    = {Benlahbib, Abdessamad and Boumhidi, Achraf and Nfaoui, El Habib},
  journal   = {Preprint submitted to Nuclear Physics B},
  year      = {2025},
  note      = {May 6, 2025}
}
