	Graph representing Regex
- Start at the initial state
- Each arrow represents reading a character

Two types of nodes:
- Accepting state
- Rejecting state
## Types of Automata
### Total DFA
A total DFA (Deterministic Finite Automata) consists of:
- A finite set $X$ of states
- An initial state $p \in X$
- A total transition function $\delta : X \times \Sigma \rightarrow X$
- A set of accepting states $\in X$
### Partial DFA
	Doesn't have transition for every possible input
- Rejected if stuck in the DFA
- Converted to a total DFA by turning it into an error state
- Can have missing initial state
### Non-deterministic
	Asks whether a word is acceptable instead of accepted
- Can have two same transitions out of the same state
- Can have two ore more initial states

## $\epsilon$ - transitions
	NFA which can move between states without an input
Eg. $a(aa)*b(bb)*$
![[Pasted image 20260120104131.png]]

**slow transition:** one input but goes through many epsilon states before input character
**slow accept:** goes through several epsilons before getting accepted
### Converting to NFA
	
- Create a shortcut to override all slow transitions

## Generalised NFA
### Converting to RegEx
1. Combine arrows with the same start and end node
2. Insert arrows labelled by $\varnothing$ where they are missing
3. Add a single initial state START and single accepting state END
	1. START has $\epsilon$ to initial states & $\varnothing$ to non-initial states
	2. END has $\epsilon$ to accepting states & $\varnothing$ to rejecting states
	3. Add $\varnothing$ between START and END 

> We have unique arrows between any two states, this state will be **invariant** in our algorithm
	**invariant:** assume true, but state must be returned to at the end

4. Remove medial states one-by-one until only START and END left
	1. Adjust all labels while removing
		1. Join all branch labels with $|$ 
		2. Replace loops with $*$ 
5. Read final label for RegEx

## Complementation
	Everything outside of the set of words

To show the complement of a regular language is regular:
- Convert RegEx to total DFA
- Swap accepting and rejecting states


Related:
[[Regex]] 
[[Kleene's Theorem]]

