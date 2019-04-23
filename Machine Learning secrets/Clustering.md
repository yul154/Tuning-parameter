# Clustering
* Customer segmentation: partitioning a customer base into groups of individuals that have similar characteristics
* cluster: a group of data points or objects in a dataset that are similar to other objects in the group, and dissimilar to datapoints in other clusters
* Applications:
  1. exploratory data analysis
  2. summary generation
  3. outlier detection
  4. find dupllicates
* Clustering algorithms
  1. partitioned-based clustering:K-means, k-median, Fuzzy c-means
  2. hierarchical clustering: produces trees of clusters(agglomerative, divisive)
  3. density-based clustering: prduces arbitrary shaped clusters(DBSCAN)
  
# K-means
> group data only unsupervised based on the similarity of customers to each other
* Divides data into k non-overlapping subsets
* objective:-Means tries to minimize the intra-cluster distances and maximize the inter-cluster distances.
## questions
1. how can we find the similarity of samples in clustering
2. how do we measure similarity two points
  * Euclidean distance, Cosine similarity, Average distance
3. How calculate the accuracy: 
  * compare the clusters with th groun truth
  * average of the distances of data points from their cluster centroids can be used as a metric of error 
4. Choosing K
  * finding elbow point
## Process
1. Randomly pick K centroids(randomly pick obervations or create k random points)
2. Finding the closest centroids for each data point,assign each data point to that cluster.
3. Update each cluster center to be the mean for datapoints in its cluste(minimize errors)
4. repeat unitl cetroids are no more change
* local optimal: run the whole process multiple times with different starting conditions

# Hierarchical Clustering
* divisive:you start with all observations in a large cluster and break it down into smaller pieces.
* agglomerative:all observations fall on dividual cluster, and merge them into a same one
## questions
* how merge clusters: 
  1. single-linkage clustering: minimum distance between clusters
  2. complete-linkage:maximum distance between clusters
  3. Averasge-linkage: average distance between clusters
  4. centroids-linkage: distance between cluster centroids
  
# Density-based clustering
* locates regions of high density that are separated from one another by regions of low density
* Density-based clustering algorithms are proper for arbitrary shape clusters.
* parameters
  1. R:determines a specified radius that if it includes enough points within it
  2. M:determines the minimum number of data points we want in a neighborhood to define a cluster.

  
