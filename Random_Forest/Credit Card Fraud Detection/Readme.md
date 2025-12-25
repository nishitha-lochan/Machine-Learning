## Project Overview

Credit card fraud detection is a binary classification problem where the objective is to identify fraudulent transactions while minimizing false alarms.
This project applies ensemble learning techniques—Random Forest and AdaBoost—to detect fraud in a highly imbalanced dataset.

# Objectives

->Detect fraudulent credit card transactions

->Handle severely imbalanced data

->Compare Random Forest (Bagging) vs AdaBoost (Boosting)

->Evaluate models using appropriate metrics beyond accuracy

## Dataset

->European Credit Card Fraud Dataset

->Total transactions: 284,807

->Fraud cases: 492 (0.17%)

->Features: V1 – V28 (anonymized using PCA), Amount, Time

->Target column:

        0 → Normal transaction

        1 → Fraud

🔗 Dataset source: Kaggle – Credit Card Fraud Detection

## Algorithms Used
# Random Forest

->Ensemble of decision trees using bagging

->Reduces variance and overfitting

->Handles non-linear relationships well

->Provides feature importance

# AdaBoost

->Boosting algorithm

->Combines multiple weak learners (decision stumps)

->Focuses more on misclassified samples

->Improves performance on hard-to-classify cases

## Project Workflow

->Data Loading

->Exploratory Data Analysis (EDA)

->Feature Scaling

->Handling Class Imbalance

->Train-Test Split (Stratified)

->Model Training

->Model Evaluation

->Model Comparison

## Data Preprocessing

->No missing values found

->Scaled Amount feature using StandardScaler

->Used stratified sampling to preserve class distribution

->Addressed imbalance using:

->class_weight = "balanced"

## Evaluation Metrics

->Due to class imbalance, accuracy alone is misleading.
The following metrics were used:

->Precision

->Recall

->F1-Score

->ROC-AUC

->Confusion Matrix

## Model Performance Summary
# Model	Strengths:

->Random Forest: High overall performance, stable predictions
->AdaBoost:	Better focus on difficult fraud cases

# Key Insight:
->Random Forest provides better overall balance, while AdaBoost excels at identifying misclassified fraud samples.

## Feature Importance

->Random Forest feature importance helps identify:

->High-risk transaction patterns

->Influential features contributing to fraud detection

->Useful for business decision-making

## Key Learnings

->Importance of evaluation metrics for imbalanced datasets

->Difference between bagging vs boosting

->Trade-off between precision and recall in fraud detection

->How ensemble models outperform single classifiers

## Future Improvements

->Apply SMOTE for oversampling

->Perform hyperparameter tuning with GridSearchCV

->Compare with XGBoost / LightGBM

->Deploy model using Flask / FastAPI

#3 Tech Stack

Python

Pandas, NumPy

Scikit-learn

Matplotlib, Seaborn

Jupyter Notebook