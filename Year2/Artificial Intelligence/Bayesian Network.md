**Curse of dimensionality:** To represent a joint distribution of $d$ binary variables, we need $2^d-1$ terms

**Bayesian Network:** A Directed Acyclic Graph (DAG) where
	**Nodes** represent random variables
	**Edges** represent probabilistic influence

**Core Factorisation Theorem:** If we have $n$ variables $x_i$ , the joint distribution of these variables factorises as:
$$P(x_{1:n}) = P(x_{1},x_{2},\dots,x_{n}) = \prod^n_{i=1} P(x_{i} \mid parents(x_{i}))$$

**Markov property:** Each random variable $X$ is conditionally independent of its non-descendants, given its parents
