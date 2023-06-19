# Cryptocurrency Market Data Cluster Analysis

This repository contains code for performing cluster analysis on cryptocurrency market data using K-means clustering and Principal Component Analysis (PCA).

## Overview

The purpose of this project is to analyze and cluster cryptocurrencies based on their price change percentage over different time periods. The data is obtained from the `crypto_market_data.csv` file located in the `Resources` directory.

The following steps are performed in the analysis:

1. **Data Preparation**: The data is loaded into a Pandas DataFrame and normalized using the StandardScaler module from scikit-learn.

2. **Finding the Best Value for k Using the Original Data**: The inertia values for different values of k are computed to identify the optimal number of clusters. The results are plotted on an elbow curve.

3. **Cluster Cryptocurrencies with K-means Using the Original Data**: The K-means model is initialized with the optimal value of k determined in the previous step. The model is fitted using the scaled data, and the resulting cluster labels are assigned to each cryptocurrency.

4. **Visualizing Clusters**: The original data is plotted using a scatter plot, with the points colored according to their assigned clusters.

5. **Optimize Clusters with Principal Component Analysis (PCA)**: PCA is applied to reduce the dimensionality of the data. The explained variance ratio is computed to assess the information retained in each principal component.

6. **Finding the Best Value for k Using the PCA Data**: The inertia values for different values of k are computed using the PCA-transformed data. The optimal number of clusters is determined based on the elbow curve.

7. **Cluster Cryptocurrencies with K-means Using the PCA Data**: The K-means model is initialized with the optimal value of k determined using PCA. The model is fitted using the PCA-transformed data, and the resulting cluster labels are assigned to each cryptocurrency.

8. **Visualizing and Comparing Results**: The cluster analysis results using both the original data and PCA-transformed data are visualized using scatter plots and elbow curves to compare the impact of using fewer features on clustering.

## Results

The cluster analysis results can be observed in the generated scatter plots and elbow curves. Both the original data and PCA-transformed data are used to cluster the cryptocurrencies, and the results are compared.

The optimal number of clusters determined in both cases is 4. This indicates that the elbow graphs and scatter plots remain unchanged when using fewer features through PCA, suggesting that the reduced dimensionality does not significantly impact the clustering results.

For a detailed explanation of the code and analysis, please refer to the comments in the `main.py` script.

