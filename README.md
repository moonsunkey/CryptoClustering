# CryptoClustering
UCB Bootcamp Challenge #19


## Overview
This document outlines the methodology for clustering cryptocurrencies using K-means and Principal Component Analysis (PCA) to assess optimal cluster numbers and the impact of feature reduction.

## Prepare the Data

### Normalize the Data
Normalize features using `StandardScaler` to ensure uniform scaling across all features, critical for unbiased clustering results.

### Create a Scream DataFrame
Convert the normalized data back into a DataFrame, using `coin_id` as the index, ensuring easy manipulation and consistent data handling.

## Determine Optimal Cluster Number

### Elbow Method
The optimal number of clusters was identified at 4 using the elbow method. 

## Cluster Cryptocurrencies

### K-means Clustering
Perform K-means clustering with k at 4, predict clusters for cryptocurrencies, and analyze the clustering patterns based on scaled features.

### Visualization
Visualize clusters through scatter plots focusing on key features like 24-hour and 7-day price changes. Enhance plots with interactivity for detailed analysis by `coin_id`.

## Optimize Clusters with PCA

### Dimensionality Reduction
Employ PCA to reduce feature dimensions to 3, focusing on the principal components that explain the most variance, to streamline the dataset for clustering.

### Analyze Explained Variance
The explained variance by the principal components turns out to be close to 0.9 which means there isn't much sacrifice in accuracy with feature reduction.

## Reapply Clustering Using PCA Data

### Clustering with PCA
K-means was reapplied on PCA-reduced data and the optimal k is at 4. 

### Final Analysis
Using the reduced set of features on this dataset yielded the same clustering result as the original set of features. This is likely due to the small size of the dataset, which minimized the impact of feature reduction. However, in the case of a larger dataset, reducing the number of features would significantly enhance computational efficiency. Nonetheless, it's important to consider that reducing features can sometimes lead to the loss of important information, which might affect the quality of the clustering and the interpretability of the results. Here is a snapshot of the composite plot. 
![composite_plot](path/to/image.png "Optional title")


---
