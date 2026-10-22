# Determinants and Invertibility of 2×2 Matrices

## Recall

$$
\det\begin{pmatrix} a & b \\ c & d \end{pmatrix} = ad - bc
$$

A square matrix is **invertible** $\iff$ its determinant is **nonzero**.

## Matrix 1

$$
A = \begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix}
$$

$$
\det A = 3\cdot 4 - (-2)\cdot 5 = 12 + 10 = 22
$$

Since $\det A = 22 \neq 0$, **$A$ is invertible**.

## Matrix 2

$$
B = \begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}
$$

$$
\det B = 1\cdot 14 - 7\cdot 2 = 14 - 14 = 0
$$

Since $\det B = 0$, **$B$ is not invertible** (it is singular).

The reason is that the second row is twice the first row:
$(2,\,14) = 2\cdot(1,\,7)$. The rows are linearly dependent, so the rank of $B$ is 1 rather than 2.

## Conclusion

| Matrix | Determinant | Invertible? |
|:------:|:-----------:|:-----------:|
| $A$ | $22$ | ✅ Yes |
| $B$ | $0$ | ❌ No |

Only $A$ is invertible. Its inverse is

$$
A^{-1} = \frac{1}{22}\begin{pmatrix} 4 & 2 \\ -5 & 3 \end{pmatrix}
$$
