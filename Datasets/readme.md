# 📂 Datasets Used for Social-DeBERTa

This folder provides an overview of all datasets used for domain-adaptive pretraining (DAPT), fine-tuning, and evaluation in our paper:

> **Social-DeBERTa: Leveraging Domain-Adaptive Pretraining for Rapid Aspect-Based Reputation Generation Across X Platform Reviews**  
> Submitted to *Knowledge-Based Systems*, 2025.

---

## 🏗 1. Domain-Adaptive Pretraining Corpus (DAPT)

These datasets were used to adapt DeBERTa V3 to social media and review-style language. The corpus combines short-form (tweets) and long-form (user reviews) to reflect the stylistic and emotional variability of real-world reputation data.

| **Dataset**                         | **Platform**      | **Entries** | **Tokens** | **Size** | **Source** |
|------------------------------------|-------------------|-------------|------------|----------|------------|
| Twitter Network Dataset            | Twitter (Kaggle)  | 100M tweets | 1.5B       | 25 GB    | [Download](https://www.kaggle.com/datasets/adarshsng/covid19-twitter-dataset-of-100-million-tweets) |
| Sentiment140                       | Twitter (Kaggle)  | 1.6M tweets | 24M        | 239 MB   | [Download](https://www.kaggle.com/datasets/kazanova/sentiment140) |
| Twitter Sentiment Dataset          | Twitter (Kaggle)  | 163K tweets | 2.4M       | ~40 MB   | [Download](https://www.kaggle.com/datasets/cosmos98/twitter-and-reddit-sentimental-analysis-dataset) |
| Twitter Tweets Sentiment           | Twitter (Kaggle)  | 27K tweets  | 405K       | ~10 MB   | [Download](https://www.kaggle.com/datasets/yasserh/twitter-tweets-sentiment-dataset) |
| IMDb Review Dataset                | IMDb (Kaggle)     | 5.5M reviews| 82.5M      | ~1.4 GB  | [Download](https://www.kaggle.com/datasets/ebiswas/imdb-review-dataset) |
| Amazon Reviews                     | Amazon (Stanford) | 34M reviews | 510M       | 11 GB    | [Download](https://snap.stanford.edu/data/web-Amazon.html) |
| Amazon Book Reviews                | Amazon (Stanford) | 13M reviews | 210M       | 4.4 GB   | [Download](https://snap.stanford.edu/data/web-Amazon.html) |
| Steam Reviews                      | Steam (Kaggle)    | 21M reviews | 315M       | 8.2 GB   | [Download](https://www.kaggle.com/datasets/najzeko/steam-reviews-2021) |
| Google Local Reviews               | Google (Kaggle)   | 44M reviews | 660M       | 11 GB    | [Download](https://www.kaggle.com/datasets/mexwell/california-google-local-data) |

> 📦 **Total**: ~220M entries • 3.3B tokens • ~53 GB compressed

---

## 🧪 2. Fine-Tuning and Evaluation Datasets

Used for supervised fine-tuning and model evaluation across the four core tasks: ABSA, sentiment regression, sarcasm detection, and deceptive review filtering.

### 📌 Aspect-Based Sentiment Analysis (ABSA)
- **SemEval-2014 Task 4**  
  Standard ABSA benchmark (Laptops & Restaurants).  
  [Download](https://alt.qcri.org/semeval2014/task4/)

- **Custom-Labeled Twitter Dataset**  
  Manually annotated tweets across various domains to extract aspects relevant to reputation.

---

### 📌 Sentiment Regression Dataset
- **10,000 reviews** annotated at the **aspect-level** with a continuous sentiment score (0–10).
- Generated via:
  1. Auto-labeling with a Social-DeBERTa model fine-tuned on SST-2
  2. Manual refinement by human annotators for purchase intention and sentiment intensity

---

### 📌 Sarcasm Detection Dataset
- **1,000 sarcastic reviews** manually labeled with sarcasm indicators:
  - Exaggeration
  - Sentiment-emotion mismatch
  - Emojis and interjections (e.g., "LOL", "smh")
  - Conflicting sentiment cues

---

### 📌 Deceptive Review Filtering Dataset
- Manually collected and labeled dataset: `Legitimate (0)` vs `Deceptive (1)`
- Used to fine-tune the deception detection module integrated in the pipeline.

---

📣 If you're using any of these datasets, please refer to their individual licenses and cite their original sources where appropriate.
