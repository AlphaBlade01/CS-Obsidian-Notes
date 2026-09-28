**Nonparametric**
**Instance-based**: prediction is based on comparison of new point with points in the training set
**lazy:** no explicit training step - defers computation until prediction

$k$ = the number of nearest neighbours sampled

## Distance metrics
#### Minkowski distance ($L^P$ norm)
$$D(x^{(1)}, x^{(2)}) = \sqrt[P]{ \sum^d_{i=1} |x_{i}^{(1)} - x_{i}^{(2)}|^P }$$
#### Manhattan distance
$$D(x^{(1)}, x^{(2)}) = \sum^d_{i=1} |x_{i}^{(1)} - x_{i}^{(2)}|$$

#### Euclidean distance ($L^2$ distance)
$$D(x^{(1)}, x^{(2)}) = \sqrt{ \sum^d_{i=1} |x_{i}^{(1)} - x_{i}^{(2)}|^2 }$$
## Choosing K
**Overfitting:** When the model is more complex than required
**Underfitting:** When the model isn't complex enough

- Small k $\rightarrow$ small neighbourhood $\rightarrow$ high complexity borders $\rightarrow$ may overfit
- Large k $\rightarrow$ large neighbourhood $\rightarrow$ low complexity/straighter borders $\rightarrow$ may underfit

## Normalisation & Standardisation
### The issue
- Attributes $x = (x_{1}, x_{2},\dots,x_{d})$ may have different ranges
- Eg. if $x_1$ attributes span $[0,2]$ and $x_2$ attributes span $[0,100]$, $x_2$ will tend to affect the distance more
- This means small proportional changes in $x_2$ will be given more importance over large proportional changes in $x_1$ 
### Normalisation
	Linearly scale the range of each attribute to be in a specific interval
- Each attribute will contribute to the distance equally
$$x^{n}_{j\_new} = \frac{x_{j}^{(n)} - min\ x_{j}}{max\ x_{j} - min\ x_{j}}$$
### Standardisation
	Linearly scale each dimension to have 0 mean & 1 variance / standard deviation

For each point:
1. Subtract the average of all points in its category
	Shifts the data so new centre is 0
2. Divide by standard deviation
	Stretches or squashes data so average distance from mean is 1
$$x^{(n)}_{j\_new} = \frac{x^{(n)}_j - \mu_j}{\sigma_j}$$
> $\mu_j$ = mean of all points representing attribute $j$
> $\sigma_j$ = standard deviation of all points representing attribute $j$ 

## Final algorithm
### Inputs
- neighbours size $k>0$ 
- distance metric $D$
- training set $\{\ (x^{(n)}, y^{(n)}): n = 1,2,\dots,N\ \}$ 
- new unlabelled data $x^{(j)}$
### Algorithm
1. Normalise/standardise $x^{(j)} \rightarrow x^{(j)}_{new}$ by normalising each of its attributes
2. For $n=1,2,\dots,N$ 
	1. Normalise/standardise $x^{(n)} \rightarrow x^{(n)}_{new}$  
	2. Calculate distance $D(x^{(j)}_{new},\ x^{(n)}_{new})$ 
	3. Select $k$ training samples closest to $x^{(j)}_{new}$ 
3. Return:
	 **Classification:** the majority vote of labels from $k$ samples
	 **Regression:** the mean of y values of $k$ samples

