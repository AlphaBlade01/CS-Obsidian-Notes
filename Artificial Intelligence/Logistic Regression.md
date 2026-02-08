	Used for classification problems
This method is **linear** and **parametric** ([[Machine Learning]])
#### Process:
1. Model formulation
2. Cost function
3. Learning algorithm by gradient descent

## Sigmoid function
	Probability function between 0 & 1

$$\sigma(x) = \frac{1}{1 + e^{-x}}$$
- Smoothed version of the step function
- Continuous
- Differentiable
	Allows it to be optimised during training

## Model (general case)
	Hypothesis function for a logistic regression model
If $x$ has $d$ attributes, we have:
$$h(x;w) = \sigma(w_0 + w_1x + \dots + w_dx_d) = \frac{1}{1 + e^{-(w^Tx)}}$$
> Note: $w^Tx$ is a single number
> Output represents the probability of the label being 1, denoted: $P(y=1|x;w)$ 

**Decision boundary:** Set of all possible inputs that result in sigmoid outputting 0.5

## Cost function
Types covered in [[Linear Regression]]

**MSE** (Mean Squared Error) doesn't work using the sigmoid function:
- function becomes non-convex 
- gradient descent doesn't work well on non-convex functions
	- **vanishing gradients** results in little progress over many iterations
	- **local minimums** may appear which tricks the algorithm into thinking it has completed
### Logistic cost function
	Also called cross-entropy loss
For each pair of training data $(x,y)$, the function $cost(h(x;w),\ y)$ is defined as:
1. if $y=1$ : $-log(h(x;w))$ 
2. if $y=0$ : $-log(1 - h(x;w))$ 

Overall cost function for all pairs in training set:
$$g(w) = \frac{1}{N}\sum^N_{n=1} cost(\ h(x^{(n)};w),\ y^{(n)})$$
**Total cost function** in one line:
$$g(w) = -\frac{1}{N}\sum^N_{n=1}\{\quad \boxed{y^{(n)}}\cdot \log(h(x^{(n)};w))\quad +\quad \boxed{(1-y^{(n)})}\cdot \log(1 - h(x^{(n)}; w))\quad \}$$
> This works because $y^{(n)}$ is always either 0 or 1

**Gradient vector** from deriving the cost function:
$$\Delta g(w) = (h(x^{(n)};w) - y^{(n)}) \cdot x^{(n)}$$
