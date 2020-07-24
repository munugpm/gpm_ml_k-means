# gpm_ml_k-means
https://realpython.com/k-means-clustering-python/

What Is Clustering?

  Overview
  
  Partitional, Hierarchical, Density-Based Clustering
How to Perform K-Means Clustering in Python
Understanding the K-Means Algorithm
K-means Clustering Code in Python
Choosing the Appropriate Number of Clusters
Evaluating Clustering Performance Using Advanced Techniques
How to Build a K-Means Clustering Pipeline in Python
Building a K-Means Clustering Pipeline
Tuning a K-Means Clustering Pipeline
Conclusion



Meaningfulness
Meaningful clusters expand domain knowledge. For example, in the medical field, researchers applied clustering to gene expression experiments.
The clustering results identified groups of patients who respond differently to medical treatments.

Usefulness
Useful clusters, on the other hand, serve as an intermediate step in a data pipeline. For example, businesses use clustering for customer 
segmentation. The clustering results segment customers into groups with similar purchase histories,
which businesses can then use to create targeted advertising campaigns.

Selecting an appropriate clustering algorithm for your dataset is often difficult due to the number of choices available.
Some important factors that affect this decision include the characteristics of the clusters, the features of the dataset,
the number of outliers, and the number of data objects.

Partitional Clustering
Partitional clustering divides data objects into nonoverlapping groups. i.e. no object can be a member of more than one cluster, 
and every cluster must have at least one object.

These techniques require the user to specify the number of clusters, indicated by the variable k. 
Many partitional clustering algorithms work through an iterative process to assign subsets of data points into k clusters.
Two examples of partitional clustering algorithms are k-means and k-medoids.
These algorithms are both nondeterministic, meaning they could produce different results from two separate runs even if the runs were based on the same input.

Partitional clustering methods have several strengths:

They work well when clusters have a spherical shape.
They’re scalable with respect to algorithm complexity.
They also have several weaknesses:

They’re not well suited for clusters with complex shapes and different sizes.
They break down when used with clusters of different densities.

Hierarchical Clustering
This is implemented approach by either a bottom-up or a top-down building a hierarchy :
Agglomerative clustering is the bottom-up approach. It merges the two points that are the most similar until all points have been merged into a single cluster.
Divisive clustering is the top-down approach. It starts with all points as one cluster and splits the least similar clusters at each step until only single data points remain.

These methods produce a tree-based hierarchy of points called a dendrogram. Similar to partitional clustering, in hierarchical clustering 
the number of clusters (k) is often predetermined by the user. 
Clusters are assigned by cutting the dendrogram at a specified depth that results in k groups of smaller dendrograms.

Unlike many partitional clustering techniques, hierarchical clustering is a deterministic process, 
meaning cluster assignments won’t change when you run an algorithm twice on the same input data.

The strengths of hierarchical clustering methods include the following:

They often reveal the finer details about the relationships between data objects.
They provide an interpretable dendrogram.
The weaknesses of hierarchical clustering methods include the following:

They’re computationally expensive with respect to algorithm complexity.
They’re sensitive to noise and outliers.

Density-Based Clustering
Density-based clustering determines cluster assignments based on the density of data points in a region. 
Clusters are assigned where there are high densities of data points separated by low-density regions.

Unlike the other clustering categories, this approach doesn’t require the user to specify the number of clusters. 
Instead, there is a distance-based parameter that acts as a tunable threshold. This threshold determines how close points must be to be considered a cluster member.

Examples of density-based clustering algorithms include Density-Based Spatial Clustering of Applications with Noise, 
or DBSCAN, and Ordering Points To Identify the Clustering Structure, or OPTICS.

The strengths of density-based clustering methods include the following:

They excel at identifying clusters of nonspherical shapes.
They’re resistant to outliers.
The weaknesses of density-based clustering methods include the following:

They aren’t well suited for clustering in high-dimensional spaces.
They have trouble identifying clusters of varying densities.
