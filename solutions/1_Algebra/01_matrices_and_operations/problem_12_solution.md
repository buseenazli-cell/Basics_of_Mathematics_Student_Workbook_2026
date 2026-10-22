# Exercise 12. Powers of a Matrix and Induction

## Question

Let

$$
A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}
$$

Compute $A^2$, $A^3$ and $A^4$, and use them to formulate a conjecture for $A^n$. Then do not stop after checking one more case: assume the formula is true for $n$, multiply by $A$, and explain why you obtain exactly the formula for $n+1$.

## Solution

### Method

Each entry of a product is obtained by pairing a row of the left matrix with a column of the right matrix: multiply corresponding entries and add. We compute successive powers by multiplying the previous power by $A$ on the right, look for a pattern, and then prove that the pattern continues forever.

### Computing the powers

$$
A^2 = AA = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}
= \begin{pmatrix} 1\cdot 1 + 1\cdot 0 & 1\cdot 1 + 1\cdot 1 \\ 0\cdot 1 + 1\cdot 0 & 0\cdot 1 + 1\cdot 1 \end{pmatrix}
= \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}
$$

$$
A^3 = A^2 A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}
= \begin{pmatrix} 1\cdot 1 + 2\cdot 0 & 1\cdot 1 + 2\cdot 1 \\ 0\cdot 1 + 1\cdot 0 & 0\cdot 1 + 1\cdot 1 \end{pmatrix}
= \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}
$$

$$
A^4 = A^3 A = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}
= \begin{pmatrix} 1\cdot 1 + 3\cdot 0 & 1\cdot 1 + 3\cdot 1 \\ 0\cdot 1 + 1\cdot 0 & 0\cdot 1 + 1\cdot 1 \end{pmatrix}
= \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}
$$

### Conjecture

In each power, the diagonal entries stay $1$, the lower left entry stays $0$, and the upper right entry equals the exponent. This suggests

$$
A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix} \qquad \text{for every integer } n \geq 1
$$

Checking a few cases does not prove this, so we show that the pattern cannot break.

### Inductive step

Assume the formula holds for some integer $n \geq 1$:

$$
A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}
$$

Multiply by $A$ once more, using $A^{n+1} = A^n A$, and compute each entry:

$$
A^{n+1} = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}
= \begin{pmatrix} 1\cdot 1 + n\cdot 0 & 1\cdot 1 + n\cdot 1 \\ 0\cdot 1 + 1\cdot 0 & 0\cdot 1 + 1\cdot 1 \end{pmatrix}
= \begin{pmatrix} 1 & 1 + n \\ 0 & 1 \end{pmatrix}
$$

Entry by entry:

- (1,1): $1\cdot 1 + n\cdot 0 = 1$
- (1,2): $1\cdot 1 + n\cdot 1 = n + 1$
- (2,1): $0\cdot 1 + 1\cdot 0 = 0$
- (2,2): $0\cdot 1 + 1\cdot 1 = 1$

Therefore

$$
A^{n+1} = \begin{pmatrix} 1 & n+1 \\ 0 & 1 \end{pmatrix}
$$

which is exactly the conjectured formula with $n$ replaced by $n+1$. The extra factor $A$ contributes one more copy of the entry $1$ to the upper right corner, so that entry increases by exactly $1$ each time.

### Conclusion

The formula holds for $n = 1$, because $A^1 = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$, and the inductive step carries every case to the next one. Hence, by induction, the formula holds for every integer $n \geq 1$:

$$
A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}
$$
