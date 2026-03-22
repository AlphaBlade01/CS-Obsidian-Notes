### Objectives
- **High intra-cluster similarity:** Distance between objects in same cluster are minimised
- **Low inter-cluster similarity:** Distance between clusters are maximised
## Agglomerative Hierarchical Clustering
1. Start with each data point in its own individual cluster
2. Find two clusters that have the highest intra-cluster similarity (smallest distance)
3. Merge two clusters into a single cluster
4. Repeat until all points are merged into a cluster

**dendrogram:** diagram representing all merges in the order they happened
## Inputs
### Distance matrix
Given N observations $(x^{(1)}, x^{(2)},\dots, x^{(N)})$ of feature vectors:
- Distance matrix $D$ is a $N\times N$ matrix with each value being $d(x_i,x_j)$ in row $i$ and column $j$ 
- $d(x_{i}, x_{j})$ is a given distance measure between two vectors
- $D_{i,j} = D_{j,i}$ , matrix is symmetric diagonally
- $D_{i,i} = 0$, all diagonal entries are 0
### Inter-Cluster Dissimilarity Metrics
#### Single Linkage (SL)
- Shortest distance between a member of one cluster and a member of another cluster
- $d_{SL} (C_{1},C_{2}) = \min\ d(i,j)$
- 