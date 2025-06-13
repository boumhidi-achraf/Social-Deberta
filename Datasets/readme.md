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

These datasets are used for supervised fine-tuning and evaluation across the core tasks: Aspect-Based Sentiment Analysis (ABSA), sentiment regression, sarcasm detection, and deceptive review filtering.

### 📌 Aspect-Based Sentiment Analysis (ABSA)

* **SemEval-2014 Task 4**
  * **Description**: Standard benchmark for ABSA tasks (Laptops & Restaurants domains).
  * **Purpose**: Evaluation and benchmarking of aspect extraction performance.
  * [Download](https://alt.qcri.org/semeval2014/task4/)

* **Custom-Labeled Twitter Dataset**
  * **Description**: Manually annotated tweets capturing diverse product-related aspects, informal language, emojis, and slang across various domains.
  * **Purpose**: Fine-tuning the Social-DeBERTa model for accurate aspect extraction specific to informal social media contexts.

---

### 📌 Sentiment Regression Dataset

* **Social-DeBERTa-RG Dataset (10,000 reviews)**
  * **Description**: Reviews from diverse social media platforms annotated at the aspect-level with continuous sentiment scores ranging from 0–10.
  * **Annotation Process**:
    1. Automatic labeling using Social-DeBERTa fine-tuned on the SST-2 dataset.
    2. Manual refinement by human annotators focusing on purchase intention, sentiment intensity, and expression strength.
  * **Purpose**: Fine-tuning Social-DeBERTa-RG to predict nuanced, continuous reputation scores.

  **📥 Access the Dataset:**  
  To request access, please fill out the following form:  
  👉 [Access Request Form (Google Form)](https://docs.google.com/forms/d/e/1FAIpQLSeNj3r0inFKJiHLKd_GuljfAr8gl5Lf8O8MIY3-WiWirWC4Dg/viewform?usp=header)
---

### 📌 Sarcasm Detection Dataset

* **Custom-Labeled Sarcasm Dataset (1,000 sarcastic reviews)**
  * **Description**: Manually annotated reviews containing sarcasm indicators such as exaggeration, sentiment-emotion mismatches, emojis, interjections ("LOL", "smh"), and conflicting sentiment cues.
  * **Purpose**: Training and evaluating the sarcasm detection capabilities of Social-DeBERTa.

---

### 📌 Deceptive Review Filtering Dataset

* **Manually Collected Dataset**
  * **Description**: Reviews labeled as `Legitimate (0)` or `Deceptive (1)` to identify misleading or promotional content.
  * **Purpose**: Fine-tuning the deception detection module within the pipeline for effective spam and deceptive review filtering.

---

### 📌 Reputation Assessment Benchmark Datasets

* **Phone Product Dataset (3,000 reviews)**
  * **Description**: Expert-annotated Twitter reviews with reputation scores.
  * **Purpose**: Performance benchmarking for the reputation scoring system.

* **Web Application Dataset (2,500 reviews)**
  * **Description**: Expert-annotated Twitter reviews with reputation scores.
  * **Purpose**: Additional performance benchmarking and validation for reputation score predictions.

---

📣 If you're using any of these datasets, please refer to their individual licenses and cite their original sources where appropriate.

