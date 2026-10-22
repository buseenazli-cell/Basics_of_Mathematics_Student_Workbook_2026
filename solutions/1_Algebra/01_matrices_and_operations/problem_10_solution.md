# Exercise 10. Columns of a Product

## Question

Given

$$
A = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & 2 \\ -1 & 0 \\ 3 & 1 \end{pmatrix}
$$

denote the columns of $B$ by $b_1$ and $b_2$.

1. Compute $Ab_1$ and $Ab_2$.
2. Compute the matrix $AB$.
3. Compare the results and explain why the columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$.

## Solution

### Method

Each entry of a matrix-vector product is a row of the matrix paired with the vector: multiply corresponding entries and add. The same row-column rule gives the entries of a matrix-matrix product.

The columns of $B$ are

$$
b_1 = \begin{pmatrix} 1 \\ -1 \\ 3 \end{pmatrix}, \qquad b_2 = \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix}
$$

### Part 1: $Ab_1$ and $Ab_2$

$$
Ab_1 = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix}\begin{pmatrix} 1 \\ -1 \\ 3 \end{pmatrix}
= \begin{pmatrix} 1\cdot 1 + 2\cdot(-1) + 0\cdot 3 \\ 0\cdot 1 + 1\cdot(-1) + 1\cdot 3 \end{pmatrix}
= \begin{pmatrix} -1 \\ 2 \end{pmatrix}
$$

$$
Ab_2 = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix}\begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix}
= \begin{pmatrix} 1\cdot 2 + 2\cdot 0 + 0\cdot 1 \\ 0\cdot 2 + 1\cdot 0 + 1\cdot 1 \end{pmatrix}
= \begin{pmatrix} 2 \\ 1 \end{pmatrix}
$$

### Part 2: the matrix $AB$

$A$ is $2\times 3$ and $B$ is $3\times 2$, so $AB$ is defined and has size $2\times 2$.

$$
AB = \begin{pmatrix} 1\cdot 1 + 2\cdot(-1) + 0\cdot 3 & 1\cdot 2 + 2\cdot 0 + 0\cdot 1 \\ 0\cdot 1 + 1\cdot(-1) + 1\cdot 3 & 0\cdot 2 + 1\cdot 0 + 1\cdot 1 \end{pmatrix}
= \begin{pmatrix} -1 & 2 \\ 2 & 1 \end{pmatrix}
$$

### Part 3: comparison and explanation

The first column of $AB$ is $(-1, 2)^T = Ab_1$ and the second column is $(2, 1)^T = Ab_2$. So

$$
AB = \begin{pmatrix} Ab_1 & Ab_2 \end{pmatrix}
$$

**Explanation by entries.** The entry of $AB$ in row $i$ and column $j$ is

$$
(AB)_{ij} = a_{i1}b_{1j} + a_{i2}b_{2j} + a_{i3}b_{3j}
$$

Fix the column index $j$. The numbers $b_{1j}, b_{2j}, b_{3j}$ are exactly the entries of the column $b_j$. So the sum above is row $i$ of $A$ paired with $b_j$, which is the $i$-th entry of $Ab_j$. This holds for every row $i$, so column $j$ of $AB$ is $Ab_j$.

For example, $(AB)_{12} = 1\cdot 2 + 2\cdot 0 + 0\cdot 1 = 2$ is the first entry of $Ab_2$.

**Explanation by basis vectors.** Let $e_1 = (1, 0)^T$ and $e_2 = (0, 1)^T$. Multiplying a matrix by $e_j$ picks out its $j$-th column. Hence $Be_j = b_j$, and

$$
(AB)e_j = A(Be_j) = Ab_j
$$

But $(AB)e_j$ is also the $j$-th column of $AB$. So the $j$-th column of $AB$ equals $Ab_j$.

### Conclusion

$$
Ab_1 = \begin{pmatrix} -1 \\ 2 \end{pmatrix}, \qquad Ab_2 = \begin{pmatrix} 2 \\ 1 \end{pmatrix}, \qquad AB = \begin{pmatrix} -1 & 2 \\ 2 & 1 \end{pmatrix}
$$

Each column of $AB$ is $A$ applied to the corresponding column of $B$.
