# Literature Review
## Financial Fraud Detection Using Machine Learning and Anomaly Detection

### 1. Introduction

Financial fraud detection has become an important application of machine learning due to the increasing volume of digital transactions. Traditional rule-based systems rely on predefined conditions and may struggle to identify previously unseen fraudulent behaviour.

Research has explored supervised machine learning, ensemble learning, anomaly detection, and explainable AI to improve the detection of suspicious transactions.

### 2. Existing Research Approaches

#### 2.1 Supervised Machine Learning

Supervised algorithms such as Logistic Regression, Decision Trees, Random Forest, and Support Vector Machines learn from labelled transaction data.

Random Forest is useful because it combines multiple decision trees and can model complex relationships between transaction features.

However, its performance can be affected by class imbalance and the decision threshold used to classify transactions.

#### 2.2 Anomaly Detection

Unsupervised anomaly detection identifies observations that differ significantly from normal patterns.

Isolation Forest is one such algorithm. It isolates unusual observations through random feature selection and random splitting.

This approach is useful for investigating suspicious transactions that may not follow previously learned fraud patterns.

#### 2.3 Hybrid Learning Approaches

Hybrid approaches combine multiple learning techniques to use their complementary strengths.

For financial fraud detection, supervised classification can identify known fraud patterns, while anomaly detection can provide additional information about unusual transaction behaviour.

The effectiveness of such combinations must be tested using the same dataset and evaluation protocol.

#### 2.4 Explainable AI

Explainable AI techniques such as SHAP help explain the contribution of individual features to a model's predictions.

Interpretability is important in fraud detection because analysts may need to understand why a transaction was flagged.

### 3. Selected Research Papers

#### Paper 1: Explainable AI-Enhanced Ensemble Learning for Financial Fraud Detection in Mobile Money Transactions (2024)

Authors: Deepshika Vijayanand and Girijakumari Sreekantan Smrithy.

The study uses the PaySim mobile-money dataset containing simulated financial transactions. It investigates ensemble learning and SHAP-based explanations to improve fraud detection and interpretability.

**Key learning:**
- Ensemble models can improve fraud detection.
- PaySim provides a relevant transaction dataset.
- Explainability can help interpret model predictions.

**Relevance to ANOVYX AI:**
This paper supports the use of financial transaction data and highlights the importance of explainable fraud detection.

#### Paper 2: Fraud Detection in Financial Transactions Using Machine Learning: Insights from the PaySim Mobile Money Dataset (2025)

The study compares Logistic Regression, K-Nearest Neighbours, Decision Tree, and Random Forest using the PaySim dataset.

It highlights the trade-off between detecting fraudulent transactions and generating false-positive alerts.

**Key learning:**
- Fraud datasets can be highly imbalanced.
- Accuracy alone does not describe fraud detection performance.
- Precision, recall, and F1-score are important for model comparison.

**Relevance to ANOVYX AI:**
The paper supports the selection of PaySim and the use of multiple evaluation metrics.

#### Paper 3: A Comparative Study of SMOTE Preprocessing for Fraud Prediction in Mobile Banking Transactions (2025)

This IEEE conference study investigates SMOTE for addressing class imbalance in the PaySim dataset and compares multiple machine learning classifiers.

**Key learning:**
- Class imbalance can significantly affect model performance.
- Resampling techniques should be evaluated carefully.
- Ensemble algorithms can provide useful fraud detection performance.

**Relevance to ANOVYX AI:**
This study motivates an investigation of class imbalance handling and comparative model evaluation.

#### Paper 4: Mobile Payment Fraud Detection Using Random Forest Algorithm on PaySim Dataset (2026)

This IEEE conference publication investigates Random Forest with resampling techniques on the PaySim dataset.

The study reports high recall but also demonstrates that precision can be low when the model is configured to detect almost all fraudulent transactions.

**Key learning:**
- High recall does not automatically mean a practical fraud detection system.
- False-positive alerts must also be considered.
- Precision and recall need to be evaluated together.

**Relevance to ANOVYX AI:**
This paper supports the need to balance fraud detection and false-positive reduction.

### 4. Research Gap

From the reviewed studies, the following challenges are identified:

1. Severe class imbalance can affect fraud detection.
2. High recall may produce excessive false-positive alerts.
3. Supervised models may have difficulty identifying unusual patterns not represented in the training labels.
4. Fraud detection systems require appropriate evaluation metrics.
5. Interpretability is important for understanding suspicious transaction predictions.

### 5. Proposed Research Direction

ANOVYX AI investigates a hybrid approach combining:

- Random Forest for supervised fraud classification.
- Isolation Forest for unsupervised anomaly detection.

The project will examine whether combining the fraud probability and anomaly score provides better performance than using either model independently.

The proposed approach will be evaluated using precision, recall, F1-score, PR-AUC, ROC-AUC, and confusion matrices.

### 6. Conclusion

The reviewed studies demonstrate the importance of suitable financial datasets, class imbalance handling, comparative model evaluation, and explainability.

Based on these findings, ANOVYX AI investigates combining supervised fraud classification and unsupervised anomaly detection to improve transaction risk assessment.

## References

[1] D. Vijayanand and G. S. Smrithy, "Explainable AI-enhanced ensemble learning for financial fraud detection in mobile money transactions," 2024.
https://doi.org/10.1177/18724981241289751

[2] "Fraud Detection in Financial Transactions Using Machine Learning: Insights from the PaySim Mobile Money Dataset," 2025.
https://doi.org/10.30574/wjarr.2025.28.3.4058

[3] "A Comparative Study of SMOTE Preprocessing for Fraud Prediction in Mobile Banking Transactions," 2025, IEEE.
https://doi.org/10.1109/ICIC68054.2025.11309462

[4] "Mobile Payment Fraud Detection Using Random Forest Algorithm on PaySim Dataset," 2026, IEEE.
https://doi.org/10.1109/ICCE-Taiwan71481.2026.11652599
