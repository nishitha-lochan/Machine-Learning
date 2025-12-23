K-Nearest Neighbors (KNN) from Scratch in Python:

Overview:

This project implements the K-Nearest Neighbors (KNN) algorithm from scratch using Python. KNN is a supervised machine learning algorithm used for classification (and can be extended for regression). It predicts the label of a new data point based on the labels of its K nearest neighbors in the training dataset.

Features:

->Fully implemented in Python without any ML libraries.   
->Supports n-dimensional feature data.    
->Implements Euclidean distance for finding nearest neighbors.    
->Uses majority voting for classification.    
->Handles multiple test points.

How It Works:

->Fit: Store training data and labels.    
->Distance Calculation: Compute Euclidean distance from the test point to all training points.     
->Find Neighbors: Sort distances and select the top K nearest neighbors.    
->Predict: For classification, choose the most frequent label among the neighbors.

Libraries Used:

->math → For square root calculation.

->collections.Counter → For counting the frequency of labels in majority voting.


Key Points:

->KNN is lazy learning: no model is trained; computation happens during prediction.

->Works best when features are scaled (e.g., normalization or standardization).

->Choosing the right K value is crucial for accuracy.