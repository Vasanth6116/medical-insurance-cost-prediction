# Medical Insurance Cost Prediction

## Overview

This project predicts medical insurance charges using demographic and health-related information. The project follows a complete Machine Learning workflow from data preprocessing and exploratory data analysis to model building, evaluation, and statistical interpretation.

---

## Problem Statement

The objective is to predict insurance charges based on:

* Age
* Gender
* BMI
* Number of Children
* Smoking Status
* Region

using Linear Regression.

---

## Dataset Information

* Rows: 1337
* Features: 6
* Target Variable: charges

### Numerical Features

* age
* bmi
* children

### Categorical Features

* sex
* smoker
* region

---

## Exploratory Data Analysis

### Key Findings

* Insurance charges are right-skewed.
* Smoking status has the strongest relationship with insurance charges.
* Age and BMI show a positive relationship with charges.
* Number of children has a relatively small impact.
* No major multicollinearity was detected.

---

## Feature Engineering

### Label Encoding

Applied on:

* sex
* smoker

### One-Hot Encoding

Applied on:

* region

---

## Models Trained

### Model 1

Linear Regression (Without Scaling)

### Model 2

Linear Regression (With Standardization)

---

## Model Performance

### Without Scaling

* MAE: 4177.05
* RMSE: 5956.34
* R² Score: 0.807

### With Scaling

* Performance remained nearly identical.

---

## OLS Statistical Analysis

### Significant Features

* Age
* BMI
* Children
* Smoker
* Region Southeast
* Region Southwest

### Non-Significant Features

* Sex
* Region Northwest

Smoking status was identified as the most influential predictor of insurance charges.

---

## Project Structure

Medical-Insurance-Cost-Prediction/

├── data/

├── notebooks/

├── images/

├── models/

│ ├── linear_regression_model.pkl

│ ├── linear_regression_scaled.pkl

│ └── scaler.pkl

├── requirements.txt

├── README.md

└── .gitignore

---

## Conclusion

Linear Regression successfully captured the relationship between insurance charges and key factors such as smoking status, age, and BMI.

The model achieved strong predictive performance and explained over 80% of the variation in insurance charges.

Feature scaling produced minimal changes in performance, which is expected for Linear Regression, but was included to demonstrate a complete machine learning workflow and prepare the data for algorithms that are sensitive to feature scale.

This project serves as a strong baseline regression project and demonstrates the complete end-to-end process of building and evaluating a machine learning model.
