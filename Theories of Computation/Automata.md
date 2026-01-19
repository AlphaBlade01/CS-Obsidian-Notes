	Graph representing Regex
- Start at the initial state
- Each arrow represents reading a character

Two types of nodes:
- Accepting state
- Rejecting state
## Definition:
A total DFA consists of:
- A finite set $X$ of states
- An initial state $p \in X$
- A total transition function $\delta : X \times \Sigma \rightarrow X$
- A set of accepting states $\in X$
#### Partial DFA
	Doesn't have transition for every possible input
- Rejected if stuck in the DFA
- Converted to a total DFA by turning it into an error state
- Can have missing initial state

### Non-deterministic
	Asks whether a word is acceptable instead of accepted
- Can have two same transitions out of the same state
- Can have two ore more initial states


Related:
[[Regex]] 

