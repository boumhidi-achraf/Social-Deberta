# 🧠 Social-DeBERTa: Aspect-Based Reputation Generation for Social Media Reviews

## 📑 About This Repository

Welcome to the official repository for the paper:  
> **Social-DeBERTa: Leveraging Domain-Adaptive Pretraining for Rapid Aspect-Based Reputation Generation Across X Platform Reviews**  
> _(Preprint submitted to Knowledge-Based Systems, 2025)_

This work introduces **Social-DeBERTa**, a domain-adaptive reputation generation framework specifically designed for the complexities of informal social media platforms like X (formerly Twitter). Our system tackles the challenges of sarcasm, influencer bias, and deceptive reviews to deliver fine-grained, aspect-based reputation scores on a continuous **0–10 scale**.

---

## 🚀 Key Contributions

- **🧠 Social-DeBERTa Transformer**: Domain-adaptive model trained on 220M+ social media and review texts.
- **🔍 Fine-Grained Sentiment Regression**: Predicts continuous sentiment scores for each aspect.
- **🎭 Sarcasm Detection Pipeline**: Uses emoji-sentiment mismatches, sentiment deviation, and human-like logic.
- **⚠️ Deceptive Review Filtering**: Removes misleading or promotional content.
- **📣 Influencer-Aware Adjustments**: Weighs reputation scores based on social engagement (likes, reposts).
- **📊 SentiGaze Dashboard**: Real-time visualization of reputation trends, demographic breakdowns, and influencer effects.

---

## 📂 Dataset Access

All datasets used in this work are available in the following folder of this repository:

🔗 [📁 Datasets Folder](https://github.com/boumhidi-achraf/Social-Deberta/tree/main/Datasets)

The datasets include:
- Domain-adaptive pretraining corpora
- Annotated sentiment regression datasets
- Aspect extraction and sarcasm detection training sets
- Benchmark evaluation data for reputation scoring

---

## ⚙️ Model Training Configuration

- **Base Model**: DeBERTa V3 Large (1.5B parameters)
- **Pretraining Strategy**: Domain-Adaptive Pretraining (DAPT) on noisy social media texts
- **Frameworks Used**: HuggingFace Transformers, PyTorch
- **Compute Infrastructure**: NVIDIA A100 (80GB), 32 vCPUs, 128GB RAM
- **Key Hyperparameters**:  
  - Batch Size: 32  
  - Sequence Length: 512  
  - Learning Rate: 3e-5 (AdamW optimizer)  
  - Pretraining Time: ~110 hours

---

## 🌐 Live Visualization: SentiGaze

Explore reputation scores in real time with our interactive dashboard:

🔗 [🌟 SentiGaze Dashboard](http://www.sentigaze.com)

SentiGaze offers:
- Aspect-level sentiment and reputation trends
- Demographic heatmaps of sentiment shifts
- Monthly evolution of product and service reputations
- Influencer-weighted analysis of public sentiment

---

## 🔬 Experimental Results

Our system achieves:
- **Up to 75% error reduction** compared to six SOTA reputation systems
- **Mean Absolute Error (MAE)** as low as **0.08** on benchmark Twitter datasets
- **Processing Speed**: ~3,000 reviews analyzed in under **93 seconds**

---

## 📜 Citation

If you use this repository or its datasets in your work, please cite:

```bibtex
@article{Benlahbib2025SocialDeberta,
  title     = {Social-DeBERTa: Leveraging Domain-Adaptive Pretraining for Rapid Aspect-Based Reputation Generation Across X Platform Reviews},
  author    = {Benlahbib, Abdessamad and Boumhidi, Achraf and Nfaoui, El Habib},
  journal   = {Preprint submitted to Knowledge-Based Systems},
  year      = {2025},
  note      = {May 6, 2025}
}
