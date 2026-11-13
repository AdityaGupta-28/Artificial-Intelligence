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


## 5. Dimensionality Reduction
Definition: Dimensionality Reduction is the process of reducing the number of features or dimensions in a dataset while trying to preserve its important information.
What is a dimension?
A dimension generally represents one feature or variable in a dataset.

For example, a customer dataset may contain:
1. Age
2. Income
3. Spending score
4. Number of purchases
5. Number of visits
6. Average order value
This dataset has six dimensions.

If a dataset has 100 features, dimensionality reduction can transform it into a smaller representation.
Why do we need it?
1. Reduces computational cost.
2. Can reduce redundant information.
3. Makes visualization easier.
4. Can help reduce overfitting in some situations.
5. Helps manage datasets with many features.


9. Final Revision: What You Must Remember
Unsupervised Learning

Learning from unlabeled data to discover patterns.

Clustering
- K-Means → Centroids and distance.
- Hierarchical → Agglomerative, divisive and dendrogram.
- DBSCAN → Density, core, border and noise points.
- Elbow Method → Helps select K.

Association Rule Learning
- Support → How frequently items occur together.
- Confidence → How often B occurs when A occurs.
- Lift → Strength of association.
- Apriori → Frequent itemset mining.

Dimensionality Reduction
- PCA → Reduces dimensions.
- PC1 → Maximum variance.
- PC2 → Maximum remaining variance, perpendicular to PC1.
- Explained variance → Information represented by components.



#### Reinforcement Learning – Short Notes
1. What is Reinforcement Learning (RL)?
Definition: Reinforcement Learning is a type of Machine Learning in which an agent learns by interacting with an environment, receiving rewards or penalties, and improving its actions to maximize cumulative rewards.

Example:
- Dog sits after receiving a command → Reward (treat).
- Robot moves towards the target → Positive reward.
- Robot hits an obstacle → Negative reward.
Key Idea: Learn through trial and error.

2. Five Fundamental Components of Reinforcement Learning
Component	Short Definition	Example
Agent	Decision-maker that learns and takes actions.	Robot
Environment	External world in which the agent operates.	Room
State	Current situation of the environment.	Robot's position
Action	Decision or movement performed by the agent.	Move left
Reward	Numerical feedback for an action or outcome.	+10 for reaching target



### Mathematics for AI

We will study six important areas:
1. Linear Algebra
Vectors, matrices, dot products and vector operations.

2. Statistics
Mean, variance, standard deviation and distributions.

3. Probability
Probability, conditional probability and Bayes' theorem.

4. Calculus
Derivatives, gradients and optimization.


5. Similarity and Distance
Euclidean distance, dot product and cosine similarity.


6. Mathematical Optimization
Loss functions, learning rates and gradient descent.


This requires mathematics.
Similarly:
## AI concept      	Mathematics required
Neural Networks	    Linear Algebra, Calculus
Machine Learning	Statistics, Probability
Gradient Descent	Derivatives, Gradients
Embeddings	        Vectors, Dot Product
Semantic Search 	Cosine Similarity
LLMs	            Linear Algebra, Probability
RAG	                 Vector Similarity
Agentic AI	        Probability, Optimization and Statistics