# Fraud-Detection
# 💳 Credit Card Fraud Detection Project

This project demonstrates a machine learning approach to proactively detect fraudulent credit card transactions using real-world anonymized data from Kaggle.

> **Dataset:** [Credit Card Fraud Detection (Kaggle)](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

---

## 🧾 Problem Statement

The goal is to build a binary classification model that can accurately identify fraudulent transactions from a large dataset of highly imbalanced financial data. The project includes:

- Data Cleaning & Preprocessing
- Exploratory Data Analysis (EDA)
- Feature Selection & Multicollinearity Removal
- Logistic Regression (Baseline)
- XGBoost Classifier (Robust Model)
- Model Evaluation (ROC-AUC, F1, Confusion Matrix)
- Business Insights & Recommendations

---

## 📁 Project Structure

```bash
fraud-detection/
│
├── creditcard.csv              # Dataset (add this manually)
├── FraudDetection.ipynb        # Final Jupyter Notebook
├── README.md                   # Project documentation
└── requirements.txt            # Python dependencies

##
🔍 Dataset Overview
Rows: 284,807

Features: 30 (anonymized PCA components V1-V28 + Amount + Time)

Target: Class (1 = Fraud, 0 = Legit)

✅ Steps Performed
1. Data Cleaning
Removed irrelevant columns like Time

Log-transformed Amount

Removed outliers using boxplots

Handled multicollinearity using VIF

2. Feature Selection
Used correlation heatmaps and feature importance from XGBoost

3. Model Building
Logistic Regression for baseline

XGBoost Classifier for advanced detection

Handled class imbalance using stratified train-test split

4. Evaluation Metrics
ROC-AUC Score

Precision / Recall / F1-Score

Confusion Matrix

Top Feature Importances

📊 Results
Model	ROC-AUC	F1-Score (Fraud Class)
Logistic Regression	~0.93	~0.72
XGBoost	~0.98	~0.90+

✅ XGBoost performed significantly better in detecting rare fraud cases.

📌 Key Insights
Features like V17, V14, V12 strongly indicate fraudulent behavior.

Fraudulent transactions typically have distinct patterns, even in anonymized data.

🛡️ Recommendations
Deploy real-time fraud detection scoring on payment gateways.

Implement alert systems for transactions with high anomaly scores.

Combine model prediction with IP/device fingerprinting for improved detection.

🚀 How to Run
Clone the repo
git clone https://github.com/akshat2004-hub/fraud-detection.git

Install dependencies
pip install -r requirements.txt

Run the notebook
Open FraudDetection.ipynb in Jupyter and execute cells step-by-step.

🧠 Technologies Used
Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)

XGBoost

Jupyter Notebook

SHAP (optional for advanced explainability)

👤 Author
Akshat Jain
B.Tech in Data Science 
