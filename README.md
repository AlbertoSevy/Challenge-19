# Challenge-19
Cryptocurrency Clustering Analysis

Overview

This project focuses on clustering cryptocurrencies using the K-means algorithm and optimizing the clustering process with Principal Component Analysis (PCA). The goal is to identify distinct groups of cryptocurrencies based on their market performance and price behavior. The process involves determining the best number of clusters (
k
k), analyzing the effect of dimensionality reduction, and visualizing the results using interactive scatter plots.

Methodology and Results

1. Finding the Best Value for 
k
k Using the Scaled DataFrame
To determine the optimal number of clusters (
k
k), the elbow method was applied:

Steps:
Tested 
k
k values ranging from 1 to 11.
Computed the inertia for each 
k
k.
Plotted the inertia values on a line chart to visualize the elbow curve.
Result: The elbow point was observed at 
k
=
4
k=4, indicating the best trade-off between cluster compactness and variance.
2. Clustering Cryptocurrencies with K-means on the Scaled DataFrame
Using the scaled dataset and 
k
=
4
k=4, the cryptocurrencies were clustered:

Key Insights:
Cluster labels were added to the DataFrame to identify each cryptocurrency's group.
A scatter plot was created with:
X-axis: 24-hour price change percentage.
Y-axis: 7-day price change percentage.
Points colored by their cluster labels, revealing distinct groupings.
Hover functionality allowed identification of individual cryptocurrencies.
3. Optimizing Clusters with Principal Component Analysis (PCA)
To simplify the dataset and reduce computational complexity, PCA was applied:

Steps:
Reduced the scaled DataFrame to three principal components.
Retrieved explained variance:
The three principal components captured 88.2% of the total variance, ensuring minimal loss of information.
Created a new DataFrame with PCA-transformed data.
4. Finding the Best Value for 
k
k Using the PCA DataFrame
The elbow method was repeated on the PCA-transformed data:

Steps:
Tested 
k
k values from 1 to 11.
Computed and plotted the inertia values.
Result: The optimal 
k
k remained 
k
=
4
k=4, consistent with the original scaled DataFrame.
5. Clustering Cryptocurrencies with K-means on the PCA DataFrame
Clustering was performed on the PCA-transformed dataset:

Key Insights:
Cluster labels were added to the PCA DataFrame.
Scatter plot created with:
X-axis: Principal Component 1 (PC1).
Y-axis: Principal Component 2 (PC2).
Points colored by cluster labels, visualizing group distinctions.
Hover functionality highlighted individual cryptocurrencies.
Observations

Impact of Dimensionality Reduction:
Using PCA reduced the dataset's complexity while maintaining clustering performance.
The clusters were consistent between the original and PCA-transformed datasets.
PCA provided a simpler visualization of the clustering results.
Cryptocurrency Groupings:
Distinct clusters represent different market behaviors, such as high volatility or stable price trends.
The clustering process highlighted patterns in price changes over 24 hours and 7 days.
Technologies Used

Python Libraries:
sklearn for K-means and PCA.
hvPlot for interactive visualizations.
pandas and numpy for data manipulation.
Key Techniques:
Elbow method for 
k
k optimization.
Principal Component Analysis (PCA) for dimensionality reduction.
Interactive plotting for cluster analysis.
This project demonstrated the power of clustering and dimensionality reduction in analyzing complex financial datasets, providing actionable insights into cryptocurrency behavior.
