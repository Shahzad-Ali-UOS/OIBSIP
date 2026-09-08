# Task 5: Sales Prediction Using Machine Learning

## Project Overview
An end-to-end regression modeling pipeline built to forecast product unit sales based on advertising investments across TV, Radio, and Newspaper channels. The project implements exploratory data analysis, pairwise regression inspections, correlation heatmaps, baseline linear modeling, non-linear ensemble benchmarking, residual error diagnostics, and marketing channel attribution.

## Dataset Details
* **Source:** Advertising Budget Dataset
* **Observations:** 200 market campaigns
* **Features:**
  * `TV`: Budget allocated to TV commercials ($ in thousands)
  * `Radio`: Budget allocated to Radio broadcast spots ($ in thousands)
  * `Newspaper`: Budget allocated to Newspaper advertisements ($ in thousands)
* **Target:** `Sales`: Product units sold (in thousands)

## Pipeline Architecture
1. **Data Sanitization & Preprocessing:** Header whitespace trimming, casing standardization, index column cleanup, and null checks.
2. **EDA & Channel Visualizations:** Pairplots, individual media regression lines, and correlation matrix heatmap.
3. **Model Benchmarking:** 80/20 train/test split benchmarking **Multiple Linear Regression (Baseline)** against **Random Forest Regressor**.
4. **Residual Diagnostics:** Scatter and distribution analysis confirming homoscedasticity and zero-mean unbiased error distribution.
5. **Attribution Analysis:** Coefficient and feature importance analysis isolating TV and Radio as high-value drivers and Newspaper as low-ROI capital.

## Model Benchmarking Results

| Model | MAE | RMSE | R² Score |
| :--- | :---: | :---: | :---: |
| **Random Forest Regressor** | **~0.62** | **~0.85** | **~0.98** |
| **Linear Regression (Baseline)** | ~1.46 | ~1.78 | ~0.90 |

## Strategic Attribution Conclusions
* **TV:** Dominates total variance explained ($\approx 60\%+$ importance) and serves as the primary driver of baseline sales volume.
* **Radio:** Offers the highest per-dollar marginal coefficient ($\approx 0.188$), functioning as an effective complementary channel.
* **Newspaper:** Produces a near-zero coefficient and negligible importance, indicating print ad spend should be rechanneled to digital/broadcast formats.

## 🎬 Video Demonstration
🎥 [Watch the Video Demonstration on LinkedIn](https://lnkd.in/p/dabuSj9n)

## Tech Stack
* **Language:** Python
* **Machine Learning:** Scikit-learn (`LinearRegression`, `RandomForestRegressor`, metrics)
* **Data Processing & Visualization:** Pandas, NumPy, Matplotlib, Seaborn
* **Environment:** VS Code, Jupyter Notebook
