## Network Intrusion Detection using PCA + XGBoost
# Project Overview

This project implements a Network Intrusion Detection System (NIDS) using XGBoost combined with Principal Component Analysis (PCA) for dimensionality reduction.
The goal is to detect malicious network activities (attacks) in real-time network traffic, while improving training efficiency by reducing feature redundancy.

# Dataset:

->NSL-KDD Dataset – widely used benchmark for network intrusion detection.

->Includes network connection features and labeled attack types.

# Features:

->Categorical: protocol_type, service, flag

->Numerical: 38 numeric attributes

# Binary classification:

0 → Normal traffic

1 → Attack

# Data Files Used:

->KDDTrain+.TXT – Training set

->KDDTest+.TXT – Test set

->Dataset source: NSL-KDD Dataset

# Methodology
1. Data Preprocessing

->OneHotEncoder for categorical features (protocol_type, service, flag)

->StandardScaler for numerical features

->ColumnTransformer used to combine preprocessing steps for numerical and categorical columns

2. Dimensionality Reduction

->PCA applied to scaled features

->Retain 95% cumulative variance

->Reduces feature redundancy and speeds up training

3. Model Training

->XGBoost Classifier (Gradient Boosted Trees)

# Hyperparameters:

n_estimators=200, max_depth=6, learning_rate=0.1

subsample=0.8, colsample_bytree=0.8

# Trained both:

->Without PCA (baseline)

->With PCA (optimized for speed)

4. Evaluation Metrics

->Classification Report: Precision, Recall, F1-score


->Training Time Comparison

# Results
Model	             Accuracy | Attack Recall | Attack Precision| TrainingTime
XGBoost without PCA	 0.80	      0.66	          0.97	       	4.95 sec
XGBoost with PCA	 0.75	      0.60	          0.93	       	3.56 sec

# Observations:

->PCA reduces dimensionality from ~122 → ~35–40 features

->Training time decreased by ~28%

->Slight drop in recall and ROC-AUC due to information loss

->Trade-off between performance and speed

# Visualization

Confusion Matrix to visualize classification errors