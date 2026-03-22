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

