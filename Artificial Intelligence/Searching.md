**Agent:** An entity that perceives the environment and acts within it

Problem-solving agents:
- Use atomic representation (each state of world is indivisible)
- Requires a precise definition of problem and goal
### Formulating search problems
Formulating a search problem requires the following:
- **Initial state:** state where agent starts its search
- **Action set:** set which describes actions that can be executed in any state
- **Transition model:** mapping between all possible start and end states given a certain action
- **Goal test:** determine if a state is a goal state
- **Path cost function:** assigns cost to each path

**Solution:** sequence of actions from the initial state
**Path:** a sequence of states connected by a sequence of actions

**State Space Graph:** creating a search tree with states as nodes and branches as actions
	**frontier:** set of all currently available leaf nodes

## Uninformed search
	Doesn't have any information beyond what was defined in the problem
### Breadth-First search (BFS)
	Goes level by level
	Equivalent to queue (FIFO)
#### Process
1. Root node is expanded
2. All successors of root node are expanded
	- Already explored nodes are not added to frontier
3. Successors of those nodes are expanded until goal state discovered
#### Performance
$d =$ depth of shallowest goal node
$b =$ maximum no. of successors of any node
$m =$ maximum length of any path

- **Completeness:** complete if goal node is at some finite depth $d$ given $b$ is finite
- **Optimality:** optimal if path cost doesn't decrease as depth does
- **Time complexity:** $O(b^d)$ 
- **Space complexity:** $O(b^d)$ since there are $O(b^{d-1})$ explored nodes & $O(b^d)$ frontier nodes

### Depth-First search (DFS)
	Goes branch by branch
	Equivalent to stack (FILO)
#### Process
1. Root node expanded
2. First successor of root node expanded
3. Deepest node in frontier repeatedly expanded until goal node visited
	- Already explored nodes are not added to frontier
#### Performance
$d =$ depth of shallowest goal node
$b =$ maximum no. of successors of any node
$m =$ maximum length of any path

- **Completeness:** complete only if search space is finite and infinite loops avoided
- **Optimality:** not optimal, may return a deeper (more expensive) goal when a shorter one exists
- **Time complexity:** $O(b^m)$ 
- **Space complexity:** $O(b^m)$ as all nodes from root to leaf of each path is stored
##### Mitigations
- Fully explored branches can be removed from memory to turn space complexity to $O(bm)$
- The depth can be limited to avoid infinite search spaces

## Informed search
	Uses problem-specific knowledge beyond problem definition
