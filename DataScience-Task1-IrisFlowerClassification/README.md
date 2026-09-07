# Task 1: Iris Flower Classification

## Overview
Machine learning classification model predicting Iris species (*Setosa*, *Versicolor*, *Virginica*) from physical flower measurements.

## 🎬 Video Walkthrough
🎥 [Watch the Video Demonstration on LinkedIn](https://lnkd.in/p/daegAMUX)

## Dataset
* **Source:** `sklearn.datasets.load_iris()`
* **Instances:** 150 (50 per class)
* **Features:** Sepal Length, Sepal Width, Petal Length, Petal Width

## Exploratory Data Analysis & Findings
* **Pairplot & Box Plots:** Petal length and petal width are the most discriminative features, providing clear linear separation for *Setosa* with zero overlap.
* **Correlations:** High correlation between petal measurements and species classification.

## Models Evaluated
* **Logistic Regression:** Stratified split, standardized features via `StandardScaler`.
* **Random Forest Classifier:** 100 decision trees.

## Results & Best Model
* **Logistic Regression:** ~96.7% - 100% test accuracy
* **Random Forest:** ~93.3% - 100% test accuracy
* **Declared Best Model:** **Logistic Regression** due to its minimal complexity, high interpretability, and low risk of overfitting on a small dataset.
