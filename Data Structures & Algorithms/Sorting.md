Related:
[[Asymptotic Notation]]

**sort key:** the attribute by which a sorting algorithm sorts
**stable sorting algorithm:** does not change order of items in a section of the array if they have the same sort key
	Eg. if we have a list of students sorted by their first name and we sort by their last name, the students with the same last name would still be in order of first name relative to each other

## Comparison-based
### Lower bound time complexity
- To sort $n$ items, there are $n!$ possible orderings
- Decision tree is a **binary tree** where there is at least one leaf for every possible ordering
	- There are at least $n!$ leaves
- **average** number of comparisons is the average path length from root to a leaf
- **worst case** number of comparisons is the height of the tree

To find lowest time complexity, we need to find the smallest height of the decision tree:
- A binary tree of height $h$ has at most $2^h$ leaves
- hence, $2^h \ge n! \implies \log 2^h \ge \log n! \implies h \ge \log n!$ 
	- (there are at least $n!$ leaves)
- $\log n! \ge \log(n/2)^{n/2} = (n/2)\log(n/2) \ge Cn\log n$ 
	- $\log n! \ge \log(n/2)^{n/2}$ always holds because it's like replacing the first half of multiplications in $n!$ by $n/2$ which is less than all the terms 
- hence, $h \ge Cn\log n \implies \Omega(n\log n)$
### Bubble sort
**Time complexity:** $O(n^2)$
1. Pass over array comparing two adjacent elements continuously
2. Swap elements if in the wrong order
3. Repeat until no swaps made in a pass
#### Notes
- After every pass, the last affected element is in the right place
- Stable sorting algorithm
### Selection sort
**Time complexity:** $O(n^2)$
1. Partition the array into sorted and unsorted elements (sorted section is empty)
2. Find smallest element from unsorted section
3. Append that element onto the end of the sorted section (increasing sorted array size by 1)
#### Notes
- Unstable sorting algorithm
### Heap sort
	Less naive implementation of selection sort
**Time complexity:** $O(n \log n)$
1. Build binary heap from array (heapify array)
2. Remove maximum element from heap and insert furthest to the end of sorted array
3. Repeat step 2 until heap is empty

## Divide & Conquer
- Recursively split problem into smaller sub-problems until simple
- Put together the solutions of the smaller sub-problems into the solution of the big problem
### Merge sort
**Time complexity:** $O(n\log(n))$
1. Recursively split input array into smaller arrays until each array is of size 1
2. Merge smaller arrays repeatedly, sorting along the way, until there is only 1 array left
#### Notes
- Stable sorting algorithm
### Quick sort
**Time complexity:** 
- **worst case:** $O(n^2)$
- **average case:** $O(n\log n)$ if constantly split into roughly equal halves

1. Select an element of the array to be a **pivot**
2. Partition the array leaving two sub-arrays either side of the pivot
3. Append all elements smaller than the pivot to the left partition
4. Append all elements greater than the pivot to the right partition
5. Repeat process on both sub-arrays
#### Notes
- After a single loop is processed, the pivot element of that loop is in the correct index
- If pivot is selected randomly or input is shuffled randomly
	- probability $\le 50\%$ that the pivot is in the middle of $50\%$ of entries
	- $\ge25\%$ smaller entries and larger entries are in the correct section
	- worst-case sizes of partitions is $\frac{3}{4}n$ and $\frac{1}{4}n$ 
	- only $\log_{4/3}n = C\log n$ recursive calls required
	- time complexity is $O(n\log n)$ 
- Stability depends on implementation

## Pigeonhole sort
	Used on list of integer values with a small range
**Time complexity:** $O(n)$
1. Find range of elements $N$ 
2. Create "pigeonholes" array of size $N$ 
3. For each element $x$ in original array, insert it into pigeonholes array into index $x$ 
4. Iterate through pigeonholes & copy elements back into original array
#### Notes
- Stable sorting algorithm