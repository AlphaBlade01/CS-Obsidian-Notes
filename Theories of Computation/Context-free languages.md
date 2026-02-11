## Context-free grammar
Uses Backus-Naur Form which is defined in [[Grammars]]
	**Eg. writing BNF grammar:**
	$A ::= 3 |\ 5 |\ A + A|\ A\times A |\ (A)|\ if\ B\ then\ A\ else\ A$

A context-free grammar is a **4-tuple:** $( V,\Sigma, R, S)$
- $V$ : finite set of **variables / non-terminals**
	Eg. $\{\ A,\ B\ \}$
- $\Sigma$ : finite set of **terminals**, disjoint from $V$ 
	Eg. $\{\ (,\ ),\ +,\ 3,\ 5,\ if,\ then,\ else,\ and,\ >,\ \times \ \}$
- $R$ : finite set of rules with each rule consisting of a variable followed by a string of variables & terminals
- $S \in V$ : start variable

## Converting DFA to CFG
1. Have a variable for each state
	1. Set start variable to initial state
2. For each variable, it can produce: $input$ followed by $next\ state$ 