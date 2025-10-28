For when $P(n)$ requires more than just $P(n - 1)$

1. **Introduce the predicate:** "We prove P(n) for all $n \in \mathbb{Z}$"
2. **Base cases:** If working with a recursive definition which looks back two steps, will need two bases cases
3. **Inductive step:** Let $n \in \mathbb{N}$ and suppose $P(k)$ for all $k < n$. We will prove $P(n)$.

### Eg. 1
Let $P(n)$ be predicate $F_n < 2^n$

Base case: 
	n = 0:
		$F_0 = 1 < 1 = 2^0$
	n = 1:
		$F_1 = 1 < 2 = 2^1$

Induction step:
Let $n > 2$, and suppose $P(k)$ for all $k > n$
$F_n = F_{n-1} + F_{n-2}$


## Strengthened induction
Used when the original predicate cannot undergo induction.
- **Preworking:** Find $Q(n) \implies P(n)$ that is amenable to induction
- **Proof:** Prove $\forall n.Q(n)$ by induction
- **Deduction:** Deduce $\forall n.P(n)$ by proving $Q(n) \implies P(n)$

