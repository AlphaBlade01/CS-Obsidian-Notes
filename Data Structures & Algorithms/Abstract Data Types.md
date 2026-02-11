
## Arrays & Dynamic arrays
- **Basic array operations:** Constant time $O(1)$ access & replacement by index
- **Insertion:** Inserting into array requires shifting elements or creating a larger array resulting in $O(n)$ time
#### Optimising for best Amortised Complexity
- **Naïve approach:** When full, increase by fixed amount
	Results in amortised complexity of $O(n)$ because copying is too frequent
- **Smart approach:** When full, double array size
	Leads to amortised complexity of $O(1)$ 

