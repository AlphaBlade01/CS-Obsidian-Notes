 ## Propositional logic
[[Propositional logic]]
Each connective has at least 1 introduction and 1 elimination

**Introduction & Elimination rules for $\forall$ and $\exists$** 
![[Pasted image 20251118132117.png]]

### Types of variables
#### Bound variables
	A variable that is bound by a quantifier
- $\forall x.even(x)\ \vee\ odd(x)$
- The variable $x$ is bound to quantifier $\forall$
- Renaming bound variable doesn't change anything
#### Free variable
	Variable not bound by a quantifier
- $\forall y.x \le y$
- $y$ is bound and $x$ is free
- changing the free variable changes the meaning of the formula

### Inference rules
#### For all elimination
	replace x with t which satisfies the predicate
- $\forall x.P \rightarrow P[x \t]$ 
#### For all introduction
	If we have prove P for an arbitrary/general/representative variable
- Condition: $y$ must not be free in any not-yet-discharged hypothesis
	- **Not yet discharged hypothesis:** one that we started with or assumed below
- $P[x\y] \rightarrow \forall x.P$ 
#### Exists introduction
	Used if predicate P proved for an element of the domain
- $P[x\t] \rightarrow \exists x.P$
#### Exists elimination
	Can conclude variable if exists in predicate P