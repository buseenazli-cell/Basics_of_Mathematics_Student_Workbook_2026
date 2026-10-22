# Determinant of a 3×3 Matrix via Sarrus' Rule

$$
A = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 2 & 1 & 5 \end{pmatrix}
$$

## Sarrus' Rule

Rewrite the first two columns to the right of the matrix:

$$
\begin{array}{ccc|cc}
1 & 2 & -1 & 1 & 2 \\
0 & 3 & 4 & 0 & 3 \\
2 & 1 & 5 & 2 & 1
\end{array}
$$

**Downward diagonals (added):**

$$
1\cdot 3\cdot 5 + 2\cdot 4\cdot 2 + (-1)\cdot 0\cdot 1 = 15 + 16 + 0 = 31
$$

**Upward diagonals (subtracted):**

$$
(-1)\cdot 3\cdot 2 + 1\cdot 4\cdot 1 + 2\cdot 0\cdot 5 = -6 + 4 + 0 = -2
$$

**Result:**

$$
\det A = 31 - (-2) = 33
$$

## Check Using a Determinant Property

**Property:** Adding a multiple of one row to another row does **not** change the determinant. The determinant of a triangular matrix is the product of its diagonal entries.

Apply $R_3 \to R_3 - 2R_1$:

$$
\begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 0 & -3 & 7 \end{pmatrix}
$$

Apply $R_3 \to R_3 + R_2$:

$$
\begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 0 & 0 & 11 \end{pmatrix}
$$

This matrix is upper triangular, so

$$
\det A = 1\cdot 3\cdot 11 = 33 \quad\checkmark
$$

## Conclusion

$$
\boxed{\det A = 33}
$$

Since $\det A \neq 0$, the matrix $A$ is invertible.
