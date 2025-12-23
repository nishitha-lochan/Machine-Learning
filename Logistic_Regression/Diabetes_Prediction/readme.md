Diabetes Prediction Project using Logistic Regression

Project Overview:
This project predicts the likelihood of diabetes in a patient using logistic regression, a popular machine learning algorithm for binary classification.

The model is trained on a dataset containing medical and lifestyle features and predicts:

-Whether a patient has diabetes (Yes/No)  
-Probability of diabetes  
-Risk level (Low/Medium/High)

Additionally, the project evaluates the model using accuracy, confusion matrix, classification report, and ROC AUC, and provides visualizations for better understanding.

Features:

The model uses 8 patient features:

1.age	:                Age of the patient                                                           
2.gender	:            Male=1, Female=0   
3.hypertension	:      1 = Yes, 0 = No  
4.heart_disease	 :     1 = Yes, 0 = No    
5.smoking_history	:    Encoded numerically (0,1,2…)   
6.bmi	          :      Body Mass Index   
7.HbA1c_level	 :       Glycated hemoglobin level (%)   
8.blood_glucose_level:	Blood glucose level (mg/dL)

Target: diabetes → 0 (No) / 1 (Yes)

How It Works:

1.Data Preprocessing:

Features and target are separated.

2.Train-test split (80-20) for model evaluation.

3.Model Training:

Logistic Regression is trained with max_iter=1000.

4.Evaluation Metrics:

-Accuracy → overall correctness  
-Confusion Matrix → true positives, false positives, etc.  
-Classification Report → precision, recall, f1-score  
-ROC Curve & AUC → model’s ability to distinguish classes  

5.New Patient Prediction:

-Accepts 8 feature values  
-Outputs prediction, probability, and risk level

6.Visualization:

-ROC Curve shows the trade-off between True Positive Rate and False Positive Rate at various thresholds.

-AUC (Area Under Curve) indicates model performance:

0.5 → random guess   
0.7–0.8 → acceptable     
0.8–0.9 → good  
0.9 → excellent  

Usage:

-> Update new_patient values to predict for any patient.  
-> Ensure feature order matches training dataset  

Probability (y_prob) is used to determine risk level:

-> ≥0.8 → High Risk   
-> 0.5–0.8 → Medium Risk     
-> <0.5 → Low Risk  

Technologies Used:

->Python 3.x   
->Pandas    
->NumPy  
->Scikit-learn  
->Matplotlib

Project Highlights:

-> Handles new patient predictions with probability and risk level    
-> Evaluates model using multiple metrics including ROC AUC  
-> Fully reproducible and easy to extend for other datasets
