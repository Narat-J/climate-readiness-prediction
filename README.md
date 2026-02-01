# Using Machine Learning to Predict Countries' Climate Readiness

**Author:** Narat Jaitui  
**Status:** Final Project (Course: Intro to ML for Economists, Degree: Applied Economics and Markets, University of Bologna)

## Overview
Assessing a country's readiness to climate change typically requires complex indices like the ND-GAIN Country Index, which relies on 45 indicators from 74 data sources. Many of these datasets suffer from reporting lags or limited coverage.

This project investigates whether ML can accurately classify national climate readiness using a set of just 12 publicly available macro-indicators from the World Bank.

## Key Results
By training on 3,912 country-year observations (182 countries, 2000–2023), the analysis found that a "lean" model can replicate complex index classifications with high accuracy.

| Metric | Result |
| :--- | :--- |
| **Best Model** | **XGBoost** (outperforming LogReg, SVM, and Random Forest) |
| **Accuracy (F1)** | **93.3%** (Macro-averaged F1-score) |
| **Efficiency** | Reduced input features from **45 $\to$ 12** indicators |
| **Robustness** | **86.2% F1-score** in temporal validation (Training: 2000–18, Testing: 2019–23) |

## Methodology & Data
* **Data Source:** World Bank Open Data & Notre Dame Global Adaptation Initiative (ND-GAIN).
* **Target Variable:** ND-GAIN Readiness classifications.
* **Models Evaluated:** Logistic Regression, Random Forests, Support Vector Machines (SVM), XGBoost.
* **Validation:** Temporal split (predicting future performance) to avoid look-ahead bias.

## Project Files
* `Climate_Readiness_Paper.pdf`: The full academic report.
* `CR_analysis_notebook.ipynb`: Python code of the project.

## Disclaimer
*This paper was submitted as a final project for the course "Introduction to Machine Learning for Economists" at the University of Bologna (Fall 2025). It is intended for portfolio demonstration and has not been peer-reviewed.*
