# Dataset Instructions

## PaySim Financial Transaction Dataset

ANOVYX AI uses the PaySim mobile money transaction dataset for financial fraud detection experiments.

### Dataset Source

https://www.kaggle.com/datasets/ealaxi/paysim1

### Download Instructions

1. Open the dataset link.
2. Download the PaySim dataset.
3. Extract the downloaded file.
4. Place the CSV file inside this `data` folder.
5. Confirm that the dataset contains the required transaction and fraud-label columns.

### Expected Dataset File

The commonly distributed PaySim CSV filename is:

PS_20174392719_1491204439457_log.csv

### Important Columns

- step
- type
- amount
- oldbalanceOrg
- newbalanceOrig
- oldbalanceDest
- newbalanceDest
- isFraud

### Dataset Handling

- Do not upload large raw datasets unnecessarily.
- Do not modify the original dataset.
- Perform preprocessing through Python scripts.
- Keep the original fraud labels for supervised evaluation.
- Avoid using the test dataset for model tuning.

### Dataset Information

PaySim is a simulated mobile-money dataset. Its results should not automatically be treated as equivalent to performance on real banking transactions.
