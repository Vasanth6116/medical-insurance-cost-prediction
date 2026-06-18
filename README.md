# Medical Insurance Cost Prediction using Regularized Regression Models

## Project Overview

This project predicts medical insurance charges using demographic and health-related information.

The objective is to compare the performance of multiple regression algorithms:

- Linear Regression
- Ridge Regression
- Lasso Regression
- ElasticNet Regression

The project follows a complete machine learning workflow including data cleaning, exploratory data analysis, feature engineering, model training, evaluation, and statistical interpretation.

---

## Problem Statement

Predict medical insurance charges based on:

- Age
- Gender
- BMI
- Number of Children
- Smoking Status
- Region

using various regression techniques.

---

## Dataset Information

Dataset: Medical Insurance Cost Prediction

Rows: 1337

Target Variable:

- charges

Features:

### Numerical Features

- age
- bmi
- children

### Categorical Features

- sex
- smoker
- region

---

## Data Preprocessing

### Data Cleaning

- Removed duplicate records
- Checked missing values
- Verified data types

### Feature Engineering

#### Label Encoding

Applied on:

- sex
- smoker

#### One-Hot Encoding

Applied on:

- region

Resulting Features:

- age
- sex
- bmi
- children
- smoker
- region_northwest
- region_southeast
- region_southwest

---

## Exploratory Data Analysis

### Key Findings

- Insurance charges are highly right-skewed.
- Smoking status has the strongest impact on insurance charges.
- Age shows a positive relationship with charges.
- BMI moderately affects insurance costs.
- Number of children has relatively low impact.
- No severe multicollinearity was detected.

---

## Outlier Analysis

IQR-based outlier detection was performed.

Findings:

- Age contained no significant outliers.
- BMI contained a few outliers.
- Charges contained several high-value observations.

These outliers were retained because they represent valid insurance records rather than data-entry errors.

---

## Models Implemented

### 1. Linear Regression

Baseline model for predicting insurance charges.

### 2. Ridge Regression

Uses L2 Regularization to reduce coefficient magnitudes and prevent overfitting.

### 3. Lasso Regression

Uses L1 Regularization and can perform feature selection.

### 4. ElasticNet Regression

Combines both L1 and L2 Regularization.

---

## Model Performance Comparison

| Model                 | MAE     | RMSE    | R² Score |
| --------------------- | ------- | ------- | -------- |
| Linear Regression     | 4177.05 | 5956.34 | 0.807    |
| Ridge Regression      | 4182.80 | 5796.98 | 0.784    |
| Lasso Regression      | 4181.51 | 5796.65 | 0.784    |
| ElasticNet Regression | 5271.30 | 7012.55 | 0.683    |

---

## OLS Statistical Analysis

OLS Regression was performed using Statsmodels.

### Significant Features

- Age
- BMI
- Children
- Smoker
- Region Southeast
- Region Southwest

### Non-Significant Features

- Sex
- Region Northwest

Smoking status was identified as the most influential predictor.

---

## Feature Importance Insights

Across all regression models:

### Most Important Features

1. Smoker
2. Age
3. BMI

### Less Important Features

- Children
- Region
- Sex

Smoking status consistently had the strongest effect on insurance charges.

---

## Key Learnings

This project helped understand:

- Linear Regression
- Multiple Linear Regression
- Feature Engineering
- Train-Test Split
- Model Evaluation Metrics
- MAE
- MSE
- RMSE
- R² Score
- Adjusted R²
- OLS Regression
- Ridge Regularization
- Lasso Regularization
- ElasticNet Regression
- Coefficient Interpretation
- Outlier Detection

---

## Project Structure

Medical-Insurance-Cost-Prediction/

├── data/

│ └── insurance.csv

├── notebooks/

│ ├── Medical_Insurance_Cost_Prediction.ipynb

│ ├── Ridge_Regression.ipynb

│ ├── Lasso_Regression.ipynb

│ └── ElasticNet_Regression.ipynb

├── models/

│ ├── linear_regression_model.pkl

│ ├── linear_regression_scaled.pkl

│ ├── ridge_regression_model.pkl

│ ├── lasso_regression_model.pkl

│ ├── elasticnet_regression_model.pkl

│ └── scaler.pkl

├── images/

├── README.md

├── requirements.txt

└── .gitignore

---

## Conclusion

Four regression algorithms were implemented and compared for predicting medical insurance charges.

Linear Regression achieved the best overall performance with an R² score of 0.807, indicating that it explained approximately 80.7% of the variation in insurance charges.

Ridge and Lasso Regression produced similar results, showing that regularization was not significantly required for this dataset.

ElasticNet Regression resulted in lower performance, suggesting that stronger regularization introduced underfitting.

Across all models, smoking status emerged as the most influential predictor, followed by age and BMI.

This project demonstrates a complete end-to-end machine learning workflow and provides a practical comparison of regularized regression techniques.
