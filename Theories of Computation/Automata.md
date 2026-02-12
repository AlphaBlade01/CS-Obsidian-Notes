	Graph representing Regex
- Start at the initial state
- Each arrow represents reading a character

Related:
[[Regex]] 
[[Kleene's Theorem]]

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
- The automata exists in all reachable states at once

**slow transition:** one input but goes through many epsilon states before input character
**slow accept:** goes through several epsilons before getting accepted
### Converting to "fast" NFA
	Removing unnecessary complexities introduced by epsilon
- Maintain all initial states & intermediary states 
- Create a shortcut to override all slow transitions
- States that lead to slow accept can become accepting states

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

## Regularities
	Regular: language can be represented by a RegEx
#### Complementation
To show the complement of a regular language is regular:
1. Convert RegEx to total DFA
2. Swap accepting and rejecting states
#### Intersection
To show the intersection of two regular languages is regular:
- Express through union & complementation: $L\cap M = \overline{\overline{L}\cup \overline{M}}$ 
- Construct a DFA with ordered pair of states from the original two automata

## Equivalence
	Testing whether two regular expressions represent the same language
1. Create automatas for either expression
2. Starting from initial state, create a new automata of pairs of states $(x,y)$ from both automata
3. If every state is either accepted or rejected by both automata, they are equivalent

## Minimal Automata
	Automata with no unnecessary states

A minimal partial DFA is a partial DFA that satisfies 3 conditions:
- Every state is **reachable**
- Every state is **hopeful**
- Every pair of equivalent states are equal

> **Reachable:** A state $s$ is reachable if there is a path from an initial state to $s$
> **Hopeful:** A state $s$ is hopeful when there is a path from $s$ to an accepting state
> **Equivalent:** Two states $s$ and $t$ are equivalent if $\delta(s, a)$ and $\delta(t,a)$ both lead to same acceptance 
> 	They must also have the same transitions: each following state is equivalent
> 	$\delta(state, input)$ represents path from $state$ along $input$ 
### How to minimise an Automata
1. Remove all unreachable states
2. Remove all hopeless states
3. Merge each set of equivalent states
![[Pasted image 20260204223642.png]]

