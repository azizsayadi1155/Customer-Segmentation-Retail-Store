# Customer Segmentation Using RFM Analysis and Clustering

## Project Overview

This project aims to segment customers based on their purchasing behavior using Recency, Frequency, and Monetary (RFM) analysis. I applied both K-Means and Hierarchical clustering methods to identify distinct customer groups and evaluate the quality of these clusters using the silhouette score.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Feature Engineering](#feature-engineering)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Clustering Methods](#clustering-methods)
  - [K-Means Clustering](#k-means-clustering)
  - [Hierarchical Clustering](#hierarchical-clustering)
- [Model Evaluation](#model-evaluation)
- [Cluster Interpretation](#cluster-interpretation)
- [Visualizations](#visualizations)
- [Conclusion](#conclusion)
- [Usage](#usage)
- [Dependencies](#dependencies)

## Dataset

The dataset used in this project is the **Online Retail** dataset, which contains transactional data of an online retail store. Each record represents an invoice and contains information about the products purchased, the customer, the purchase quantity, and the price.
https://archive.ics.uci.edu/dataset/352/online+retail

## Data Preprocessing

- Remove entries with missing CustomerID.
- Convert `InvoiceDate` to datetime format.
- Calculate the total amount for each invoice (`Quantity * UnitPrice`).
- Remove duplicate records.
- Filter out records with non-positive `Quantity` and `UnitPrice`.

## Feature Engineering

I calculate the following RFM features for each customer:

- **Recency:** Number of days since the last purchase.
- **Frequency:** Number of purchases made by the customer.
- **Monetary:** Total amount spent by the customer.

## Exploratory Data Analysis

I perform EDA to understand the distribution of the RFM features:

- Histogram of Recency
- Histogram of Frequency
- Histogram of Monetary

## Clustering Methods

### K-Means Clustering

- Applied directly on the original RFM features.
- Determined the optimal number of clusters using the Elbow method.
- Evaluated the clustering using the silhouette score.

### Hierarchical Clustering

- Applied directly on the original RFM features.
- Used Ward's method for linkage.
- Visualized the dendrogram to determine the optimal number of clusters.
- Evaluated the clustering using the silhouette score.

## Model Evaluation

I used the silhouette score to evaluate the quality of both K-Means and Hierarchical clustering methods.

## Cluster Interpretation

I analyzed the resulting clusters by examining the mean RFM values for each cluster to understand the characteristics of each customer segment.

## Visualizations

- Scatter plot of Recency vs. Frequency colored by K-Means clusters.
- Scatter plot of Recency vs. Frequency colored by Hierarchical clusters.
- Bar plot of mean RFM values for each cluster.

## Conclusion

The project successfully segments customers into distinct groups based on their purchasing behavior. These segments can help businesses tailor their marketing strategies and improve customer retention.
