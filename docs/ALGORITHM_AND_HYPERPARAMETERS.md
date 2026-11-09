# Algorithm and Hyperparameter Analysis

## 1. Random Forest

Random Forest is a supervised ensemble learning algorithm that combines multiple decision trees.

Each tree produces a prediction, and the ensemble combines the predictions to classify a transaction.

### Working Principle

1. Select training samples.
2. Build multiple decision trees.
3. Use random subsets of features during tree construction.
4. Obtain predictions from individual trees.
5. Combine the predictions to produce the final classification.

### Important Hyperparameters

| Parameter | Meaning |
|---|---|
| n_estimators | Number of decision trees |
| max_depth | Maximum depth of each tree |
| min_samples_split | Minimum samples required to split a node |
| min_samples_leaf | Minimum samples required in a leaf |
| max_features | Number of features considered during splitting |
| class_weight | Weight assigned to different classes |

### Proposed Tuning Strategy

The following values can be investigated using validation data:

- n_estimators: 100, 200, 300
- max_depth: None, 10, 20
- min_samples_split: 2, 5, 10
- min_samples_leaf: 1, 2, 4
- class_weight: None, balanced, balanced_subsample

The final values will be selected based on validation performance and computational requirements.

## 2. Isolation Forest

Isolation Forest is an unsupervised anomaly detection algorithm.

It identifies unusual observations by randomly selecting features and splitting the data until observations are isolated.

Anomalies are generally isolated in fewer splits than normal observations.

### Important Hyperparameters

| Parameter | Meaning |
|---|---|
| n_estimators | Number of isolation trees |
| max_samples | Number of samples used to build each tree |
| contamination | Expected proportion of anomalies |
| max_features | Number of features used |
| random_state | Controls reproducibility |

### Proposed Tuning Strategy

Investigate:

- n_estimators: 100, 200, 300
- max_samples: 256, 512, auto
- contamination: values selected using training knowledge or validation analysis
- max_features: 0.5, 0.75, 1.0

Contamination should not be selected by looking at the final test labels.

## 3. Proposed Hybrid Approach

The hybrid approach combines the strengths of supervised and unsupervised learning.

### Random Forest Contribution

Identifies patterns associated with known fraudulent transactions.

### Isolation Forest Contribution

Provides an additional anomaly score for unusual transaction behaviour.

### Combined Prediction

The project will investigate whether using both outputs provides a better balance between precision and recall.

The combination method and decision threshold will be selected using validation data only.

## 4. Parameter Tuning

Hyperparameter tuning will be conducted using:

- Grid Search or Randomized Search.
- Stratified validation where appropriate.
- Chronological validation when time-based splitting is used.
- F1-score and PR-AUC as important selection metrics.

The final parameter configuration and experiment results will be documented for reproducibility.

## 5. Reproducibility

All experiments should record:

- Dataset version.
- Training and testing split.
- Random seed.
- Model parameters.
- Decision threshold.
- Evaluation metrics.
- Execution time.
