# Retail_Customer_Analysis_Recommendation_System

## 📘 Project Owerview
This project focuses on analyzing retail customer purchase behavior, segmenting customers using clustering techniques, and generating personalized product recommendations. The dataset used comes from a real-world retail transaction log and contains information about invoices, products, and customer purchases.

## 🔁 Key Processes
1. Data Cleaning

To ensure the quality and reliability of insights, thorough data preprocessing was performed. Missing values in key columns like CustomerID were removed to avoid incomplete records. Duplicate entries were dropped to prevent skewed analysis. Cancelled transactions (invoices starting with 'C') were excluded, as they don't reflect actual purchases. StockCode anomalies such as generic codes were filtered out. The Description column was standardized by removing whitespace and special characters. Zero-priced items were also removed to focus on valid purchases. Lastly, outliers were detected using Isolation Forest, ensuring clean and robust input for downstream clustering and recommendation models.

2. Feature Engineering

To gain deeper insights into customer behavior, RFM (Recency, Frequency, Monetary) features were obtained:

Recency (R): Measures how recently a customer made a purchase. Customers with lower recency values are more engaged.

Frequency (F): Counts how often a customer made purchases. Frequent buyers are considered more loyal.

Monetary (M): Calculates the total amount spent by each customer, helping identify high-value individuals.

These three features form the foundation for segmentation. RFM provides a compact yet powerful summary of customer behavior, making it ideal for clustering and building tailored marketing strategies or recommendations.

Beyond RFM, additional features were created to capture broader customer behavior and context:

Product Diversity: Number of unique products purchased by each customer, reflecting variety-seeking behavior and product interest.

Behavioral Features: Included average basket size, average spend per transaction, and purchase patterns to profile buying intensity and habits.

Geographic Features: Country-based segmentation helped identify regional preferences and customer distributions.

Cancellation Insights: Count and percentage of cancelled orders per customer were tracked to flag dissatisfaction or unusual activity.

Seasonality & Trends: Purchase activity was analyzed over time to uncover seasonal buying behaviors and peak transaction periods.

3. Outlier Detection

Applied Isolation Forest algorithm to detect abnormal customer behavior.

Filtered out outliers to improve clustering accuracy.

4. Dimensionallity Reduction

Performing Dimensionallity reduction with Principal Component Analysis(PCA) by reducing columns to identify most important features.

5.Customer Segmentation

📊 K-Means Clustering
To segment customers based on their behavior, K-Means Clustering was applied to the engineered feature set. This unsupervised learning method groups customers into clusters with similar characteristics, enabling targeted marketing and personalized strategies.

🔍 Determining the Optimal Number of Clusters:

Choosing the right number of clusters is crucial for meaningful segmentation. Two methods were used:

Elbow Method: Plots the Within-Cluster Sum of Squares (WCSS) against the number of clusters to identify the point where adding more clusters yields diminishing returns.

Silhouette Method: Measures how well-separated the clusters are. Higher silhouette scores indicate well-defined clusters.

Visualized distributions of key features (spending, frequency, quantity) across clusters through histograms.

Based on visuallization, drawing out observations.

6. Best-Selling Product Analysis

Aggregated purchase data per cluster.

Identified top 10 best-selling products for each cluster.

7. Product Recommendation System

For each customer, recommended 3 products from their cluster’s top-selling list that they haven't purchased.

Personalized, cluster-aware suggestions.
