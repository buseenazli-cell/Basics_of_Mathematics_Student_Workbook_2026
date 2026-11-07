# Exercise 4. Matrix Multiplication and Noncommutativity

## Question

For

$$A=\begin{pmatrix}1&2\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}2&0\\3&1\end{pmatrix}$$

compute $AB$ and $BA$. Is $AB=BA$? Use this example to explain what noncommutativity of matrix multiplication means.

## Solution

**Method.** The entry in row $i$ and column $j$ of a product is the sum of products of the entries of row $i$ of the left matrix with the corresponding entries of column $j$ of the right matrix.

**Computing $AB$.**

$$AB=\begin{pmatrix}1&2\\0&1\end{pmatrix}\begin{pmatrix}2&0\\3&1\end{pmatrix}
=\begin{pmatrix}1\cdot2+2\cdot3 & 1\cdot0+2\cdot1\\ 0\cdot2+1\cdot3 & 0\cdot0+1\cdot1\end{pmatrix}
=\begin{pmatrix}8&2\\3&1\end{pmatrix}.$$

**Computing $BA$.**

$$BA=\begin{pmatrix}2&0\\3&1\end{pmatrix}\begin{pmatrix}1&2\\0&1\end{pmatrix}
=\begin{pmatrix}2\cdot1+0\cdot0 & 2\cdot2+0\cdot1\\ 3\cdot1+1\cdot0 & 3\cdot2+1\cdot1\end{pmatrix}
=\begin{pmatrix}2&4\\3&7\end{pmatrix}.$$

**Comparison.** Since

$$AB=\begin{pmatrix}8&2\\3&1\end{pmatrix}\neq\begin{pmatrix}2&4\\3&7\end{pmatrix}=BA,$$

we have $AB\neq BA$ (they differ in three of the four entries).

**Meaning of noncommutativity.** Both products are defined and have the same size, yet the order of the factors changes the result. For numbers, $ab=ba$ always; for matrices, $AB=BA$ is a special property that holds only for some pairs, not a rule. In this example, $AB$ and $BA$ are different matrices, so we must always keep the factors in the given order and may not swap them when simplifying expressions.
