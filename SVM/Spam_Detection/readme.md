Spam Detection using SVM

Project Overview:

This project implements a Spam Detection System using Support Vector Machines (SVM). The system classifies text messages as “spam” or “ham” (non-spam) using machine learning. It uses TF-IDF vectorization to convert text into numerical features suitable for the SVM model.

Features:
-Preprocess text messages (lowercasing, removing punctuation)   
-Convert text into TF-IDF vectors  
-Label Encoding    
-Train Linear SVM classifier   
-Evaluate model performance using accuracy, precision, recall, and F1-score  
-Predict spam/ham for new messages   
-Save and load the trained model and vectorizer for reuse

Dataset:
-The dataset contains SMS messages labeled as ham or spam.

Example columns:
label: Target label (ham or spam)
message: Text message

Requirements:
-Python 3.8+

Libraries:
-pandas  
-numpy  
-matplotlib  
-scikit-learn  
-joblib  
-re