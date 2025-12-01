# Customer Segmentation with K-Means

![University](https://img.shields.io/badge/University-University%20of%20Tehran-red)
![Course](https://img.shields.io/badge/Course-Machine%20Learning-blue)
![Library](https://img.shields.io/badge/Library-Scikit--Learn-orange)

This project applies the **K-Means Clustering** algorithm to segment customers of a shopping mall based on their spending behavior and income.

## Project Overview
Using the "Mall Customers" dataset, we aim to identify distinct groups of shoppers. This insight allows businesses to target specific groups with tailored marketing campaigns.

**Techniques Used:**
* **Data Visualization:** 3D Scatter plots and Pairplots to understand data distribution.
* **Elbow Method:** A heuristic used in determining the number of clusters in a data set.
* **Centroid Visualization:** Plotting cluster centers to interpret the "average customer" in each segment.

## Files
* `KMeans_Clustering_Mall_Customers.ipynb`: The main analysis notebook.
* `Mall_Customers.csv`: The dataset containing CustomerID, Gender, Age, Annual Income, and Spending Score.

## Key Results
Using the Elbow Method, we determined that the optimal number of clusters is **k=5**. The customers were segmented into groups such as:
1.  High Income, Low Spending
2.  High Income, High Spending (Target Group)
3.  Average Income, Average Spending
4.  Low Income, High Spending
5.  Low Income, Low Spending

## How to run
1.  Ensure `Mall_Customers.csv` is in the same directory as the notebook.
2.  Run the notebook to generate the clusters and view the visualizations.