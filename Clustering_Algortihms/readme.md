# Clustering algorithms validation and comparison 

## *Introduction*

Clustering is an important Machine Learning Technology work on data without labels. Unlike the data with labels, which we can estimate the values (regression) or classification. For data withoutlabels, we can use clustering to group the different data points, we assume the data points in the same group have similar or same features, data points in the different groups have different features. Here, we’ll use four different algorithms on clustering (K-means nearest, Hierarchial,Density Based Clustering, Gaussian Maximum Model Clustering), optimize the parameters and then comparethree different algorithms on different datasets to find the best performance algorithm on eachdataset. Iris dataset and is used to here. Although the IRIS dataset has labels (target), we willhide them then apply our algorithms to do the clustering. Accuracy and confusion matrix are two candidates to used for compareing performances among three algorithms.

## *Metholody*

#### 1. K-Means Clustering
K-Means Nearest Clustering is the most common and easy cluster method we used in the world. Here, K represents the number of clusters (groups) we want to seperate. First, we randomly place k points, which we called centroids. Then, calculate the distance between the centroids and the data points. Therefore, each data points here have K different distance to k centroids. After that, data points assigned to the K different groups which has the mimum distance to the centroids. After different grousp assigned, we calculate the centers of K different gourps and then move the centroids to K different centers. Then, we repeate the past two steps until centroids cannot be moved.

#### 2. Hierarchial Clustering
Hierarchial clustering is used to group similar objects. Here, each object is viewed as a seperate cluster. Then two closest clusters/datapoints are merged together based on distance. This step will be repeated again and again until all datapoints merged together. Distance in the hierarchial clustering is called Euclidean distance, which measured based on linkage. There are different linkage methods available, which are single-link clustering, complete-link clustering, average-link clustering and Ward’s method clustering. Single-link is to measure the cloest distance between two clusters, it will not be applied in our example here as it is the not in sklearn in python. Complete-link is to measure the farest distance between two clusters; Average-link is to calculate the average distance between two clusters; Ward’s method, we first identify the center points between two clusters and calculate the square distance between the center to each data points, set as D. Then for each cluster, we calculate the distance between the data points to the center within the cluster, set as d. Then we used the sum of square distance between the data points and centers (between= the clusters, D) minus the sum of distance between the data points and centers (within the cluster,d).

#### 3. Gaussian Mixture Model Clustering
Gaussian Mixture Model Clustering is a clustering algorithm which assumes each cluster has their own statistical distribution. Unlike other clustering methods, GMM uses the soft clustering approach to cluster the data points. First, it initializes a Gaussian Distribution with initial parameter (μ, ￿²). Then, it soft-clustering the data points on a soft step based on membership, which is the PDF of normal distribution. Then, re-estimate the parameters by using Expectation- Maximization algorithm.

#### 4. Density – Based Clustering (DBSCAN)
Density-Based Clustering is different from the algortihms above, not all points will be in the clusters. Two important parameters in DBSCAN defines how to formulate a cluster. Minumum numbers of points (m) and maximum distance between two samples (d). For any point we started, it needs to find m points within d distance. If there are m points within d distance, this point will be identified as core point; if not this point will be indenfied as noise points unless find another core point within d distance.


## References
1. https://www.displayr.com/what-is-hierarchical-clustering/
2. https://towardsdatascience.com/the-5-clustering-algorithms-data-scientists-need-to-knowa36d136ef68
3. https://www.analyticsvidhya.com/blog/2019/10/gaussian-mixture-models-clustering/
4. https://www.dummies.com/programming/big-data/data-science/how-to-create-anunsupervised-
learning-model-with-dbscan/
5. https://scikit-learn.org/stable/modules/clustering.html#clustering-performance-evaluation
