Related: [[Matrices]]

- S is **linearly dependent** if for some vectors $v_1, ..., v_k$ in S with k > 0 and some non-zero $r_{1},\dots,r_{k} \in \mathbb{R}$ 
	- $r_{1}v_{1}+\dots+r_{k}v_{k} = 0$
- S is **linearly independent** if $r_{1}=\dots=r_{k}=0$

In Vector space $V$:
	**Span:** $S \subseteq V$ is the set of all linear combinations of S
	**Basis:** $B \subseteq V$ where $V$ is linearly independent

#### Rotation of axes
Rotating clockwise:
	$x' = \cos(\theta)x + \sin(\theta)y$ 
	$y' = -\sin(\theta)x + \cos(\theta)y$

## Linear Operators
Given vector spaces $V, W$ a map $F:\ V\to W$ is **linear operator** if:
	$F(r \vec{v}) = rF(\vec{v})$
	$F(\vec{v} + \vec{w}) = F(\vec{v}) + F(\vec{w})$
- Preserve zero vectors
### Composition
Given $\mathcal{L}(V, W)$ is a set of all linear operators from V to W
$F \in \mathcal{L}(U,W)\ \wedge\ G \in \mathcal{L}(V,U) \implies F \cdot G \in \mathcal{L}(V, W)$ 
- applies $G$ first then $F$ 
### Properties
- Associativity with addition
	$(F+G) + H = F + (G+H)$
- Associativity with function composition
	$F\cdot (G\cdot H) = (F\cdot G)\cdot H$
- Distributivity with composition over addition
	$F\cdot(G+H) = F\cdot G+F\cdot H$

## Orthonormal basis
For basis $(\vec{v_{1}},\dots,\vec{v_{n}})$:
- **Orthogonal:** If $\langle \vec{v_{i}}, \vec{v_{j}} \rangle = 0$ when $i \neq j$
- **Orthonormal:** If orthogonal and $\langle \vec{v_{i}} = \vec{v_{j}} \rangle = 1$
### Householder Reflections
	Reflection over the hyperplane orthogonal to v

$$H = I - \frac{2}{|v|^2} v^T v$$
## Eigenvectors & Eigenvalues
For a $n\times n$ matrix $A$, & $n\times 1$ vector $v$:
- $Av = \lambda v$ 
- $v$ would be an eigenvector of $A$
- $\lambda$ is the eigenvalue corresponding to $v$
$$Av = \lambda v \iff Av - \lambda v = O \iff (A - \lambda I)v = O$$
