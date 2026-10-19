# Exercise 4. Matrix Multiplication and Noncommutativity

## Solution

$$
A=\begin{pmatrix}1&2\\0&1\end{pmatrix},\qquad
B=\begin{pmatrix}2&0\\3&1\end{pmatrix}
$$

### Computing $AB$

$$
AB=\begin{pmatrix}1&2\\0&1\end{pmatrix}\begin{pmatrix}2&0\\3&1\end{pmatrix}
=\begin{pmatrix}
1\cdot 2+2\cdot 3 & 1\cdot 0+2\cdot 1\\
0\cdot 2+1\cdot 3 & 0\cdot 0+1\cdot 1
\end{pmatrix}
=\begin{pmatrix}8&2\\3&1\end{pmatrix}
$$

### Computing $BA$

$$
BA=\begin{pmatrix}2&0\\3&1\end{pmatrix}\begin{pmatrix}1&2\\0&1\end{pmatrix}
=\begin{pmatrix}
2\cdot 1+0\cdot 0 & 2\cdot 2+0\cdot 1\\
3\cdot 1+1\cdot 0 & 3\cdot 2+1\cdot 1
\end{pmatrix}
=\begin{pmatrix}2&4\\3&7\end{pmatrix}
$$

### Is $AB=BA$?

No:

$$
AB=\begin{pmatrix}8&2\\3&1\end{pmatrix}\neq\begin{pmatrix}2&4\\3&7\end{pmatrix}=BA.
$$

### Meaning of noncommutativity

Matrix multiplication is **noncommutative**: in general $AB\neq BA$, so the order of the factors matters. In this example, multiplying $A$ by $B$ and $B$ by $A$ give different matrices. Since a product $AB$ means "apply $B$ first, then $A$", changing the order of the transformations changes the result.

## Answer

$$
AB=\begin{pmatrix}8&2\\3&1\end{pmatrix},\qquad
BA=\begin{pmatrix}2&4\\3&7\end{pmatrix},\qquad
AB\neq BA.
$$
