**Type:** set of possible values with a set of allowed operations on them
**Abstract Data Type:** type whose internal representation is hidden to the user
	Interface

## Arrays & Dynamic arrays
- **Basic array operations:** Constant time $O(1)$ access & replacement by index
- **Insertion:** Inserting into array requires shifting elements or creating a larger array resulting in $O(n)$ time
#### Optimising for best Amortised Complexity
- **Naïve approach:** When full, increase by fixed amount
	Results in amortised complexity of $O(n)$ because copying is too frequent
- **Smart approach:** When full, double array size
	Leads to amortised complexity of $O(1)$ 

## Linked Lists
	List without contiguous memory space
- Built up of **nodes** containing a value variable & pointer to the next node

**Doubly Linked List:** Each node contains pointers to next & previous nodes
	Allows for efficient deletion from the end if address of last node known
**Circular Linked List:** Last node points back to beginning

## Trees
**Level:** length of path between root and node
**Height:** length of longest path between root & leaf node
**Size:** number of nodes in tree
**Complete:** when all levels except for the last have the maximum number of nodes & all leaf nodes are towards the left

**Quad tree:** Each node has exactly 4 children & often only leaf nodes have values
### Binary Tree
	Tree with each node having max 2 children
**Complete binary tree:** A binary tree that can be stored in an array without wasting space
**Perfect binary tree:** Has the maximum no. of nodes for its height
**Full binary tree:** Each node has either 0 or 2 children
### Implementation
**Basic:** Use doubly linked list nodes with a value field and left & right children pointers
**Sibling list:** Use nodes with value field, single child pointer & sibling pointer
**Array:** Store all values within array with root node at index 0
	**Left child index:** $2i + 1$
	**Right child index:** $2i + 2$
	**Parent index:** $(i-1)/2$

## Binary search tree
	Binary tree where elements are in order when flattened
**Flattening:** Turning a tree to an array 
	recursively flatten(root.left) + root.value + flatten(root.right)
#### Requirements
- Values in left subtree are smaller than root
- Values in right subtree are larger than root
- Root's left & right subtrees are also BSTs
#### Complexity
	Heavily dependent on height
**Best/average case:** If tree is balanced, height is approximately $O(\log n)$
**Worst case:** If tree skewed to one side, height is approximately $O(n)$ 
>Average height of a general BST is $O(\sqrt{ n })$
#### Searching
**Time complexity:** $O(height) \subseteq O(n)$ 
1. Start at root
2. If $x$ smaller, value is in left subtree
3. If $x$ larger, value is in right subtree
#### Insertion
**Time complexity:** $O(height) \subseteq O(n)$
1. Start at root
2. If $x$ greater, insert into right subtree
3. If $x$ smaller, insert into left subtree
4. Repeat until inserting into empty subtree then insert into root of that subtree
#### Deletion
1. Find node containing element to be deleted
2. If node is a leaf node, delete node
3. If node has 1 child, replace node with child
4. Else:
	1. Find left-most node $x$ in right subtree (smallest value)
	2. Replace node with $x$
	3. Replace old location of $x$ with $x$'s right child (may be empty)

## Heap
### Priority Queues
	an ADT which maintains a collection of items with priorities
- Implemented using a heap
#### Operations
- **insert(value)**: Adds a new value with a predefined key into the heap
- **get_max()**: Returns the item with the max key 
- **delete_max()**: Deletes the item with the max key & returns its value
### Binary Heaps
**heap tree:** if the key of each node is $\ge$ than the key of each of its children
**binary heap tree:** a complete binary tree
- Can be efficiently stored in an array
#### Operations
**Bubble up:** Keep moving value up until it is smaller than its parent
**Bubble down:** Keep moving value down until it is greater than all its children
##### Insert
1. Insert value at the end of last level
2. Keep "bubbling" it up as long as it's larger than its parent
##### Delete Max
1. Delete root node
2. Replace deleted value with last value in heap
3. Bubble new root node down until correct order
	Ensure node is swapped with highest priority child in each bubble down stage
##### Delete Arbitrary
1. Delete node and replace it with last value in heap
2. Compare it with parent & children to decide whether to bubble down or up
3. Repeat step 2 until in correct place
### Heapifying an Array
	Turning an arbitrary array into a (binary) heap
- Values can be either bubbled down or bubbled up
#### Bubbling up
	Naive approach (worse time complexity)
**Time complexity:** $O(n\log n)$ 
1. Start from 1st level (ignoring root) and bubble up each node in level
2. Go to lower level & repeat step 1 until all nodes considered
#### Bubbling down
	Better method
**Time complexity:** $O(n)$
1. Start from second lowest level and bubble down each node in level
2. Go to higher level & repeat step 1 until root node processed
#### Why bubbling down is better
- Leaf nodes don't have to be considered (half the tree)
- For bubbling up, leaf nodes have maximum potential swaps, & high density of leaf nodes
- For bubbling down, root node has maximum potential swaps, lower density at the top

## AVL Trees
	self-balancing binary tree
- **balance invariant:** each node must have a balance of $-1,\ 0,\ \text{or}\ 1$  
- balance = height(x.left) - height(x.right)
- ensures height of tree remains $O(\log n)$ 