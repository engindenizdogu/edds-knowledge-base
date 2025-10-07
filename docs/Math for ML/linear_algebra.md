---
title: Linear Algebra
parent: Math for ML
---
**Vector Operations:**
- Addition
- Scalar multiplication

**Linear Combinations (c, d, e $\in \mathbb{R}$):**
* c***u*** + d***v***
* c***u*** + d***v*** + e***w***

**Properties of Dot Product:**
- Distributive: $u^T(v + w) = u^Tv+u^Tw$
- Non-Associative: $u^T(v^Tw) \ne (u^Tv)^Tw$
- Commutative: $u^Tv = v^Tu$

**Cosine Formula for Dot Product:** $v^Tw = \|v\| . \|w\| . cos(θ)$ (**note:** cos(θ) = 0 when θ = 90°)

**Length of a vector:** $\left\| \mathbf{v} \right\| = \sqrt{v_1^2 + v_2^2 + v_3^2 + ...}$

**Matrix operations:**
- Addition (both matrices should have the same dimensions)
- Scalar multiplication
- Transpose: mapping A ∈ $\mathbb{R}^{n \times m}$ to B ∈ $\mathbb{R}^{m \times n}$ with $a_{ij} = b_{ji}$
- Trace: sum of all the elements along the diagonal
- Matrix multiplication (reminder: A∈$\mathbb{R}^{n \times m}$ and B∈$\mathbb{R}^{m \times k}$ then C=AB∈$\mathbb{R}^{n \times k}$)

**Multiplication Properties:**
- Distributivity: $(A +B)C = AC+BC$ and $A(C+D) =AC+AD$
- Associativity: $(AB)C = A(BC)$
- Non-commutative: $AB \ne BA$ (because of dimensions)
- Multiplication with the identity matrix results in the matrix itself

**Properties of Transpose:**
- $(A+B)^T =A^T +B^T$ and $(A - B)^T =A^T - B^T$
- $(AB)^T =B^T . A^T$

**Systems of Linear Equations Recap:**
- $Ax = b$
- Gaussian Elimination
- Row Echelon/Reduced Row Echelon Form

A matrix is in **row echelon form** if
- all rows having *only zero* entries are at the bottom
- The pivot (the leftmost non-zero entry) of every non-zero row, called the **pivot**, is to the right of the leading entry of every row above

A matrix is in **reduced row echelon form** if:
- it is in row echelon form
- the leading entry in each nonzero row is 1 (called a leading one)
- each column containing a leading 1 has zeros in all its other entries (or in other words, above the pivot if condition one is achieved)

**Properties of Determinants:**
- Matrix must be square
- The determinant of the identity matrix is 1.
- The exchange of two rows multiplies the determinant by −1.
- Multiplying a row or a column by a number multiplies the determinant by this number.
- Adding a multiple of one row to another row does not change the determinant.
- If two rows of matrix A are equal, then $det(A) = 0$.
- A matrix with a row of zeros has $det(A) = 0$.
- If A is *triangular* then $det(A)$ is the product of diagonal entries.
- $det(AB) = det(A).det(B)$
- $det(A^T) = det(A)$

**Laplace Expansion Example:**

![](../../../assets/images/determinant_3by3.png)


**Invertibility:**
- Matrix must be square
- If A is singular, then $det(A) = 0$. If A is invertible, then $det(A) \ne 0$.
- Can calculate the inverse using Gaussian Elimination
	- $[A \vert I]$  -> $[I \vert A^-1]$
* Inverse for a 2x2:

![](../../../assets/images/inverted_2by2.png)

