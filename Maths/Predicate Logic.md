Related:
[[Propositional logic]]

Also known as **first-order logic**

**Relations:** For $Student(sid, name)$, the predicate $Student$ relates student ids and names
**Domain:** Non-empty set of objects/entities to reason about
**Formula:** A query

### Ingredients of predicate logic
- **Predicates:** Evaluates true/false depending on its arguments
- **Quantifiers:** Universal quantifier $\forall$, Existential quantifier $\exists$ 
- **Variables:** Symbol to represent objects in the domain
- **Functions:** Build an element of the domain from elements of the domain
	- Arity: The number of arguments a function is given - $f^n$, where $n$ is arity 
- **Constants:** Specific objects in the domain with arity 0

#### Syntax
$t::= x\ |\ f(t,\dots, t)$
$P ::= p(t, \dots, t)\ |$  ....same as propositional... $|\ \forall x.P\ |\ \exists x.P$ 

- The scope of a quantifier extends as far right as possible

## Semantics
	Assigning meaning/interpretations to formulas

Given a domain $D$ and a predicate symbol $p$ of arity $n$:
- $p$ is interpreted by a $n$-ary relation $R_p$
	$\{ <d_{1}^1,\dots,d_{n}^1>,\ <d_{1}^2,\dots,d_{n}^2>,\ \dots \}$ 

Given domain $D$ and function symbol $f$ of arity $n$:
- $f$ is interpreted by function $F_f$ which maps $D^n$ to $D$
	$F_{f} \in D^n \to D$

## Models
	Provides interpretation of all symbols

Given **signature** $\langle \langle f^{k_1}_{j_1}, \dots, f^{k_n}_{j_n} \rangle, \langle p^{j_1}_{i_1}, \dots, p^{j_m}_{i_m} \rangle \rangle$ 
- function symbols $f_i$ of arity $k_i$
- predicate symbols $p_i$ of arity $j_i$ 
a **model** is the structure $\langle D, \langle \mathcal{F}_{f_1}, \dots, \mathcal{F}_{f_n} \rangle, \langle \mathcal{R}_{p_1}, \dots, \mathcal{R}_{p_m} \rangle \rangle$ 
- for non-empty domain $D$
- interpretations $F_f$ for function symbols $f_{i}$
- interpretations $R_{p}$ for predicate symbols $p_i$ 

#### Variable valuations
	Assign meaning to variables
- Done using a partial function $v$
- maps variables to $D$ 

To apply meaning to a predicate logic formula, we use:
- $[[t]]^M_v$ : gives meaning to term $t$ with model $M$ and variable valuation $v$
- $\vDash _{M,v} P$  : gives meaning to formula $P$ w.r.t. $M$ and $v$
