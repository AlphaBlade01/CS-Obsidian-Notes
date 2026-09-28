## Binary Relations
**Relation on X:** A subset $R \subseteq X^2$  
**Notation:** $x\ R\ Y$ means $(x, y) \in R$ 
#### Example
$R_1= \{ (x,y) \in \mathbb{Z}^2\ |\ x \equiv y\ (m od\ 7) \}$

### Relations as (directed) graphs
For a relation $R$ on $X$, depict $R$ as a **graph**:
- Draw elements from $X$ as nodes
- Connect $x$ to $y$ when $x\ R\ y$ with $x,y \in X$ 

### Equivalence Relation
	Relation that looks like equality
#### Axioms
- **Reflexivity:** Every element relates to itself 
	$\forall x \in X.x\ R\ x$
- **Symmetry:** Every element is related both ways around
	$\forall x,y \in X.x\ R\ y \implies y\ R\ x$
- **Transitivity:** Wherever you can go in two steps, there is a shortcut in one step
	$\forall x,y,z \in X.x\ R\ y \ \wedge\ y\ R\ z \implies x\ R\ z$
#### Equivalence Class
Equivalent class of an $x \in X$ is a set of all directly connected nodes.

For any $x \in X$ the equivalence class of $x$ is:
	$[x]_{R} = [x] = \{ y \in X\ |\ x\ R\ y \}$ 
The set of equivalent classes is written
	$X / R = \{ [x]\ |\ x \in X \}$ 

#### Partial Order
- **Antisymmetric relation:** $\forall x,y \in X.x\ R\ y \wedge y\ R\ x \implies x = y$
- Reflexivity
- Transitivity

## Heterogenous Relations
A subset $R \subseteq X \times Y$  