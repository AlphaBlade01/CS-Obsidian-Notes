
## Arrays & Dynamic arrays
- **Basic array operations:** Constant time $O(1)$ access & replacement by index
- **Insertion:** Inserting into array requires shifting elements or creating a larger array resulting in $O(n)$ time
#### Optimising for best Amortised Complexity
- **Naïve approach:** When full, increase by fixed amount
	Results in amortised complexity of $O(n)$ because copying is too frequent
- **Smart approach:** When full, double array size
	Leads to amortised complexity of $O(1)$ 
## Trees
**complete:** when all levels except for the last have the maximum number of nodes & all leaf nodes are towards the left
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
## Heap
### Priority Queues
	an ADT which maintains a collection of items with priorities
#### Operations
- **insert(value)**: Adds a new value with a predefined key into the heap
- **get_max()**: Returns the item with the max key 
- **delete_max()**: Deletes the item with the max key & returns its value
### Binary Heaps
**heap tree:** if the key of each node is $\ge$ than the key of each of its children
**binary heap tree:** a complete & binary heap tree
#### Representation
	Binary heaps can efficiently be stored in an array.
For each node at index $i$:
- **Parent index:** $(i-1)/2$
- **Left child index:** $2i + 1$
- **Right child index:** $2i + 2$
#### Operations
**Bubble up:** Keep moving value up until it is smaller than its parent
**Bubble down:** Keep moving value down until it is greater than all its children
##### Insert
1. Insert value at the end of last level
2. Keep "bubbling" it up as long as it's larger than its parent
##### Delete
1. Delete value
2. Replace deleted value with last value in the subtree under the value
3. Bubble down until correct order