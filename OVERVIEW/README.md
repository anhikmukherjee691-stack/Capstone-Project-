# ANOVYX AI
### AI-Driven Intelligent Fraud & Anomaly Detection System

**Tagline:** Detect the unusual. Prevent the unthinkable.

## 1. Project Overview

ANOVYX AI is a machine learning-based financial fraud detection system designed to identify suspicious transactions and unusual financial activities.

The project aims to address the limitations of conventional fraud detection systems, particularly their dependence on fixed rules, difficulty detecting unusual transaction patterns, and challenges associated with highly imbalanced financial datasets.

The proposed system combines supervised machine learning with anomaly detection to improve fraud identification and reduce unnecessary false alerts.

## 2. Problem Statement

Digital financial transactions are increasing rapidly, creating opportunities for fraudulent activities. Traditional rule-based systems may fail to identify new and evolving fraud patterns.

Machine learning models can improve fraud detection, but financial datasets often contain a very small proportion of fraudulent transactions. This class imbalance can cause a model to classify most transactions correctly while failing to identify actual fraud.

ANOVYX AI aims to develop a system that evaluates transaction characteristics, identifies suspicious patterns, and provides a fraud risk assessment.

## 3. Project Objectives

- Develop a machine learning-based financial fraud detection system.
- Study and compare supervised and unsupervised learning algorithms.
- Investigate the effect of class imbalance on fraud detection.
- Explore a hybrid Random Forest and Isolation Forest approach.
- Evaluate performance using appropriate classification metrics.
- Develop a Streamlit-based interface for transaction risk analysis.

## 4. Proposed Methodology

The proposed workflow consists of:

1. Dataset collection.
2. Data cleaning and preprocessing.
3. Exploratory data analysis.
4. Feature engineering.
5. Training a supervised Random Forest baseline.
6. Training an Isolation Forest anomaly detector.
7. Combining model outputs in a hybrid approach.
8. Decision-threshold selection using validation data.
9. Evaluation on unseen test data.
10. Integration with the ANOVYX AI dashboard.

## 5. Dataset

The project plans to use the PaySim mobile money transaction dataset.

PaySim contains simulated financial transactions with legitimate and fraudulent transaction labels. It provides transaction attributes such as transaction type, amount, account balances, and fraud labels.

Dataset source:
https://www.kaggle.com/datasets/ealaxi/paysim1

The dataset will be examined for class imbalance, missing values, duplicate records, feature relevance, and possible data leakage before model training.

## 6. Algorithms

### Random Forest
A supervised ensemble learning algorithm that combines multiple decision trees to classify transactions as legitimate or fraudulent.

### Isolation Forest
An unsupervised anomaly detection algorithm that identifies unusual observations by isolating them through random feature and split selection.

### Proposed Hybrid Approach
The proposed approach investigates combining Random Forest fraud probabilities with Isolation Forest anomaly scores.

The purpose is to evaluate whether supervised classification and anomaly detection provide complementary information for identifying suspicious financial transactions.

## 7. Model Evaluation

The system will be evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Precision-Recall AUC (PR-AUC)
- ROC-AUC
- Confusion Matrix
- False Positive Rate

Because fraudulent transactions are relatively rare, accuracy alone will not be treated as sufficient evidence of model performance.

## 8. Current Development Status

### Phase 1 – Baseline Prototype
- Streamlit dashboard developed.
- Synthetic transaction generation implemented.
- Random Forest baseline implemented.
- Initial model evaluation and confusion matrix generated.
- Transaction risk prediction interface developed.

### Phase 2 – Dataset and Hybrid Model Improvement
- Integrate a suitable financial fraud benchmark dataset.
- Train and evaluate the Isolation Forest model.
- Investigate the hybrid Random Forest and Isolation Forest approach.
- Tune model parameters and decision thresholds.
- Compare baseline and hybrid performance.

### Phase 3 – Future Development
- Explainable AI using SHAP.
- Real-time transaction monitoring.
- Alert logging and investigation workflow.
- Data drift monitoring.
- Scalable deployment.

## 9. Research Gap

Existing fraud detection approaches face challenges involving severe class imbalance, evolving fraud patterns, false-positive alerts, and limited interpretability.

This project investigates whether combining supervised classification with unsupervised anomaly detection can improve the identification of suspicious transactions while maintaining an acceptable false-positive rate.

The effectiveness of this approach will be established through comparative experiments rather than assumed in advance.

## 10. Technology Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Streamlit

## 11. Project Disclaimer

ANOVYX AI is an academic prototype. Its predictions are experimental risk assessments and should not be treated as definitive proof of financial fraud or used as the sole basis for real financial decisions.
