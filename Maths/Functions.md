A function $f:X \rightarrow Y$  takes an element $x \in X$ to a precise singular choice of element $f(x) \in Y$
- **Total:** for all $x \in X$, there is some $y \in Y$ with $x\ f\ y$ 
- **Single-valued:** for all $x \in X$, there is at most one $y \in Y$ with $x\ f\ y$

<hr>

- Always has **domain** $X$ and **codomain** $Y$ 
	- **Domain:** Possible inputs
	- **Codomains:** Possible outputs
- Written as:
	- $x \mapsto y$ \[Some predicate of x & y]
	- $x \mapsto$ \[Some expression involving x]
	- $f(x) = [\dots]$ 

### Definitions
- For $x \in X$, $f(x)$ is the **image** of x
- The **image** (or **range**) of $f$ is $f[X] = \{ f(x)\ |\ x \in X\}$ 
- For $B \subseteq Y$ the **preimage** is $f^{-1} (B) = \{ x \in X\ |\ f(x) \in B \}$
- For $A \subseteq X$, the **restriction** is $f \upharpoonright_{A} = f \cap (A\times Y)$ is a function $f \upharpoonright_{A} : A \rightarrow Y$ 
	- From original function $f: X \rightarrow Y$ 

<hr>
### Injections
	Distinct inputs go to distinct outputs
> $\forall y_{1},y_{2} \in Y$ 
> $f(y_{1}) = f(y_{2}) \implies y_{1} = y_{2}$ 
### Surjections
	Every potential output is indeed the image of some input
> $\forall y \in Y.\exists x \in X.f(x) = y$
### Bijections
	Both injective and surjective (one-to-one correspondence)

<hr>
## Inverses
	Provides input from an output of the original function
- An inverse of $f: X \rightarrow Y$ is $g: Y \rightarrow X$ 
- A function can only have an inverse iff it is bijective
## Cardinalities
- If there exists an injection $f: X \rightarrow Y$, then $|X| \le |Y|$
- if there exists a surjection $f: X \rightarrow Y$, then $|X|\ge |Y|$
- If there exists a bijection $f:X \rightarrow Y$, then $|X|=|Y|$

