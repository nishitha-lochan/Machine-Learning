## Mall Customer Segmentation using Clustering Algorithms

# Project Overview

This project aims to segment customers of a mall into meaningful groups based on their demographic and behavioral features. Clustering is used to find natural groupings without prior labels. The features considered are:

-Age: Customer’s age

-Annual Income: Customer’s yearly income (k$)

-Spending Score: A score assigned based on customer spending behavior

The goal is to identify distinct customer segments to help marketing and business decisions.

## Problem Statement

-Cluster customers into groups with similar characteristics.

-Understand customer profiles for targeted marketing strategies.

-Compare different clustering algorithms (K-Means, Hierarchical, DBSCAN) for effectiveness.

# Dataset

-Source: Mall Customer Dataset

-Size: 200 records, 5 features (CustomerID, Gender, Age, Annual Income, Spending Score)


# Preprocessing

->Load dataset and inspect for null/missing values

->Drop irrelevant columns: CustomerID and Gender

->Apply Standard Scaling to features to ensure equal weighting during clustering

## Algorithms Implemented

->K-Means Clustering

-- Partitioned data into K clusters

-- Used silhouette score to measure cluster quality

->Hierarchical Clustering (Agglomerative)

-- Built a hierarchy of clusters

-- Visualized clusters using 2D scatter plots

->DBSCAN (Density-Based)

-- Identified dense regions as clusters

-- Detected noise points (-1 label)

-- Tuned eps and min_samples for optimal cluster detection

## Visualizations

-> Pairplot: Compare features and detect patterns

-> Correlation Heatmap: Understand feature relationships

-> Histograms / Boxplots: Inspect distribution and outliers

-> 2D Scatter Plots: Visualize clusters by feature pairs

-> 3D Scatter Plot: Visualize clustering across three features


## Evaluation Metrics

Algorithm	               Silhouette Score
K-Means:     	               0.36
Hierarchical:   	           0.32
DBSCAN:                    	   0.10

Silhouette Score: Measures how well points are clustered

Higher values indicate better-defined clusters

K-Means performed best for this dataset

## Key Insights

->Customers can be segmented into distinct groups for targeted marketing.

->K-Means is the most suitable clustering algorithm for this dataset.

->DBSCAN detected some noise but produced fewer distinct clusters.

->Visualizations help interpret clusters and customer profiles.

# Conclusion

Clustering helps discover hidden patterns in customer behavior.

K-Means is effective for numeric features like Age, Annual Income, and Spending Score.

# Future work:

Include additional features like gender or product category

Experiment with PCA for dimensionality reduction

Tune DBSCAN parameters for better density-based clustering