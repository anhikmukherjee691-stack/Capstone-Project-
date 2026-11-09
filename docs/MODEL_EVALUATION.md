# Model Evaluation and Performance Analysis

## 1. Introduction

Fraud detection datasets usually contain significantly more legitimate transactions than fraudulent transactions.

Therefore, accuracy alone is not sufficient to evaluate a fraud detection model.

ANOVYX AI will use multiple evaluation metrics to examine both correct fraud detection and incorrect fraud alerts.

## 2. Evaluation Metrics

### Accuracy

Accuracy measures the proportion of all transactions classified correctly.

Accuracy = (TP + TN) / (TP + TN + FP + FN)

### Precision

Precision measures how many transactions predicted as fraud are actually fraudulent.

Precision = TP / (TP + FP)

### Recall

Recall measures how many actual fraudulent transactions are correctly detected.

Recall = TP / (TP + FN)

### F1-score

F1-score is the harmonic mean of precision and recall.

F1 = 2 × (Precision × Recall) / (Precision + Recall)

### ROC-AUC

ROC-AUC measures the model's ability to distinguish between legitimate and fraudulent transactions across different decision thresholds.

### PR-AUC

PR-AUC measures the area under the Precision-Recall curve.

It is particularly important when the fraudulent class is much smaller than the legitimate class.

## 3. Confusion Matrix

| | Predicted Legitimate | Predicted Fraud |
|---|---:|---:|
| Actual Legitimate | True Negative (TN) | False Positive (FP) |
| Actual Fraud | False Negative (FN) | True Positive (TP) |

### Interpretation

- True Positive: A fraudulent transaction correctly detected.
- True Negative: A legitimate transaction correctly identified.
- False Positive: A legitimate transaction incorrectly flagged as fraud.
- False Negative: A fraudulent transaction incorrectly classified as legitimate.

## 4. Initial Prototype Results

The initial dashboard evaluated 3,000 synthetic test transactions.

The displayed confusion matrix contains:

| | Predicted Legitimate | Predicted Fraud |
|---|---:|---:|
| Actual Legitimate | 2,284 | 651 |
| Actual Fraud | 35 | 30 |

The corresponding metrics are:

| Metric | Initial Result |
|---|---:|
| Accuracy | 77.1% |
| Precision | 4.4% |
| Recall | 46.2% |
| F1-score | 8.0% |

These values represent the initial synthetic-data baseline, not the final PaySim-based model.

## 5. Initial Result Analysis

The model correctly identified 30 fraudulent transactions out of 65 actual fraudulent transactions.

However, it incorrectly flagged 651 legitimate transactions as fraudulent.

This indicates that the initial prototype has a high false-positive count and low precision.

Although the model achieved 77.1% accuracy, its fraud detection performance is not yet satisfactory.

## 6. Planned Improvements

The following improvements will be investigated:

1. Use a suitable financial fraud benchmark dataset.
2. Examine class imbalance.
3. Investigate class weighting and resampling techniques.
4. Tune model hyperparameters.
5. Select a decision threshold using validation data.
6. Compare Random Forest and Isolation Forest.
7. Evaluate the proposed hybrid approach.
8. Compare false positives and false negatives.

## 7. Final Model Comparison

The following table will be completed after the experiments.

| Model | Accuracy | Precision | Recall | F1-score | PR-AUC | ROC-AUC |
|---|---|---|---|---|---|---|
| Random Forest | Pending | Pending | Pending | Pending | Pending | Pending |
| Isolation Forest | Pending | Pending | Pending | Pending | Pending | Pending |
| Hybrid Model | Pending | Pending | Pending | Pending | Pending | Pending |

## 8. Evaluation Conclusion

The final model will be selected based on its ability to detect fraudulent transactions while maintaining an acceptable false-positive rate.

The evaluation will prioritize precision, recall, F1-score, and PR-AUC rather than relying only on accuracy.

All final results will be generated from the held-out test data.
