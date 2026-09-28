Related: [[Logic]]

**Proposition:** a sentence that states a fact

An argument is valid iff all premises and conclusion is correct
**Symbols:**
- Atomic proposition (true/false atomic statements)
- Combined using logical connectives

## Syntax
#### Atomic propositions (atoms)
- Cannot be broken into smaller parts
- $\top$ stands for True $\bot$ stands for False
#### Logical Connectives
- conjunction: $P\wedge Q$ both $P$ and $Q$ are true
- disjunction: $P \vee Q$ at least one of $P$ and $Q$ are true
- implication: $P \implies Q$   if...then / implies
- negation: $¬P$ flips $P$

 
**Associativity:** All operators are right associative

## Arguments
	A list of propositions

- **Conclusion:** Last proposition in an argument
- **Premises:** Other propositions in an argument

- Written as a sequent
- Set of premises separated by commas, then a **turnstile** ( $\vdash$ ) followed by conclusion.

## Natural Deduction
- Syntactic proof method
- Constructed by applying inference rules

#### Inference Rules
	Tools we have/are allowed to use

**Eg.** And-introduction
$$\frac{A \ \ \ \ B}{A\wedge B} \ [\wedge I]$$
	"If A is true and B is true then $A\wedge B$ is true"
	Inference rule name on the right

## Classical Reasoning
- Relies on boolean truth values

#### Double Negation Elimination
	"Proof by contradiction"
- $¬¬A \vdash A$ 
#### Law of Excluded Middle
- $\vdash A \vee ¬A$


##### Contrapositive
The contrapositive of $A \implies B$ is $¬B \implies ¬A$


## Semantics
	Assign meanings/interpretations with formulas

**Truth assignment:** Function assigning a truth value for each atomic proposition ($\phi$)
**Satisfiability:** Given a valuation $\phi$ on all atomic propositions, $\phi$ satisfies $A$ if $\phi(A) = T$ 
**Validity:** A formula is true in all scenarios
	**Syntactically:** conclusion can be derived from premises
	**Semantically:** conclusion is true whenever premises are true
#### Compound Formulas
$\phi(A\wedge B)=T \iff \phi(A)=T\ \cap\ \phi(B)=T$
$\phi(A\vee B) =T \iff \phi(A)=T\ \cup \phi(B)=T$
$\dots$

**Soundness:** A deduction system is sound w.r.t. a semantics if every provable formula is valid
	$\vdash A \rightarrow\ \models A$
**Completeness:** A deduction system is complete w.r.t. a semantics if every valid formula is provable
	$\models A \rightarrow\ \vdash A$ 


## Normal forms

**Conjunctive Normal forms**: $(A \vee B \vee C) \wedge (D \vee X) \wedge (¬A)$ 
	Disjunction of literals
**Disjunctive Normal form:** $(P \wedge Q \wedge A) \vee (R \wedge ¬Q) \vee (¬A)$ 
	Conjunction of literals

> **Theorem:** Every proposition is equivalent to a formula in CNF and DNF

- To read DNF from truth table, OR the truthy fields
- To read CNF from truth table, AND the negation of the falsey fields

## SAT Problem
**Definition:** Given a CNF formula, can we assign T or F to each variable to satisfy the formula?

**P:** Class of problems that can be solved in polynomial time
**NP:** Class of problems that can have a potential solution derived in polynomial time
	$P \subseteq NP$

- Solution can be verified efficiently
- No known algorithm to solve the problem efficiently

#### DPLL Algorithm
	SAT Solver which uses pruning instead of brute force
1. Easy cases:
	- Atom $p$ only appears as either $p$ or $¬p$ (but not both): assign truth value accordingly
2. Branch:
	- Set a truth value to a variable $p$ then remove unnecessary clauses
3. Repeat until:
	- All clauses are true
	- One clause is false $\rightarrow$ return to step 2 and assign different truth value to $p$ 

- Empty clauses `()` are the same as false
