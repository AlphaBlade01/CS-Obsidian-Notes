## Logic Gates
For n inputs there are $2^n$ possible outputs.
- AND gate represented using two switches in series
- OR gate represented using two switches in parallel
### Universal Gates
NAND and NOR gates are **Universal Gates**. Any boolean function can be represented using just NAND or NOR gates. 

### Deriving Expression from Truth Table
**minterm:** product term where each variable appears at least once in truthy and complemented form
**maxterm:** 

## Boolean Algebra
- ``.`` and ``^`` used to denote AND 
- ``+`` used to denote OR
- $\bar{A}$ used to denote NOT
- $\oplus$ Used to denote XOR
##### Identity
$a + 0 = a$
$a.a = a$
##### Commutativity
$a + b = b + a$
$a.b = b.a$
##### Associativity
$a + (b + c) = (a + b) + c$
$a.(b.c) = (a.b).c$
##### Distributivity
$a + (b.c) = (a + b).(a + c)$
##### DeMorgan's Law
$\bar{(a.b)} = \bar{a}+\bar{b}$  (Negates variables and operators)
##### Absorption
$a + a.b \to a(a + b)$ 

