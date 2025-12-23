# Decision Tree from Scratch in Python

This repository demonstrates how to **build a Decision Tree classifier from scratch** in Python, without using any machine learning libraries. The tree is built using **Information Gain** as the splitting criterion for classification problems.

---

## Dataset

The example dataset consists of students’ study hours and attendance, with the target being **Pass (1) or Fail (0)**:

| Hours Studied | Attendance | Pass/Fail |
|---------------|------------|-----------|
| 1             | 20         | 0         |
| 2             | 30         | 0         |
| 3             | 40         | 0         |
| 3             | 62         | 0         |
| 1             | 70         | 0         |
| 7             | 70         | 1         |
| 8             | 80         | 1         |
| 8             | 85         | 1         |
| 9             | 80         | 1         |
| 9             | 85         | 1         |
| 10            | 90         | 1         |
| 10            | 96         | 1         |

---

## Features

- **Hours Studied**  
- **Attendance (%)**  

**Target**: Pass (1) / Fail (0)

---

## How It Works

1. **Entropy Calculation**:  
   Measures the impurity of a node. Formula:
   Entropy(S) = - p0log2(p0) - p1log2(p1)


2. **Information Gain (IG)**:  
Measures how much a feature split reduces entropy:
G(S, feature) = Entropy(S) - WeightedEntropy(children)


3. **Threshold Selection**:  
For each feature, the algorithm tests all unique values as thresholds and selects the one with the **highest IG**.

4. **Recursive Tree Building**:  
- Split the dataset at the best feature + threshold  
- Recurse on left and right subtrees  
- Stop when all samples are pure or no features remain  

5. **Prediction**:  
Traverse the tree comparing features with thresholds until reaching a leaf node.

---

## How to Run

1. Clone the repository:
```bash
git clone <your-repo-url>



