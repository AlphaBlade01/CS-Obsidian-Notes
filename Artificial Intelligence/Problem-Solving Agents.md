**Agent:** An entity that perceives the environment and acts within it

Problem-solving agents:
- Use atomic representation (each state of world is indivisible)
- Requires a precise definition of problem and goal

## Formulating search problems
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