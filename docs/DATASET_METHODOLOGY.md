# Dataset and Methodology

## 1. Dataset Selection

The project plans to use the PaySim mobile money transaction dataset.

Dataset link:
https://www.kaggle.com/datasets/ealaxi/paysim1

PaySim is a simulated mobile-money transaction dataset designed for studying financial fraud detection.

It contains approximately 6.36 million transaction records and 8,213 fraudulent transactions.

## 2. Dataset Features

Important dataset columns include:

| Feature | Description |
|---|---|
| step | Time step of the transaction |
| type | Transaction type |
| amount | Transaction amount |
| nameOrig | Originating account identifier |
| oldbalanceOrg | Sender's balance before transaction |
| newbalanceOrig | Sender's balance after transaction |
| nameDest | Destination account identifier |
| oldbalanceDest | Recipient's balance before transaction |
| newbalanceDest | Recipient's balance after transaction |
| isFraud | Target variable indicating fraud |
| isFlaggedFraud | Existing system flag |

The target variable is `isFraud`.

- 0 represents a legitimate transaction.
- 1 represents a fraudulent transaction.

## 3. Data Preprocessing

The following preprocessing operations will be performed:

1. Load the dataset.
2. Inspect its shape and column names.
3. Check missing and duplicate values.
4. Analyse the distribution of legitimate and fraudulent transactions.
5. Encode categorical transaction types.
6. Remove identifier columns that are not suitable as direct model inputs.
7. Examine features for target leakage.
8. Separate training, validation, and testing data.

The existing `isFlaggedFraud` field will not be used as a model input because it represents an existing fraud flag and could introduce leakage or bias into the evaluation.

## 4. Feature Engineering

Potential model features include:

- Transaction amount.
- Transaction type.
- Transaction time step.
- Sender's previous balance.
- Sender's new balance.
- Recipient's previous balance.
- Recipient's new balance.
- Sender balance difference.
- Recipient balance difference.

Feature usefulness and leakage risk will be checked before final selection.

## 5. Data Splitting

The dataset will be divided into training, validation, and testing subsets.

A chronological split is preferred when transaction time is available:

- Training data: earlier transactions.
- Validation data: subsequent transactions.
- Testing data: later unseen transactions.

This helps evaluate the model on transactions that occur after its training period.

The test set will not be used for parameter tuning or threshold selection.

## 6. Proposed Model Architecture

### Model 1: Random Forest

Random Forest will be trained using labelled transactions.

It will estimate the probability that a transaction is fraudulent.

### Model 2: Isolation Forest

Isolation Forest will be trained using legitimate transactions from the training period.

It will calculate an anomaly score for transactions.

### Model 3: Hybrid Model

The proposed hybrid model will investigate combining:

- Random Forest fraud probability.
- Isolation Forest anomaly score.

The two outputs will be combined using a validation-selected decision rule or a separately trained combination model.

The final combination strategy will be documented after implementation.

## 7. Model Comparison

The following models will be compared:

1. Random Forest baseline.
2. Isolation Forest anomaly detector.
3. Hybrid Random Forest and Isolation Forest.

All models will be evaluated on the same held-out test period.

## 8. Expected Outcome

The project aims to determine whether the hybrid approach can improve fraud detection while maintaining a manageable false-positive rate.

No performance improvement will be claimed until the experiments are completed.
