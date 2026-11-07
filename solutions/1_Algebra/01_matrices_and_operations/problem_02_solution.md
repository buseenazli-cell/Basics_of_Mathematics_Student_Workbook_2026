## Exercise 2 — Determinant of a 3×3 Matrix

### Problem Statement

Given the matrix:

\[
A =
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5
\end{pmatrix}
\]

Calculate the determinant of matrix \(A\) using **Sarrus' Rule**. Verify your result using the **cofactor expansion method**.

### Solution

**1. Using Sarrus' Rule**

Repeat the first two columns:

\[
\begin{vmatrix}
1 & 2 & -1 & 1 & 2\\
0 & 3 & 4 & 0 & 3\\
2 & 1 & 5 & 2 & 1
\end{vmatrix}
\]

Sum of the downward diagonals:

\[
(1 \cdot 3 \cdot 5) +
(2 \cdot 4 \cdot 2) +
(-1 \cdot 0 \cdot 1)
\]

\[
=15+16+0=31
\]

Sum of the upward diagonals:

\[
(-1 \cdot 3 \cdot 2) +
(1 \cdot 4 \cdot 1) +
(2 \cdot 0 \cdot 5)
\]

\[
=-6+4+0=-2
\]

Therefore:

\[
\det(A)=31-(-2)=33
\]

**2. Verification Using Cofactor Expansion**

Expanding along the first row:

\[
\det(A)=
1\begin{vmatrix}3&4\\1&5\end{vmatrix}
-2\begin{vmatrix}0&4\\2&5\end{vmatrix}
+(-1)\begin{vmatrix}0&3\\2&1\end{vmatrix}
\]

\[
=1(15-4)-2(0-8)+(-1)(0-6)
\]

\[
=11+16+6
\]

\[
\boxed{\det(A)=33}
\]

### Final Answer

Both Sarrus' Rule and cofactor expansion produce the same result:

\[
\boxed{\det(A)=33}
\]

This confirms that the determinant calculation is correct.
