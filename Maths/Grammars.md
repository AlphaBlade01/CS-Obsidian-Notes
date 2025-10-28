## Backus Naur Form
are collections of rules of the form:
$$lhs ::= rhs_{1} | \dots | rhs_{n}$$
Each $lhs$ (a non-terminal symbol) can transform into any $rhs_i$ . Each $rhs_1$ to $rhs_n$ is a sequence of terminal symbols.

Example:
$$\exp ::= num|\exp+\exp|\exp\times\exp$$

## Arity
The number of arguments a terminal symbol takes
	**unary:** Contains one argument
	**binary:** Contains two arguments

## Fixity
The position the terminal symbol occurs in an argument.
	**infix:** occurs between an argument
	**prefix:** occurs before an argument
	**postfix:** occurs after argument

- 0, 1, etc. are **nullary** (arity 0) operators
- + and $\times$ are binary (arity 2) infix operators

#### Eg. 1
$$ \exp \mapsto \exp + \exp \mapsto 1 + \exp \mapsto 1 + 2 $$

## Abstract Syntax Tree
Grammar expressions can be represented as a tree

## Associativity
Sometimes there maybe be ambiguity in an expression. This will affect the Abstract Syntax Tree generated. 
- Left associativity: $(0 + 1) + 2$
- Right associativity: $0 + (1 + 2)$

## Precedence
The order that terminal symbols are conceived in. 
	**Eg.** $\times$ has higher precedence than $+$ in maths

## Axiom schemata
Defines a rule of a language by using (meta)variables to generalise statements to all applicable expressions.

**Eg. Schema that defines commutativity**
$$ \exp_{1} + \exp_{2} = \exp_{2} + \exp_{1} $$
