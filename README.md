📊 Twitter & Reddit Sentiment Analysis Using PySpark
An End-to-End Pipeline for Social Media Text Classification

Author: Bob Philip
Institution: African Institute for Mathematical Sciences (AIMS–Rwanda)
Supervisor: Dr. Lema Logamou
Date: November 28, 2025

📌 Overview

This project builds a complete PySpark-based sentiment analysis pipeline for large social-media text datasets collected from Twitter and Reddit.
It classifies messages into:

Positive (1)

Neutral (0)

Negative (-1)

The final model achieves ~81% accuracy using Logistic Regression on TF-IDF features.

🎯 Project Goals

Process and analyze 230K+ text records from social platforms

Build a scalable text-cleaning and feature-engineering pipeline

Train ML models on TF-IDF features

Evaluate and compare classifiers

Visualize insights via word clouds and distribution plots

Deploy real-time sentiment classification using Tweepy

📁 Repository Structure
├── images/
│   ├── figure1.png
│   ├── figure2.png
│   ├── figure3.png
│   ├── ...
│
├── Sentimental_Analysis_Presentation.pdf
├── src/
│   ├── cleaning_pipeline.py
│   ├── train.py
│   ├── evaluate.py
│   ├── stream_twitter.py
│
├── requirements.txt
└── README.md

📝 Project Summary (Based on Presentation)
1️⃣ Introduction & Motivation

Millions of opinions are posted daily on Twitter and Reddit, making manual monitoring impossible.

Why sentiment analysis?

📈 Market Research: Understand public opinion

🏛 Political Analysis: Gauge support levels

🚨 Crisis Response: Detect negative trends early

2️⃣ Data Exploration & Preparation
Dataset Size

230,436 raw records

Removed 34,755 invalid entries

Final clean dataset: 195,323 rows

Label Distribution

Message Length Analysis

3️⃣ PySpark Cleaning Pipeline

Cleaning operations:

Lowercasing

Removing URLs, HTML tags, punctuation

Removing @mentions

Dropping null labels

Result: Clean, scalable dataset ready for NLP.

4️⃣ Feature Engineering (TF-IDF)

Steps:

Tokenization

StopWord removal

CountVectorizer → TF

IDF transformation

5️⃣ Text Visualization
Raw Word Cloud

Positive Word Cloud

Negative Word Cloud

6️⃣ Model Training & Evaluation
Trained Models

Logistic Regression

Naive Bayes

Random Forest

Performance (Test Set)
Model	Accuracy	F1 Score
Logistic Regression	0.8103	0.8101
Naive Bayes	0.7003	0.7032
Random Forest	0.4464	0.2758

📌 Logistic Regression performed best and is used in the deployed system.

7️⃣ Real-Time Twitter Streaming

Integrated with Tweepy to fetch live tweets and classify them automatically.

🔗 Live App Link

👉 https://00cc8358-d0e5-4992-b27d-90e2463817eb-00-1ggm5un9s27rk.worf.replit.dev/

🎯 Key Takeaways

Achieved 81% accuracy with Logistic Regression

PySpark enabled fast processing of large text datasets

Proper data cleaning & TF-IDF feature extraction is crucial

Word clouds validated the vocabulary associated with each sentiment

The pipeline supports real-time classification

🚀 Future Improvements

Hyperparameter tuning (cross-validation)

Integration of Word2Vec, GloVe, or BERT

More advanced deep learning approaches

Better deployment + dashboard
