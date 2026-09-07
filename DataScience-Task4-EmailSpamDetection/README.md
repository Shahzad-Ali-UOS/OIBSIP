# Task 4: Email & SMS Spam Detection with Machine Learning

## Project Overview
An end-to-end Natural Language Processing (NLP) binary classification pipeline built to automatically detect and filter unsolicited spam messages from legitimate communications (ham). The workflow implements text normalization, tokenization, stemming, TF-IDF vectorization, model benchmarking, and error trade-off analysis.

## Dataset Description
* **Source:** SMS Spam Collection Dataset
* **Observations:** 5,169 unique messages (after removing duplicates)
* **Target Labels:** `ham` (legitimate communication) vs. `spam` (unsolicited advertisement/phishing)
* **Class Balance:** Approximately 87% Ham and 13% Spam, reflecting real-world class imbalance.

## Pipeline Architecture
1. **Text Preprocessing:**
   * Case folding (lowercasing).
   * Regex filtering to strip punctuation, numbers, and special characters.
   * Stopword elimination using NLTK English corpora.
   * Porter Stemming to reduce lexical variations to morphological roots.
2. **Feature Extraction:**
   * **TF-IDF Vectorization:** Evaluates term relevance by balancing local term frequency (TF) against corpus-wide inverse document frequency (IDF), capturing discriminative keywords (e.g., *claim*, *prize*, *urgent*).
   * Restricted vocabulary to top 3,000 informative n-gram features.
3. **Exploratory Data Analysis (EDA):**
   * Class frequency distributions.
   * Lexical frequency visualization through separate Ham and Spam **WordClouds**.
4. **Model Training & Benchmarking:**
   * Stratified 80/20 train-test split to preserve class ratios.
   * Benchmarked **Multinomial Naive Bayes (MNB)** against **Linear Support Vector Machine (Linear SVM)**.
   * Evaluated across Accuracy, Precision, Recall, and F1-Score.
5. **Trade-Off Analysis:**
   * Evaluated the operational cost of False Positives versus False Negatives. In spam filtering, **Precision is prioritized** to ensure legitimate user messages are never dropped or misdirected into junk folders.

## Model Performance Summary

| Model | Accuracy | Precision | Recall | F1-Score |
| :--- | :---: | :---: | :---: | :---: |
| **Linear SVM** | ~0.98+ | High (>0.95) | High (>0.85) | High (>0.90) |
| **Multinomial Naive Bayes** | ~0.97+ | Very High (~1.00) | Moderate (~0.80) | Strong (~0.88) |

## Tech Stack
* **Language:** Python
* **NLP & ML:** NLTK, Scikit-learn (`TfidfVectorizer`, `MultinomialNB`, `SVC`)
* **Data Processing & Visualization:** Pandas, NumPy, Matplotlib, Seaborn, WordCloud
* **Environment:** VS Code, Jupyter Notebook