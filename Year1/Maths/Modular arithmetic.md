a, b are congruent modulo m if a mod m = b mod m

Inverse of $a \in Z$ (mod m) is any $b \in \mathbb{Z}$ with $ab \equiv 1$ (mod m)
$a^-1$ (mod m) exists $\iff$ $a, m$ are coprime

### Bezout's Lemma
$\exists x, y \in \mathbb{Z}$ such that $ax + by = gcd(a, b)$

### Chinese Remainder Theorem
	$x \equiv a_1$ (mod $m_1$)    and     $x \equiv a_2$ (mod $m_2$)

When $m_{1}$ and $m_2$ are **coprime** and solutions given by $x \equiv N$ (mod $m_1 m_2$) for some N,
you can write down $N$ with formula:
- If $m_1 x + m_2 y = 1...$
- then $N = a_2 m_1 x + a_1 m_2 y$
