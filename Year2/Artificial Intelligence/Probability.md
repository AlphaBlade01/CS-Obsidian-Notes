**Random variable:** A variable which maps an outcome to a number

$$P(A|B) = \frac{P(A\cap B)}{P(B)}$$
**Bayes rule:**
	If $P(A) > 0$
$$P(B|A) = \frac{P(A|B)P(B)}{P(A)}$$
## Independence
- If events $A$ and $B$ are independent: $P(A\cap B) = P(A)P(B)$
### Conditional independence
	Means A and B are independent once C is known
- $A\ \bot\ B\ |\ C$

## Random variable
	Variable which maps an outcome to a number
- Random variable $X$ maps outcome $w\in \Omega$ to a real number $X: \Omega \rightarrow \mathbb{R}$
	$\Omega$ - Total sample space of outcomes
### Probability mass function
	Probability measure of event corresponding to x
- $\sum_{x\in X(\Omega)}P_{X}(x)=1$

- **Bernoulli distribution:** Discrete distribution with two possible outcomes
	Success = 1 & Failure = 0
- **Binomial random variable:** Sum of Bernoulli variables 
	$k$ heads in $n$ trials gives each trial a probability $p^k(1-p)^{n-k}$
## Likelihood
	measures the probability of observing the dataset given a parameter
- Data fixed, parameter varies
For a fixed value of $\theta$, the joint PMF is:
	$P(X=x\mid \theta) = P(x\mid\theta) = \prod^n_{i=1} P(X_{i}=x_{i}\mid\theta)$
Likelihood function:
	$L(\theta\mid x) = P(x \mid \theta)$ 
