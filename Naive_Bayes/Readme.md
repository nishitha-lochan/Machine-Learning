## Breast Cancer Prediction using Naive Bayes
# Project Overview

Breast cancer is one of the most common cancers among women. Early detection significantly improves survival rates.
This project uses Gaussian Naive Bayes to classify tumors as Malignant or Benign based on diagnostic features.

# Objective

-Predict whether a tumor is Malignant or Benign.

-Evaluate the model using accuracy, confusion matrix, and classification metrics.

-Demonstrate feature preprocessing, visualization, and ML workflow.

## Why Naive Bayes?

Fast and simple probabilistic classifier.

Works well with high-dimensional data.

Performs well even with small datasets.

Based on Bayes’ theorem with the assumption of feature independence.

# Dataset

-Source: Breast Cancer Wisconsin Dataset (CSV or sklearn)

-Samples: 569

-Features: 30 numerical features (mean, standard error, worst)

-Target Classes:

M → Malignant

B → Benign

## Workflow

-Load dataset.

-Handle missing values.

-Encode target variable (M → 1, B → 0).

-Drop unnecessary columns (_se, _worst, Unnamed: 32).

-Visualize dataset (class distribution, correlation heatmap).

-Separate features (X) and target (y).

-Split dataset into training and testing sets.

-Scale features using StandardScaler.

-Train Gaussian Naive Bayes model.

-Make predictions and evaluate performance.

## Technologies Used
-Python

-Pandas

-Scikit-learn

-Seaborn & Matplotlib

## Results

-Accuracy: 90.6%

-Confusion Matrix:

[[267  23]
 [ 20 146]]


-True Positives (TP): 146

-True Negatives (TN): 267

-False Positives (FP): 23

-False Negatives (FN): 20

-Model correctly predicts most cases, with few misclassifications.

-Classification Metrics (Malignant Class):

-Precision ≈ 0.86

-Recall ≈ 0.88

-F1-score ≈ 0.87

## Visualizations

Class Distribution: Number of Malignant vs Benign cases.

Correlation Heatmap: Shows relationships among features.

Feature Boxplots / Pairplots: Optional for feature analysis.

## Future Improvements

Feature selection using SelectKBest or PCA.

Compare performance with Logistic Regression, SVM, or Random Forest.

Hyperparameter tuning for GaussianNB.

Deploy model using Flask or Streamlit.