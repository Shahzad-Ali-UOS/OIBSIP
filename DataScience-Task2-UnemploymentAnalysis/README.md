# Task 2: Unemployment Analysis with Python (COVID-19 Impact)

## Overview
An exploratory data analysis (EDA) project analyzing temporal trajectories, regional disparities, and the economic shock delivered by the COVID-19 nationwide lockdowns on Indian unemployment metrics.

## 🎬 Walkthrough Video
[Watch Demo Video](DataScience-Task2-UnemploymentAnalysis.mp4)

## Dataset
* **File:** `Unemployment in India.csv`
* **Features:** State, Date, Frequency, Estimated Unemployment Rate (%), Estimated Employed, Estimated Labour Participation Rate (%), Area (Rural vs. Urban)
* **Pre-processing:** Stripped column whitespace, handled null rows, and parsed dates into datetime format.

## Key Analyses & Visualizations
* **Top 10 Impacted States:** Evaluated state-wise mean unemployment to isolate chronic high-unemployment zones (e.g., Haryana, Tripura, Jharkhand).
* **Area Analysis:** Box plot comparison showing greater volatility and higher baseline peaks in Urban centers versus Rural regions.
* **Time-Series Trajectory:** Multi-state trend tracking (Maharashtra, Delhi, Uttar Pradesh) demonstrating the steep March–May 2020 spike immediately post-lockdown.
* **Correlation Heatmap:** Evaluated the interaction between unemployment rate, raw employment counts, and labor participation.
* **Pre vs. Post COVID Impact:** Grouped analysis establishing the significant rise in mean unemployment and concurrent drop in labor participation after April 2020.

## Tech Stack
* Python
* Pandas & NumPy
* Matplotlib & Seaborn
* Jupyter Notebook