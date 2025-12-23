# Support Vector Machine (SVM) from Scratch

This project implements a Linear Support Vector Machine from scratch using Python and NumPy.

## Concepts Used
- Maximum Margin Classifier
- Hinge Loss
- Soft Margin
- Gradient Descent

## How SVM Works
SVM finds a hyperplane that separates two classes with the maximum margin.
Only the closest points (support vectors) affect the hyperplane.

## Equation
Decision function:
w·x + b = 0

Prediction:
- +1 if result ≥ 0
- -1 if result < 0

## Files
- svm.py → SVM implementation
- train.py → training and testing

## Run
```bash
python train.py
