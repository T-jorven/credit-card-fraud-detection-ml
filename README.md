# credit-card-fraud-detection-ml

Dataset Description

**Credit Card Fraud Detection Dataset **
This dataset contains 10,000 credit card transactions designed to support research and experimentation in fraud detection using machine learning. The data realistically simulates both legitimate and fraudulent transactions, while maintaining a naturally imbalanced class distribution, which reflects real-world financial systems.

The dataset is suitable for binary classification tasks, where the objective is to predict whether a transaction is fraudulent (1) or legitimate (0) based on transaction behavior, risk indicators, and cardholder information.

🎯 Objective

To build and evaluate machine learning models that can identify fraudulent credit card transactions using transaction-level features such as amount, time, location mismatch, device trust, and transaction velocity.

📊 Dataset Characteristics

Total Records: 10,000
Total Features: 10
Target Variable: is_fraud
Class Distribution: Highly imbalanced (fraud ≈ 4–5%)
* Data Type: Synthetic (privacy-safe)

🧾 Feature Description

Feature Name	Description
transaction_id	Unique identifier for each transaction
amount	Transaction amount
transaction_hour	Hour of transaction (0–23)
merchant_category	Type of merchant
foreign_transaction	Indicates if transaction is international (0/1)
location_mismatch	Billing vs transaction location mismatch (0/1)
device_trust_score	Trust score of the device (0–100)
velocity_last_24h	Number of transactions in last 24 hours
cardholder_age	Age of the cardholder
| is_fraud | Target variable (0 = Normal, 1 = Fraud) |

🔍 Potential Use Cases

Credit card fraud detection systems
Imbalanced classification problems
Feature engineering and risk analysis
Model comparison (Logistic Regression, Random Forest, XGBoost, etc.)
* Anomaly detection research

📈 Recommended Evaluation Metrics

Due to class imbalance, the following metrics are recommended:

Precision
Recall
F1-score
ROC-AUC
* Confusion Matrix

⚠️ Notes

This dataset is synthetically generated and does not contain any real customer data.
* It is intended for educational, research, and practice purposes only.
