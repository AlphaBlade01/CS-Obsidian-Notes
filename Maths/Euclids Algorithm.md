Finds the **greatest common divisor** (gcd) of two numbers $a, b \in \mathbb{Z}$ 

1. **Initialisation:** set $r_0 = max(a,b)$  and $r_1 = min(a,b)$
2. For each iteration step $k$ :
	1. $r_k = ar_{k+1} + r_{k+2}$ 
		$r_{k+2}= r_k\mod r_{k+1}$  
	2. Repeat until $r_{k+2}=0$ 
