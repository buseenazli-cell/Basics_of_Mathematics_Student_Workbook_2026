# Exercise 4. Matrix Multiplication and Noncommutativity

## Question

Let

$$
A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix}
$$

Compute $AB$ and $BA$. Is $AB = BA$? Use this example to explain what noncommutativity of matrix multiplication means.

## Solution

### Method

Each entry of a product is obtained by pairing a row of the left matrix with a column of the right matrix: multiply corresponding entries and add. The entry in row $i$ and column $j$ of $XY$ uses row $i$ of $X$ and column $j$ of $Y$.

### The product AB

$$
AB = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix}
= \begin{pmatrix} 1\cdot 2 + 2\cdot 3 & 1\cdot 0 + 2\cdot 1 \\ 0\cdot 2 + 1\cdot 3 & 0\cdot 0 + 1\cdot 1 \end{pmatrix}
= \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix}
$$

### The product BA

$$
BA = \begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix}\begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}
= \begin{pmatrix} 2\cdot 1 + 0\cdot 0 & 2\cdot 2 + 0\cdot 1 \\ 3\cdot 1 + 1\cdot 0 & 3\cdot 2 + 1\cdot 1 \end{pmatrix}
= \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}
$$

### Comparison

$$
AB = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix} \neq \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix} = BA
$$

So $AB \neq BA$. They differ in three of the four entries. Only the (2,1) entry, which is $3$, happens to agree.

### Meaning of noncommutativity

Both products $AB$ and $BA$ are defined here, and both are $2\times 2$ matrices, yet they are different. Multiplication of matrices is therefore **noncommutative**: the order of the factors matters, and in general

$$
AB \neq BA
$$

This is different from multiplication of real numbers, where $ab = ba$ always. A single example with $AB \neq BA$ is enough to show that the commutative law does not hold for matrices in general.

The reason is that $AB$ and $BA$ pair different rows with different columns. In $AB$ the rows of $A$ are combined with the columns of $B$, while in $BA$ the rows of $B$ are combined with the columns of $A$, so there is no reason for the sums to coincide.

Note that this does not mean that no two matrices commute. Some pairs satisfy $XY = YX$ (for example, any matrix commutes with the identity matrix $I$), but this cannot be assumed without checking.
