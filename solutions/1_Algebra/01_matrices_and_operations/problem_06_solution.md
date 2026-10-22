# Exercise 6. Transpose of a Product

## Question

Let

$$
A = \begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix}
$$

Compute $A^T$, $B^T$ and $AB$. Then verify in this example that $(AB)^T = B^T A^T$.

## Solution

### Transposes

Transposition turns each row into a column. For example, the first row of $A$ is $(1, 2, 3)$, and it becomes the first column of $A^T$. The second row $(4, 5, 6)$ becomes the second column.

$$
A^T = \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix}
$$

In the same way, the rows $(1, 0)$, $(2, 1)$ and $(-1, 3)$ of $B$ become the columns of $B^T$:

$$
B^T = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \end{pmatrix}
$$

### The product AB

$A$ is $2\times 3$ and $B$ is $3\times 2$, so $AB$ is defined and has size $2\times 2$. Each entry is a row of $A$ paired with a column of $B$: multiply corresponding entries and add.

$$
AB = \begin{pmatrix} 1\cdot 1 + 2\cdot 2 + 3\cdot(-1) & 1\cdot 0 + 2\cdot 1 + 3\cdot 3 \\ 4\cdot 1 + 5\cdot 2 + 6\cdot(-1) & 4\cdot 0 + 5\cdot 1 + 6\cdot 3 \end{pmatrix}
= \begin{pmatrix} 1 + 4 - 3 & 0 + 2 + 9 \\ 4 + 10 - 6 & 0 + 5 + 18 \end{pmatrix}
= \begin{pmatrix} 2 & 11 \\ 8 & 23 \end{pmatrix}
$$

Its transpose swaps the off-diagonal entries:

$$
(AB)^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}
$$

### The product B^T A^T

The identity says that the transpose of a product is the product of the transposes in reversed order, so we compute $B^T A^T$ (not $A^T B^T$). Here $B^T$ is $2\times 3$ and $A^T$ is $3\times 2$, so the result is $2\times 2$. Again each entry is a row-column sum:

$$
B^T A^T = \begin{pmatrix} 1\cdot 1 + 2\cdot 2 + (-1)\cdot 3 & 1\cdot 4 + 2\cdot 5 + (-1)\cdot 6 \\ 0\cdot 1 + 1\cdot 2 + 3\cdot 3 & 0\cdot 4 + 1\cdot 5 + 3\cdot 6 \end{pmatrix}
= \begin{pmatrix} 1 + 4 - 3 & 4 + 10 - 6 \\ 0 + 2 + 9 & 0 + 5 + 18 \end{pmatrix}
= \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}
$$

### Comparison

$$
(AB)^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix} = B^T A^T
$$

All four entries agree. The sums are the same numbers in a different arrangement: for instance, the (1,2) entry of $B^T A^T$ pairs the first row of $B^T$ (the first column of $B$) with the second column of $A^T$ (the second row of $A$), which is exactly the (2,1) entry of $AB$.

### Conclusion

In this example, $(AB)^T = B^T A^T$ holds. This is a check on one example, not a general proof of the theorem.
