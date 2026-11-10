### 1 Unsupervised Learning
Definition: Unsupervised Learning is a type of Machine Learning in which a model learns patterns, relationships, and structures from unlabeled data without being provided with predefined correct outputs.

In simple words, the machine receives data and discovers meaningful patterns on its own.
Important algorithms - K-Means, DBSCAN, PCA

## 2 Major Techniques of Unsupervised Learning
## 3 Clustering -
Definition: Clustering is an unsupervised learning technique that divides a dataset into groups called clusters, where data points within the same cluster are more similar to each other than to points in other clusters.
Example
A shopping company wants to group customers based on income and spending habits.

The algorithm may discover three clusters:
- Cluster 1: Low-income, low-spending customers.
- Cluster 2: Medium-income, medium-spending customers.
- Cluster 3: High-income, high-spending customers.

### 3.1 K-Means Clustering
Definition: K-Means is a centroid-based clustering algorithm that divides a dataset into K clusters by assigning each data point to the nearest centroid and repeatedly updating the centroids.
Important terminology
Term	          Definition
K	            Number of clusters
Cluster	        Group of similar data points
Centroid	    Center point of a cluster
Distance	    Measurement of how far two points are
Inertia (WCSS)	Sum of squared distances between points and their assigned centroids

How to select K? – Elbow Method
Definition: The Elbow Method is a technique used to estimate the appropriate number of clusters by observing how inertia changes as K increases


## 4. Association Rule Learning
Definition: Association Rule Learning is an unsupervised learning technique that discovers relationships between items that frequently occur together in a dataset.

Example: A supermarket analyzes thousands of customer transactions.

It discovers:
- Customers buying bread often buy butter.
- Customers buying milk often buy cereal.

This is called Market Basket Analysis.

Three important measures
These are especially important for technical interviews and MCQs.

1. Support
Support tells us how frequently a group of items occurs in all transactions.
Support(A -> B)=Count(A U B)/{Total Transactions}

Example:
- Total transactions = 100.
- Transactions containing bread and butter = 30.
Support = 30/100 = 0.30 = 30%.

2. Confidence
Confidence tells us how often B is purchased when A is purchased.

Confidence(A -> B)=Support(A U B)/Support(A)

Example:
- Transactions containing bread = 50.
- Transactions containing bread and butter = 30.
Confidence = 30/50 = 60%.
Interpretation: 60% of customers who bought bread also bought butter.


