# ANOVYX AI
### AI-Driven Intelligent Fraud & Anomaly Detection System
---
**Detect the unusual. Prevent the unthinkable.**

## About the Project

ANOVYX AI is our B.Tech final-year capstone project. The main idea is to develop a system that can identify potentially fraudulent financial transactions using machine learning.

As online transactions continue to increase, detecting suspicious activities has become an important challenge. Traditional systems mostly depend on predefined rules, which may not always identify new or unusual fraud patterns.

Through this project, we are trying to build a system that studies transaction details, detects suspicious behaviour and displays the prediction through a simple dashboard.

## What we are trying to achieve

- Detect potentially fraudulent financial transactions.
- Identify unusual transaction patterns.
- Study different machine learning algorithms for fraud detection.
- Reduce incorrect fraud alerts as much as possible.
- Display transaction analysis through a web dashboard.

## How the system works

The current project follows a basic machine learning workflow:

1. Load the transaction dataset.
2. Clean and prepare the data.
3. Select the relevant transaction features.
4. Train the machine learning model.
5. Test the model using unseen transactions.
6. Display the prediction and evaluation results on the dashboard.

## Algorithms

We initially worked with Random Forest for transaction classification.

As part of the improvements suggested during our project review, we are also exploring Isolation Forest for identifying unusual transaction behaviour.

We plan to compare both models and study whether combining them can improve the overall detection process.

## Dataset

For the initial prototype, we used synthetically generated transaction data to test the working of the application.

We are now moving towards the PaySim mobile money transaction dataset for further experiments.

Dataset link: https://www.kaggle.com/datasets/ealaxi/paysim1

PaySim is a simulated transaction dataset containing both legitimate and fraudulent transactions. It provides features such as transaction amount, transaction type and account balances.

## Technologies Used

- Python
- Pandas and NumPy
- Scikit-learn
- Streamlit
- Matplotlib and Seaborn

## Current Progress

The first version of the prototype includes:

- A working Streamlit dashboard.
- Transaction analysis interface.
- Initial Random Forest implementation.
- Basic fraud prediction.
- Model performance display.

We are currently working on improving the dataset, studying anomaly detection algorithms and making the model evaluation more reliable.

## Future Improvements

Some features we would like to work on include:

- Improving fraud detection performance.
- Combining supervised learning and anomaly detection.
- Adding better explanations for suspicious predictions.
- Maintaining a record of analysed transactions.
- Exploring real-time transaction monitoring.

## Note

This project is being developed for academic purposes as part of our B.Tech final-year capstone project. The current prototype is experimental and is not intended to make actual banking decisions.
