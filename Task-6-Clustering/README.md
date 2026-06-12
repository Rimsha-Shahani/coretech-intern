# Task 6: Unsupervised Learning – Clustering

## Project Overview

This project applies Unsupervised Machine Learning techniques to group CoreTech clients based on their characteristics. K-Means Clustering and Hierarchical Clustering were used to identify customer segments and generate business insights.

---

## Dataset Description

The dataset contains 50 client records with the following features:

| Feature       | Description                      |
| ------------- | -------------------------------- |
| ClientID      | Unique customer identifier       |
| Age           | Customer age                     |
| AnnualIncome  | Customer annual income           |
| SpendingScore | Customer spending behavior score |

Dataset Size:

* Total Records: 50
* Total Features: 4

---

## Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the dataset using Pandas.
2. Checked dataset information using `df.info()`.
3. Verified missing values using `df.isnull().sum()`.
4. Generated descriptive statistics using `df.describe()`.
5. Selected numerical features for clustering.
6. Applied StandardScaler to normalize the data.

Result:

* No missing values were found.
* Data was successfully standardized before clustering.

---

## Elbow Method

The Elbow Method was used to determine the optimal number of clusters.

The WCSS (Within Cluster Sum of Squares) values were calculated for K values from 1 to 10.

Observation:

* The elbow point was observed at **K = 3**.
* Therefore, 3 clusters were selected for K-Means Clustering.

---

## K-Means Clustering

K-Means Clustering was applied with:

* Number of Clusters = 3
* Random State = 42

A new column named `KMeans_Cluster` was added to the dataset containing cluster assignments.

---

## Cluster Visualization

A scatter plot was generated to visualize the clusters formed by K-Means Clustering.

The visualization showed three distinct groups of customers based on their income and spending behavior.

---

## Cluster Analysis

### Cluster 0

* High annual income
* High spending score
* Premium customers

### Cluster 1

* Medium annual income
* Moderate spending score
* Regular customers

### Cluster 2

* Lower annual income
* Lower spending score
* Budget-conscious customers

---

## Silhouette Score

The Silhouette Score was calculated to evaluate clustering quality.

A positive silhouette score indicated that the customer groups were reasonably separated and well clustered.

---

## Hierarchical Clustering

Agglomerative Hierarchical Clustering was applied with 3 clusters.

A separate visualization was generated and compared with the K-Means results.

---

## Comparison of Clustering Methods

| Method                  | Observation                                                |
| ----------------------- | ---------------------------------------------------------- |
| K-Means                 | Fast, simple, and efficient                                |
| Hierarchical Clustering | Useful for understanding relationships between data points |

---

## Business Insights

### Premium Customers

* Offer VIP memberships.
* Provide exclusive discounts and premium services.

### Regular Customers

* Introduce loyalty reward programs.
* Encourage repeat purchases through personalized offers.

### Budget Customers

* Provide promotional discounts.
* Offer special deals to increase engagement.

---

## Conclusion

Customer segmentation was successfully performed using K-Means and Hierarchical Clustering techniques.

Three customer groups were identified based on age, annual income, and spending score. These insights can help businesses develop targeted marketing strategies, improve customer retention, and increase overall customer satisfaction.

---

## Files Included

* coretech_clients.csv
* clustered_clients.csv
* clustering.ipynb
* README.md

