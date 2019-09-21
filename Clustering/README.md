## Clustering 
Clustering is basically a type of unsupervised learning method. <br/>
Clustering is the task of dividing the data points into a number of groups such that data points in the same groups are more similar to other data points in the same group and dissimilar to the data points in other groups.

### TYPES OF CLUSTERING

## K-Means Clustering
1.To begin, we first select a number of classes/groups to use and randomly initialize their respective center points. <br/>
2.Each data point is classified by computing the distance between that point and each group center, and then classifying the point to be in the group whose center is closest to it. <br/>
3.Based on these classified points, we recompute the group center by taking the mean of all the vectors in the group. <br/>
4.Repeat these steps for a set number of iterations or until the group centers don’t change much between iterations.

## Mean-Shift Clustering 
1.Mean shift clustering is a sliding-window-based algorithm that attempts to find dense areas of data points. <br/>
2.It is a centroid-based algorithm meaning that the goal is to locate the center points of each group/class. <br/>
3.It works by updating candidates for center points to be the mean of the points within the sliding-window. <br/>
4.Duplicates centroids are filtered in post processing stage.

## Hierarchical Clustering
1.Consider each data point as a cluster. <br/>
2.Compute the distance matrix between each input data points. <br/>
3.Repeat : <br/>
- Merge two closest clusters.
- Update the distance matrix. 
4.Repeat step 3 until one single cluster remains.

Number of clusters is chosen by **Dendrogram**.
Whenever two clusters are merged, we will join them in dendrogram and the height of the join will be the distance between these points.

### Types of Hierarchical Clustering
1.Agglomerative hierarchical clustering <br/>
2.Divisive Hierarchical clustering

## Agglomerative Hierarchical Clustering 
1.Assign each point to an individual cluster in this technique. Suppose there are 4 data points. We will assign each of these points to a cluster and hence will have 4 clusters in the beginning. <br/>
2.Then, at each iteration, we merge the closest pair of clusters and repeat this step until only a single cluster is left. 

## Divisive Hierarchical Clustering
1.Divisive hierarchical clustering works in the opposite way. Instead of starting with n clusters, we start with a single cluster and assign all the points to that cluster. <br/>
2.Now, at each iteration, we split the farthest point in the cluster and repeat this process until each cluster only contains a single point.

## Density-Based Clustering
It based on density of the data points and it does not require the number of the clusters in advance. <br/>
2 Types : <br/>
1.DBSCAN  - Density-based spatial clustering of applications with noise <br/>
2.OPTICS  - Ordering points to identify the clustering structure

## DBSCAN
2 parameters :  <br/>
1.Eps - Maximum radius of the neighbourhood <br/>
2.Minpts - Minimum number of points in the Eps- neighbourhood of the point

3 points : <br/>
**Core point** - A point is a core point if it has a more than a specified points (Minpts) within Eps. <br/>
**Border point** - Border point has fewer than Minpts within Eps but is in neighbourhood of the core point. <br/>
**Noise point** - A noise point is a any point that is not a core point and border point.

1. Find all the neighbour points within eps and identify the core points or visited with more than MinPts neighbors. <br/>
2. For each core point if it is not already assigned to a cluster, create a new cluster. <br/>
3. Find recursively all its density connected points and assign them to the same cluster as the core point. <br/>
4. Iterate through the remaining unvisited points in the dataset. Those points that do not belong to any cluster are noise. 

## OPTICS
Optics is an algorithm for finding density-based clusters in spatial data like dbscan but it keeps cluster hierarchy for a variable neighbourhood radius. <br/>
It adds two more terms to the concepts of DBSCAN clustering. They are:- <br/>
1.Core Distance <br/>
2.Reachability Distance

**Core Distance**: It is the minimum value of radius required to classify a given point as a core point. If the given point is not a Core point, then it’s Core Distance is undefined. <br/>
**Reachability Distance**: It is defined with respect to another data point. The Reachability distance between a point p and q is the maximum of the Core Distance of p and the Euclidean Distance between p and q.

DBSCAN works well in the constant amount of the density among the data points. <br/>
OPTICS works in varying density regions also. <br/>
Density based clustering algorithms will work in any shapes including non spherical ones and it can be able to identify the noise data.<br/>
But, It fails if there are no density drops between clusters.

## Spectral Clustering
1.Construct a similarity graph <br/>
2.Determine the Adjacency matrix W, Degree matrix D and the Laplacian matrix L <br/>
3.Compute the eigenvectors of the matrix L <br/>
4.Using the second smallest eigenvector as input, train a k-means model and use it to classify the data.

## Affinity propagation Clustering
Affinity Propagation does not require to specify the number of clusters. <br/>
Important concepts: <br/>
1. Similarity Matrix (c) <br/>
2. Responsibility Matrix (r) <br/>
3. Availability Matrix (a) <br/>
4. Criterion Matrix (c)


## References
https://scikit-learn.org/stable/modules/clustering.html <br/>
https://towardsdatascience.com/the-5-clustering-algorithms-data-scientists-need-to-know-a36d136ef68 <br/>
http://madhugnadig.com/articles/machine-learning/2017/03/04/implementing-k-means-clustering-from-scratch-in-python.html <br/>
https://towardsdatascience.com/unsupervised-machine-learning-spectral-clustering-algorithm-implemented-from-scratch-in-python-205c87271045 <br/>
https://www.analyticsvidhya.com/blog/2019/05/beginners-guide-hierarchical-clustering/ <br/>
https://towardsdatascience.com/unsupervised-machine-learning-affinity-propagation-algorithm-explained-d1fef85f22c8 <br/>
https://www.ritchievink.com/blog/2018/05/18/algorithm-breakdown-affinity-propagation/ <br/>
https://pythonprogramming.net/mean-shift-from-scratch-python-machine-learning-tutorial/ <br/>
https://github.com/choffstein/dbscan/blob/master/dbscan/dbscan.py































