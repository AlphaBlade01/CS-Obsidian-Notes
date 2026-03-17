A decision problem is **decidable** if there is an algorithm that can always provide "Yes" or "No" answers
Decision problems can be formatted as:
- function $\Sigma* \rightarrow \{Yes, No\}$
- subset of $\Sigma*$

**Church's Thesis:** Any decision problem on words, that can be decided by an algorithm, can be decided by a TM
	Turing-decidable = decidable

**primitive recursive:** function that can be computed in a fixed number of loops

## Ackermann Function
	Example of a non-primitive recursive algorithm
**Function:**
$A(0,\ n) = n + 1$
$A(m + 1,\ 0) = A(m,\ 1)$
$A(m+1,\ n+1) = A(m,\ A(m+1, n))$

