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
