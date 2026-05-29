# 📊 Twitter & Reddit Sentiment Analysis Using PySpark

### *An End-to-End Pipeline for Social Media Text Classification*

**Author:** Bob Philip\
**Institution:** African Institute for Mathematical Sciences
(AIMS--Rwanda)\
**Supervisor:** Dr. Lema Logamou\
**Date:** November 28, 2025

------------------------------------------------------------------------

## 📌 Overview

This project implements a full **PySpark sentiment analysis pipeline**
on a combined dataset from **Twitter** and **Reddit**, totaling over
**230K messages**.\
The classifier predicts:

-   **Positive (1)**
-   **Neutral (0)**
-   **Negative (-1)**

The final model achieved **≈ 81% accuracy** using Logistic Regression.

------------------------------------------------------------------------

## 📁 Repository Structure

```{=html}
<details>
```
```{=html}
<summary>
```
`<strong>`{=html}Click to expand`</strong>`{=html}
```{=html}
</summary>
```
    ├── images/
    │   ├── figure1.png
    │   ├── figure2.png
    │   ├── figure3.png
    │   ├── figure4.png
    │   ├── figure5.png
    │   ├── figure6.png
    │   ├── figure7.png
    │   ├── figure8.png
    │   ├── figure9.png
    │   ├── figure10.png
    │
    ├── Sentimental_Analysis_Presentation.pdf
    ├── src/
    │   ├── cleaning_pipeline.py
    │   ├── train.py
    │   ├── evaluate.py
    │   ├── twitter_stream.py
    │
    ├── requirements.txt
    └── README.md

```{=html}
</details>
```

------------------------------------------------------------------------

## 1️⃣ Introduction & Motivation

```{=html}
<details>
```
```{=html}
<summary>
```
`<strong>`{=html}Click to expand`</strong>`{=html}
```{=html}
</summary>
```
Social media platforms like **Twitter** and **Reddit** generate millions
of opinions every day.\
Analyzing this sentiment is helpful for:

-   Market research\
-   Political analytics\
-   Crisis management\
-   Trend detection

### 🎯 Target Classification

![Figure 1](images/figure1.png)

```{=html}
</details>
```

------------------------------------------------------------------------

## 2️⃣ Data Exploration & Preparation

```{=html}
<details>
```
```{=html}
<summary>
```
`<strong>`{=html}Click to expand`</strong>`{=html}
```{=html}
</summary>
```
### 📊 Dataset Summary

-   **230,436** raw messages collected\
-   **34,755** invalid/null labels removed\
-   **195,323** clean rows used for training

### 🔢 Label Distribution

![Figure 2](images/figure2.png)

### ✉️ Message Length Distribution

![Figure 3](images/figure3.png)

------------------------------------------------------------------------

### 🧹 PySpark Cleaning Pipeline

![Figure 4](images/figure4.png)

Pipeline steps:

-   Lowercasing\
-   Removing URLs\
-   Removing HTML tags\
-   Removing @mentions\
-   Removing punctuation\
-   Dropping null labels

### 📦 Final Dataset

![Figure 5](images/figure5.png)

```{=html}
</details>
```

------------------------------------------------------------------------

## 3️⃣ Feature Engineering

```{=html}
<details>
```
```{=html}
<summary>
```
`<strong>`{=html}Click to expand`</strong>`{=html}
```{=html}
</summary>
```
### 🔠 TF-IDF Pipeline

![Figure 7](images/figure7.png)

**Steps used:**

1.  Tokenization\
2.  Stopword removal\
3.  CountVectorizer\
4.  IDF weighting

------------------------------------------------------------------------

### ☁️ Word Clouds

#### Raw Word Cloud

![Figure 6](images/figure6.png)

#### Positive Messages

![Figure 8](images/figure8.png)

#### Negative Messages

![Figure 9](images/figure9.png)

```{=html}
</details>
```

------------------------------------------------------------------------

## 4️⃣ Model Training & Evaluation

```{=html}
<details>
```
```{=html}
<summary>
```
`<strong>`{=html}Click to expand`</strong>`{=html}
```{=html}
</summary>
```
### 🤖 Models Trained

-   Logistic Regression\
-   Naive Bayes\
-   Random Forest

### 📈 Performance Results

  Model                     Accuracy     F1 Score
  ------------------------- ------------ ------------
  **Logistic Regression**   **0.8103**   **0.8101**
  Naive Bayes               0.7003       0.7032
  Random Forest             0.4464       0.2758

**Best Model:** Logistic Regression

```{=html}
</details>
```

------------------------------------------------------------------------

## 5️⃣ Deployment: Real-Time Twitter Streaming

```{=html}
<details>
```
```{=html}
<summary>
```
`<strong>`{=html}Click to expand`</strong>`{=html}
```{=html}
</summary>
```
This project includes integration with **Tweepy** to classify tweets in
real time as they are streamed.

### 🔗 Live App

👉
[Tweetsence Live App/](https://tweetsense--bobphilip.replit.app)

### PySpark Features

![Figure 10](images/figure10.png)

```{=html}
</details>
```

------------------------------------------------------------------------

## 6️⃣ Key Takeaways

```{=html}
<details>
```
```{=html}
<summary>
```
`<strong>`{=html}Click to expand`</strong>`{=html}
```{=html}
</summary>
```
-   Achieved **81% accuracy** using Logistic Regression\
-   PySpark efficiently handled large datasets\
-   TF-IDF and strong cleaning improved performance\
-   Word clouds validated sentiment-based vocabulary\
-   The system supports **real-time predictions**

```{=html}
</details>
```

------------------------------------------------------------------------

## 7️⃣ Future Work

```{=html}
<details>
```
```{=html}
<summary>
```
`<strong>`{=html}Click to expand`</strong>`{=html}
```{=html}
</summary>
```
-   Hyperparameter tuning (GridSearchCV)\
-   Word2Vec / GloVe / BERT embeddings\
-   Deep learning models\
-   Real-time dashboard\
-   Multi-language sentiment support

```{=html}
</details>
```

------------------------------------------------------------------------

## 📜 License

This project is licensed under the **MIT License**.
