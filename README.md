# Task-8
Task 8 AL &amp; ML Internship By Elevate Labs

Tools : sklearn, pandas, matplotlib, seaborn
Datset : Mall Customer Dataset

Step 1: Load and Visualize Dataset
The Mall Customer dataset was first loaded using pandas for analysis. Unnecessary columns like CustomerID were dropped, and the categorical Gender column was encoded numerically to make it suitable for machine learning models. All features were then standardized using StandardScaler to ensure that differences in units or scales wouldn’t skew the clustering process. Finally, Principal Component Analysis (PCA) was applied to reduce the data to two dimensions, allowing us to plot a 2D scatter plot and gain a basic visual understanding of how the customers are distributed.

Step 2: Fit K-Means and Assign Cluster Labels
The K-Means clustering algorithm was applied to the scaled dataset with an initial choice of n_clusters=5. The algorithm grouped the customers into five clusters by minimizing the within-cluster variance. After training the model, it assigned a cluster label to each customer, indicating which group they belong to based on their spending habits and demographic traits. These labels were then added back into the original DataFrame for further use and visualization.

Step 3: Use the Elbow Method to Find Optimal K
To determine the optimal number of clusters, the Elbow Method was used. This involved running K-Means for a range of cluster counts (from 1 to 10) and recording the inertia (sum of squared distances between samples and their closest cluster center) for each. A plot of the number of clusters against inertia helped identify the "elbow" point—where the rate of decrease sharply slows—indicating the most appropriate number of clusters to use. This step is crucial to avoid underfitting or overfitting the clustering model.

Step 4: Visualize Clusters with Color-Coding
After determining the number of clusters, the dataset was again projected into two dimensions using PCA to maintain consistency in visualization. A scatter plot was created using seaborn, where each point represented a customer and was colored according to its assigned cluster. This visual representation made it easy to see how well-separated the clusters were and to identify any overlapping or outlying points, providing intuitive insight into the customer segments.

Step 5: Evaluate Clustering Using Silhouette Score
Finally, the quality of the clustering was evaluated using the Silhouette Score, which measures how similar each point is to its own cluster compared to other clusters. This score ranges from -1 to 1, with higher values indicating well-defined, non-overlapping clusters. The score was computed using the scaled data and the cluster labels produced by the K-Means model. A good Silhouette Score confirmed that the clustering captured meaningful customer segments.

