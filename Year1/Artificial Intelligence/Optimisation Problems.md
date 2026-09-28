### Formulation
- **design variables:** represent candidate solution
- **objective function:** defines cost of solution (minimised or maximised)
- **constraints:** rules that the solution must satisfy
## Local search algorithms
- Search from an initial state
- Do **not** keep track of paths or states that have been reached
- Advantages:
	- They use very little memory
	- Can find reasonable solutions in large spaces
### Hill climbing
	Greedy algorithm
**Completeness:** hill climbing is not complete
	Depends on problem formulation and algorithm design
**Optimality:** hill climbing is not optimal
	Can get stuck in local maximum
**Time complexity:** $O(mnp)$ 
	$m$ = max no. of iterations
	$n$ = max no. of neighbours
	$p$ = time to generate neighbours
**Space complexity:** $O(n)$
#### Process:
1. Generate random initial solution
2. Move to better neighbouring solutions
3. If no better neighbouring solutions, terminate.
#### Stochastic Hill Climbing
- Chooses at random among the uphill moves
- Probability can depend on the steepness
- Converges more slowly
- Can find higher quality solutions
#### First-Choice Hill Climbing
	Implementation of stochastic hill climbing
- Randomly generates successors until better than current
- Performs well when a state has many successors
#### Random-Restart Hill Climbing
- Generates a series of hill climbing searches from random initial states
- **Complete** because guaranteed to find a solution

### Simulated Annealing
	A more random implementation of hill climbing to avoid getting stuck in local maxima
**Completeness:** Not complete as it depends on problem formulation & algorithm design
**Optimality:** Not optimal as it depends on termination criteria
**Time complexity:** depends on schedule and termination criterion
**Space complexity:** depends on how design variables are represented
#### Process
1. Generate neighbour solutions
2. Pick random solution
	- Better solutions always accepted
	- Worse solutions accepted with $P < 1$ and $P$ (temp) decreases over time
3. Terminate when min temp reached or solution does not change in value
#### Probability
Probability defined $e^{\Delta E / T}$
	$\Delta E$ = change in quality between states
	$T$ = temperature

- **High temperature:** higher probability to accept move
- **Low temperature:** lower probability to accept move
