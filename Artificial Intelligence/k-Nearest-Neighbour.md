**Nonparametric**
**Instance-based**: prediction is based on comparison of new point with points in the training set
**lazy:** no explicit training step - defers computation until prediction

- $k$ = the number of nearest neighbours sampled

## Distance metrics
#### Minkowski distance ($L^P$ norm)
$$D(x^{(1)}, x^{(2)}) = \sqrt[P]{ \sum^d_{i=1} |x_{i}^{(1)} - x_{i}^{(2)}|^P }$$
#### Manhattan distance
$$D(x^{(1)}, x^{(2)}) = \sum^d_{i=1} |x_{i}^{(1)} - x_{i}^{(2)}|$$

#### Euclidean distance
$$D(x^{(1)}, x^{(2)}) = \sqrt{ \sum^d_{i=1} |x_{i}^{(1)} - x_{i}^{(2)}|^2 }$$
## Normalisation & Standardisation
### The issue
- Attributes $x = (x_{1}, x_{2},\dots,x_{d})$ may have different ranges
- Eg. if $x_1$ in $[0,2]$ and $x_2$ is in $[0,100]$, $x_2$ will affect the distance more

### Normalisation
	Linearly scale the range of each attribute to be in a specific interval

$$x^{n}_{j\_new} = \frac{x_{j}^{(n)} - min\ x_{j}}{max\ x_{j} - min\ x_{j}}$$
### Standardisation
	Linearly scale each dimension to have 0 mean & variance
