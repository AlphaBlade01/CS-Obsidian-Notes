- $n$ = the input size
## Big O Notation
	Represents the upper bound of a function's growth relative to n
- When giving an upper bound, we write it in the form: $f(n) \le Cg(n)$ for some constant $C>0$ 
- We can also write it as $f(n) \in O(g(n))$ **if** $\exists C,n_0$ such that $\forall n \ge n_0,\ |f(n)| \le |Cg(n)|$ 
- $O(g(n))$ is a set of functions that **do not** grow at a faster rate than $g$ 
## Omega notation ($\Omega$)
	A lower bound on a function's growth relative to n
- $f\in \Omega(g)$ if exists $C,n_0 > 0$ such that for all $n > n_0:\ C|g(n)| \le |f(n)|$
## Theta notation ($\Theta$)
	Upper bound & lower bound on a function's growth relative to n
- $f\in \Theta(g)$ if exists $C_0, C_1, n_0 > 0$ such that for all $n > n_0:\ C_0|g(n)| \le |f(n)| \le C_1(g(n))$ 
