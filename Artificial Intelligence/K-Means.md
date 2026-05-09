	Iterative, non-deterministic, greedy descent algorithm

- Clustering as an optimisation problem
- Find clustering structure $C$ of $K$ clusters that minimises following objective:
	- **Minimise** $WCSS(C)$
	- $$WCSS(C) = \sum_{c \in C} \sum_{e\in C} d_{Euc} (e, centroid(c))^2$$
- Clusters are non-overlapping & all elements included in one cluster

### K-Means Algorithm
**Input:**
- $K$ : Number of clusters
- $N$ examples: $(x^{(1)}, \dots, x^{(n)})$ 

1. Select $K$ random examples and assign them as centroids
2. Repeat until centroids don't change:
	1. **Assignment:** Assign each observation to its closest cluster centroid
	2. **Refitting:** Recalculate average cluster centroid

## K-Means++
	Choosing better initial centroids
**Problem:** Nonoptimal initial centroids may result in bad results
### Algorithm
1. Choose first centroid $c_1$ at random
2. Repeat until $K$ centroids found:
	1. Choose random point $p$
	2. Calculate distance between point $p$ & nearest centroid $c_k$: $d(p, c_k)^2$
	3. Assign $p$ as next centroid with probability proportional to $d(p, c_k)^2$ 
	(Data point furthest from $p$ is highly likely to be picked)
3. Run **K-Means** on initial centroids
### Cons
- Heuristic concept
- Not easy to identify elbow

## Choosing K
- **Conventional approach:** Use prior domain knowledge
- **Data-based approach:** Elbow method
### Elbow method
1. Run K-Means repeatedly for increasing $K$
2. Evaluate $WCSS$ of obtained clustering structure in each run
3. Plot $WCSS(C)$ as function of $K$ 
4. Optimal $K$ lies at "elbow" (inflection point) of graph

## Limitations
Problems arise:
- When outliers present: increases WCSS & influences clusters that are found
- With clusters of different sizes, may attempt to make spherical clusters of equal sizes
- When clusters of varying densities 
- When clusters are of non-globular shape