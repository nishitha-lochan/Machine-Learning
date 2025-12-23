Customer Churn Prediction using Decision Tree

Project Overview:

Customer churn is a major challenge for subscription-based businesses.
This project focuses on analyzing customer behavior, visualizing churn patterns, and building a Decision Tree model to predict whether a customer is likely to churn.

The goal is to identify key factors influencing churn and provide insights that can help businesses improve customer retention.

Dataset Description:

The dataset contains customer-level information including:

-Demographics: Age, Gender

-Engagement: Usage Frequency, Tenure

-Support Behavior: Support Calls, Last Interaction

-Billing Behavior: Payment Delay, Total Spend

-Subscription Details: Contract Length, Subscription Type

-Target Variable: Churn (0 = No, 1 = Yes)

Data Preprocessing:

The following preprocessing steps were applied:

-Dropped irrelevant column (CustomerID)

Handled missing values:

-Numerical features → filled using median

-Categorical features → filled using mode

Encoded categorical variables:

-Label Encoding for binary features (Gender, Churn)

-One-Hot Encoding for multi-category features (Contract Length, Subscription Type, Last Interaction)

-Converted boolean dummy variables to numeric where required

-Ensured consistent preprocessing between training and testing datasets to avoid data leakage

📊 Exploratory Data Analysis (EDA)

Key visualizations performed:

->Churn distribution

->Usage Frequency vs Churn

->Tenure vs Churn (binned bar plot)

->Payment Delay vs Churn

->Contract Length & Subscription Type vs Churn

->Correlation Heatmap (numeric features only)

->Feature Importance

Insights from EDA:

->Customers with low tenure show higher churn rates

->Lower usage frequency is strongly associated with churn

->Monthly contracts have higher churn compared to longer-term contracts

->Customers with payment delays are more likely to churn

Model Building:

->Algorithm used: Decision Tree Classifier

Reason for choice:

->Easy to interpret

->Handles non-linear relationships

->Works well with categorical data

->Model evaluation performed using a separate test dataset

⭐ Feature Importance:

Feature importance analysis revealed that the most influential factors for churn are:

Tenure

Usage Frequency

Payment Delay

Contract Length

Subscription Type

This helps in understanding why customers churn, not just predicting it.

Results:

->The Decision Tree model achieved good predictive performance

->Feature importance aligned well with insights from EDA

->Model provides interpretable business insights for churn reduction strategies

🛠️ Technologies Used

->Python

->Pandas, NumPy

->Matplotlib, Seaborn

->Scikit-learn

->Jupyter Notebook

Future Improvements:

->Try advanced models like Random Forest or XGBoost

->Perform hyperparameter tuning

->Handle class imbalance using SMOTE

->Deploy the model using Flask / FastAPI

Conclusion:

This project demonstrates an end-to-end machine learning workflow:

->Data cleaning

->Visualization

->Model training

->Interpretation

It provides actionable insights into customer churn and serves as a strong foundation for real-world ML applications.