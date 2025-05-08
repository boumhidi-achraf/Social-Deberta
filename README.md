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

### 🏗 Domain-Adaptive Pretraining Corpus (DAPT)
| Platform | Dataset | Entries | Tokens | Size |
|----------|---------|---------|--------|------|
| Twitter | Twitter Network Dataset | 100M | 1.5B | 25 GB |
|         | Sentiment140 | 1.6M | 24M | 0.4 GB |
|         | Twitter Sentiment | 163K | 2.4M | 0.04 GB |
|         | Tweets Sentiment | 27K | 405K | 0.01 GB |
| IMDb    | IMDb Review Dataset | 5.5M | 82.5M | 1.4 GB |
| Amazon  | Amazon Reviews | 34M | 510M | 8 GB |
|         | Amazon Book Reviews | 14M | 210M | 3 GB |
| Steam   | Steam Reviews | 21M | 315M | 5 GB |
| Google  | Google Local Reviews | 44M | 660M | 11 GB |

> 📌 **Total**: 220M entries / 3.3B tokens / ~53 GB

---

### 📊 Fine-Tuning & Evaluation Datasets

#### 1️⃣ Aspect-Based Sentiment Analysis (ABSA)
- **SemEval-2014 Task 4** – Laptops & Restaurants  
- **Custom-labeled reviews from X (Twitter)** – Annotated aspects across multiple domains

#### 2️⃣ Sentiment Regression
- 10,000 reviews annotated at **aspect-level** for continuous sentiment scores (0–10)
- Auto-labeled with SST-2 fine-tuned model, then refined by human annotators

#### 3️⃣ Sarcasm Detection
- **1,000 sarcastic reviews** manually labeled for cues:
  - Exaggeration, emojis, interjections, mismatched sentiment

#### 4️⃣ Deceptive Review Filtering
- Manually collected dataset labeled as legitimate vs deceptive
- Used for fine-tuning deception detection classifier

---

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
