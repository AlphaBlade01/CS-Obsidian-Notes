## Augmented Matrix
	Matrix with coefficients as the row values

![[Pasted image 20251113114254.png]]

### Row Echelon form
**Leading entry:** first non-zero entry in a row

A matrix is in row echelon form if:
- Every row with zero entries only is at the bottom of the matrix
- First leading entry is strictly to the right of the leading entry in the row above

A matrix is in **Reduced Row Echelon form** if:
- It is in row echelon form
- Every leading entry is 1
- Every entry above and below every leading entry is 0

## Inversion

## Rank
- **rank-deficient:** its rank < no. of columns/rows
- Any square matrix is **rank-deficient** $\iff$ its determinant = 0

### Orthogonal matrices
$A$ is **orthogonal** if $A^T A = I$ 
- $A^T$ is inverse
- $A$ preserves dot product: $\langle Ax, Ay \rangle = \langle x^T, y^T \rangle$ 
- $A$ preserves length: $|Ax| = |x^T|$
- $A$ preserves distance: $d(Ax, Ay) = d(x^T, y^T)$
- $A$ preserves angles: $\angle(Ax, Ay) = \angle(x, y)$

