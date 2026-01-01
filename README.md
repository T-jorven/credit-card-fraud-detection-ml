# Credit Card Fraud Detection using Machine Learning

## Project Overview

This project focuses on detecting fraudulent credit card transactions using machine learning techniques. The objective is to identify fraudulent activity in a highly imbalanced dataset while minimizing false positives and missed fraud cases. The project demonstrates an end-to-end workflow, from data exploration and preprocessing to model training, evaluation, and threshold tuning.

The dataset consists of synthetic credit card transaction records designed to reflect real-world fraud patterns while remaining privacy-safe.

---

## Dataset Description

- Total records: 10,000  
- Features: 10  
- Target variable: `is_fraud` (0 = legitimate, 1 = fraud)  
- Fraud rate: approximately 1.5 percent  
- Data type: synthetic  

### Features

| Feature | Description |
|------|------------|
| transaction_id | Unique transaction identifier |
| amount | Transaction amount |
| transaction_hour | Hour of transaction (0–23) |
| merchant_category | Merchant category |
| foreign_transaction | International transaction indicator |
| location_mismatch | Billing and transaction location mismatch |
| device_trust_score | Trust score of the device (0–100) |
| velocity_last_24h | Number of transactions in the last 24 hours |
| cardholder_age | Age of the cardholder |
| is_fraud | Target variable |

---

## Methodology

### Data Preparation
- Removed non-predictive identifiers (`transaction_id`)
- One-hot encoded categorical features
- Scaled numerical features where appropriate
- Used stratified train/test splitting to preserve class distribution

### Modeling
Two models were trained and evaluated:
- Logistic Regression with class weighting (baseline model)
- Random Forest (non-linear comparison model)

Logistic Regression was selected as the final model due to its interpretability and realistic performance behavior on imbalanced data.

---

## Evaluation Strategy

Due to severe class imbalance, model performance was evaluated using:
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion matrix

Accuracy alone was not used as a primary metric.

---

## Threshold Tuning

Instead of using the default classification threshold, decision thresholds were systematically evaluated to balance fraud recall and false positives. The final threshold was selected based on maximizing the F1-score while maintaining high fraud recall.

---

## Results Summary

- Logistic Regression achieved high recall while maintaining reasonable precision after threshold tuning
- Random Forest achieved near-perfect performance due to strong rule-based patterns in the synthetic dataset
- Feature importance analysis confirmed that behavioral and risk-based features drive fraud detection
- Logistic Regression was chosen as the final model for its robustness and interpretability

---

## Feature Importance Insights

The most influential features included:
- Transaction hour
- Device trust score
- Transaction velocity
- Location mismatch
- Foreign transaction indicator

These features align with known fraud detection risk patterns.

---

## Model Export and Reproducibility

Trained models are not stored in this repository. Models can be reproduced by running the provided notebooks or scripts. The Logistic Regression model was exported locally using `joblib` along with the selected decision threshold.

