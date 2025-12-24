Breast Cancer Prediction using Naive Bayes (From Scratch)
## Overview:

This project demonstrates an end-to-end implementation of a Naive Bayes classifier from scratch to predict whether a breast tumor is Malignant (M) or Benign (B) using medical diagnostic features.

# The main focus of this project is to:

-Understand Naive Bayes at a conceptual and mathematical level

-Choose the correct Naive Bayes variant based on data type

-Implement the algorithm without using sklearn’s Naive Bayes

## Algorithm:

Gaussian Naive Bayes

# Why Gaussian Naive Bayes?:

-The dataset contains continuous numerical features

-Medical measurements (radius, area, perimeter, etc.) are well-modeled using a normal distribution

-Gaussian Naive Bayes is widely used as a baseline model in medical ML problems

## Dataset:

-Dataset: Breast Cancer Wisconsin Dataset

-Target Column: diagnosis

M → Malignant

B → Benign

-Features: Continuous numeric tumor measurements

-Dropped Columns:

id (non-informative)

##Project Workflow:

-Load dataset using Pandas

-Remove unnecessary columns (id)

-Split data into training and testing sets

-Train Gaussian Naive Bayes model from scratch

-Predict on unseen test data

-Evaluate model performance

## Mathematical Background:

Naive Bayes is based on Bayes’ Theorem:

                   P(y∣X)∝P(y)i=1∏n​P(xi​∣y)
# Key Assumptions:

-Features are conditionally independent

-Feature values follow a Gaussian (Normal) distribution

-Log probabilities are used to prevent numerical underflow

# Technologies Used:

Python

NumPy

Pandas

Scikit-learn (only for train-test split and evaluation)

 No sklearn Naive Bayes model was used

# Model Evaluation:

Metric Used: Accuracy

Train-Test Split: 80% / 20%

Special importance is given to correct classification of malignant tumors, which is critical in medical diagnosis.

📂 Project Structure
├── data.csv
├── Naive_Bayes.ipynb
├── README.md

## Key Learnings

#Understanding different types of Naive Bayes:

Gaussian

Bernoulli

Multinomial

Categorical

Choosing algorithms based on data distribution

Implementing ML algorithms from scratch

Importance of probabilistic modeling in healthcare applications

## Future Improvements

Add confusion matrix and recall score

Compare performance with sklearn’s GaussianNB

Experiment with Logistic Regression and SVM

Perform feature scaling and exploratory analysis