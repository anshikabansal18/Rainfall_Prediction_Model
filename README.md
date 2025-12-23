# 🌧️ Rainfall Prediction with Reliability & Uncertainty Analysis
## 📌 Overview

Rainfall prediction is an inherently uncertain problem with significant societal and economic implications. This project focuses on predicting whether it will rain the next day using meteorological observations, while placing strong emphasis on statistical rigor, reliability, and uncertainty-aware evaluation, rather than accuracy alone.

The work combines classical statistical preprocessing, machine learning models, and advanced evaluation techniques to study not only how well models perform, but also how stable and reliable their predictions are.

## 🎯 Objectives

- Predict next-day rainfall occurrence using weather data

- Address real-world challenges such as class imbalance and missing values

- Evaluate models using reliability-focused metrics

- Quantify uncertainty and stability in model performance

- Analyze probabilistic outputs, not just hard classifications

## 🧹 Data Preprocessing

The following statistically grounded preprocessing steps were applied:

- Class imbalance handling using oversampling

- Categorical encoding via label encoding

- Advanced multivariate imputation using MICE (Iterative Imputer)

- Outlier detection and removal using Interquartile Range (IQR)

- Correlation analysis to examine multicollinearity

These steps ensure that statistical relationships in the data are preserved while reducing noise and bias.

## 🔍 Feature Selection

- Feature importance was examined using:

- Filter methods (Chi-square test)

- Wrapper methods (Random Forest–based selection)

Key predictors included:

- Sunshine

- Humidity (morning and afternoon)

- Pressure (morning and afternoon)

- Cloud cover

- Recent rainfall indicators

## 🤖 Models Implemented

The following models were trained and evaluated:

- Logistic Regression

- Decision Tree

- Random Forest

- Neural Network (MLP)

- LightGBM

- CatBoost

- XGBoost

Models were compared not only on performance, but also on computational efficiency and reliability.

## 📈 Evaluation Metrics

- ROC–AUC – discrimination ability

- Cohen’s Kappa – agreement beyond chance

- Precision / Recall – for imbalanced decision contexts

- Execution Time – practical efficiency

## 🔁 Reliability & Stability Analysis

### Train–Test Stability

- Model performance evaluated across multiple random splits

- Mean Cohen’s Kappa ≈ 0.87

Standard deviation ≈ 0.003, indicating highly stable behavior

### Probability Threshold Sensitivity

- Examined how varying decision thresholds affect reliability

- Highlighted trade-offs between confidence and agreement

### Probability Calibration

- Calibration curves used to compare predicted probabilities with observed frequencies

- Identified regions of good calibration and areas of overconfidence

### Bootstrap Confidence Intervals

- Bootstrap resampling used to quantify uncertainty in accuracy

- 95% confidence interval ≈ 0.61–0.62, demonstrating statistically stable performance

## 🧠 Key Insights

- Ensemble models (Random Forest, XGBoost, CatBoost) achieved strong discriminative performance

- Reliability metrics revealed that high accuracy alone can be misleading

- Probability calibration and uncertainty analysis are essential for real-world decision-making

- Rainfall prediction models are sensitive to threshold selection and data imbalance
