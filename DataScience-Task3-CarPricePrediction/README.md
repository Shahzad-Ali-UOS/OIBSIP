# Task 3: Car Price Prediction with Machine Learning

## Project Overview
An end-to-end regression machine learning project to estimate the resale value of pre-owned vehicles. Using the CarDekho dataset, this project implements complete feature engineering, exploratory data analysis, categorical encoding, and comparative model benchmarking across linear and tree-based regression algorithms.

## 🎬 Walkthrough Video
[Watch Demo Video](DataScience-Task3-CarPricePrediction.mp4)

## Dataset Description
* **Source:** CarDekho Vehicle Dataset (Kaggle)
* **Raw Features:** `Car_Name`, `Year`, `Selling_Price` (Target), `Present_Price`, `Kms_Driven`, `Fuel_Type`, `Seller_Type`, `Transmission`, `Owner`
* **Engineered Features:** 
  * `Car_Age`: Computed from manufacturing year ($2026 - \text{Year}$) to represent temporal depreciation.
  * `Brand`: Extracted primary manufacturer from vehicle name.

## Workflow & Methodology
1. **Data Cleaning:** Handled missing values, deduplicated records, and standardized string encodings across categorical columns.
2. **Exploratory Data Analysis (EDA):**
   * Distribution of vehicle selling prices with Kernel Density Estimation (KDE).
   * Fuel type vs. price distribution comparisons via boxplots.
   * Depreciation curve analysis relating vehicle age to market value.
3. **Feature Preprocessing:** Applied One-Hot Encoding to categorical attributes (`Fuel_Type`, `Seller_Type`, `Transmission`), avoiding multicollinearity by dropping reference baselines.
4. **Model Training & Evaluation:**
   * Partitioned data into an 80/20 train-test split.
   * Evaluated three models: **Linear Regression**, **Random Forest Regressor**, and **Gradient Boosting Regressor**.
   * Evaluated metrics: Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and $R^2$ Score.
5. **Feature Importance:** Isolated dominant price determinants from the highest-performing ensemble model.

## Key Insights
* **Primary Valuation Drivers:** Present showroom price (`Present_Price`) and temporal age (`Car_Age`) account for the vast majority of price variance.
* **Algorithm Selection:** Non-linear ensemble methods (Random Forest / Gradient Boosting) substantially outperform classical Linear Regression by capturing non-linear depreciation dynamics.

## Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
* **Environment:** VS Code, Jupyter Notebook