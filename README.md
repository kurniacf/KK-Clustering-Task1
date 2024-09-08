# Clustering Task - Hepatitis C Virus (HCV) Dataset

## Class: Computational Intelligence / Kecerdasan Komputasional - B  
**Name**: Kurnia Cahya Febryanto  

---

## Table of Contents

1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Requirements](#requirements)
4. [Data Preprocessing](#data-preprocessing)
5. [Clustering Algorithms](#clustering-algorithms)
   - [K-Means Clustering](#k-means-clustering)
   - [Agglomerative Clustering](#agglomerative-clustering)
6. [Additional Analysis](#additional-analysis)
   - [Elbow Method for Optimal K](#elbow-method-for-optimal-k)
   - [Dendrogram for Agglomerative Clustering](#dendrogram-for-agglomerative-clustering)
   - [Cluster Size Distributions](#cluster-size-distributions)
   - [Cluster Interpretability](#cluster-interpretability)
7. [Performance Evaluation](#performance-evaluation)
8. [Visualization of Clusters](#visualization-of-clusters)
9. [Conclusion](#conclusion)

---

## Introduction

This project explores clustering techniques applied to the **Hepatitis C Virus (HCV)** dataset to group patients based on laboratory and demographic data. The primary goal is to distinguish between healthy individuals (blood donors) and patients with different stages of Hepatitis C progression, such as **Hepatitis**, **Fibrosis**, and **Cirrhosis**. Two clustering algorithms are compared: **K-Means** and **Agglomerative Clustering**, using metrics like **Sum of Squared Errors (SSE)** and the **Silhouette Coefficient**.

## Dataset

The dataset includes **615 instances** and **12 features**, capturing laboratory results and demographic information. The dataset contains numerical attributes such as ALT, AST, and demographic features like **Age** and **Sex**. The target variable classifies patients into categories like blood donors and those in different stages of Hepatitis C.

## Requirements

This project requires the following libraries:
- Pandas
- Numpy
- Matplotlib
- Scikit-Learn
- UCI ML Repo (for fetching the dataset)

## Data Preprocessing

To prepare the data for clustering:
- **Handle Missing Values**: Replace missing values with column means.
- **Standardization**: Apply `StandardScaler` to ensure uniform scaling of features for better clustering performance.

## Clustering Algorithms

### K-Means Clustering
K-Means is a partition-based clustering method used here to group the dataset into 3 clusters. Performance is evaluated using SSE and the Silhouette Coefficient.

### Agglomerative Clustering
Agglomerative Clustering is a hierarchical method that iteratively merges data points. It is also applied with 3 clusters, and the results are evaluated using the Silhouette Coefficient.

## Additional Analysis

### Elbow Method for Optimal K
The Elbow Method is applied to determine the optimal number of clusters for K-Means by plotting the SSE against various values of K.

### Dendrogram for Agglomerative Clustering
A dendrogram is used to visualize hierarchical clustering, showing how clusters merge step by step in Agglomerative Clustering.

### Cluster Size Distributions
The size of each cluster is analyzed to assess the distribution of data points across clusters, ensuring balanced clusters.

### Cluster Interpretability
The centroids of K-Means clusters are examined to understand which features influence each cluster, providing interpretability to the results.

## Performance Evaluation

The performance of K-Means and Agglomerative Clustering is compared based on:
- **Sum of Squared Errors (SSE)** for K-Means.
- **Silhouette Coefficient** for both algorithms, indicating how well-separated the clusters are.

## Visualization of Clusters

Principal Component Analysis (PCA) is used to reduce the data to 2 dimensions, allowing visualization of the clusters formed by both K-Means and Agglomerative Clustering.

## Conclusion

- **Agglomerative Clustering** outperforms K-Means based on the **Silhouette Coefficient**, suggesting better-separated clusters.
- While **K-Means** is effective for partitioning, it produced less distinct clusters in this dataset, as indicated by a lower Silhouette score.
- Overall, **Agglomerative Clustering** provides more coherent and distinct clusters, making it better suited for identifying different stages of Hepatitis C in this dataset.
