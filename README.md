# Retail_Customer_Analysis_Recommendation_System

## 📘 Project Owerview
This project focuses on analyzing retail customer purchase behavior, segmenting customers using clustering techniques, and generating personalized product recommendations. The dataset used comes from a real-world retail transaction log and contains information about invoices, products, and customer purchases.

## 🔁 Key Processes
1. Data Cleaning

Removed null and duplicate values

Filtered out negative or invalid quantities and prices

Created a clean, structured dataset suitable for modeling

2. Feature Engineering

Derived RFM features: Recency, Frequency, Monetary Value

Created customer-level aggregated data

Additional features like total products purchased, average basket size

3. Outlier Detection

Applied Isolation Forest algorithm to detect abnormal customer behavior

Filtered out outliers to improve clustering accuracy

4. Customer Segmentation

Used KMeans clustering based on normalized RFM features

Determined optimal number of clusters using Elbow Method and Silhouette Score

Assigned customers to clusters with unique behavioral traits

5. Cluster Analysis

Visualized distributions of key features (spending, frequency, quantity) across clusters

Labeled clusters based on inferred personas (e.g., High-Value, Loyal, At-Risk)

6. Best-Selling Product Analysis

Aggregated purchase data per cluster

Identified top 10 best-selling products for each cluster

7. Product Recommendation System

For each customer, recommended 3 products from their cluster’s top-selling list that they haven't purchased

Personalized, cluster-aware suggestions
