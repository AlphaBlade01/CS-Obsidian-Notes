**Regression:** Learning a function which captures the trend between input & output
	output being continuous
This model is **linear** and **parametric** ([[Machine Learning]])
## Univariate linear regression
	One input attribute to regression function

$$y = f(x; w_0, w_1) = w_1x + w_0$$
$w_0, w_1$ = free parameters that determine the "best" line
$x$ = input / independent variable
$y$ = output / dependent variable

## Loss function
	Cost function / Error function
Figures out how good/bad the line of best fit is.
	Loss is the mismatch (distance) between model's output $f(x)$ and actual target $y$
### Types
**Absolute value loss:** $L1 = |f(x) - y|$
**Mean squared error loss:** $L2 = (f(x) - y)^2$
	**Empirical loss:** Average loss across dataset$$\frac{1}{N} \sum^N_{n=1} (f(x^{(n)}; w_0, w_1) - y^{(n)})^2$$
**0/1 loss:** $L_{0/1} = 0$ if $f(x) = y$, else $1$ 

## Gradient Descent
	A general strategy to minimise cost functions
Process:
1. Start at a random point, eg. $w_0 = 0,\ w_1 = 0$ 
2. Repeat until no changes:
	Update $w_0,\ w_1$ by taking a smell step in the **direction of steepest decent of cost**
	$\vec{w} := \vec{w} - a\Delta g(\vec{w})$ 
3. Return $w_0,\ w_1$ 

> $\Delta g(\vec{w})$ is a vector of partial derivatives which is iteratively used until it results in a ~0 step size
> $\Delta g(\vec{w}) = 2(\vec{w}^T x^{(n)} - y^{(n)})x^{(n)}$ 
