# Exercise 7

## Question

Let

$$
A = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}
$$

Compute $AI$, $IA$, $A+0$, $A^2$ and $A^3$, where $I$ is the $2\times 2$ identity matrix and $0$ is the $2\times 2$ zero matrix. Explain the roles of $I$ and $0$, and describe the pattern observed in the powers of $A$.

## Solution

### Roles of I and 0

The identity matrix $I$ is the neutral element for multiplication, and the zero matrix $0$ is the neutral element for addition.

$$
AI = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}
= \begin{pmatrix} 2\cdot 1 + 1\cdot 0 & 2\cdot 0 + 1\cdot 1 \\ 0\cdot 1 + 2\cdot 0 & 0\cdot 0 + 2\cdot 1 \end{pmatrix}
= \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = A
$$

$$
IA = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}
= \begin{pmatrix} 1\cdot 2 + 0\cdot 0 & 1\cdot 1 + 0\cdot 2 \\ 0\cdot 2 + 1\cdot 0 & 0\cdot 1 + 1\cdot 2 \end{pmatrix}
= \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = A
$$

$$
A + 0 = \begin{pmatrix} 2+0 & 1+0 \\ 0+0 & 2+0 \end{pmatrix} = A
$$

Multiplying by $I$ or adding $0$ leaves $A$ unchanged.

### Powers of A

Each entry of a product is the sum of products of a row of the left matrix with a column of the right matrix.

$$
A^2 = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}\begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}
= \begin{pmatrix} 2\cdot 2 + 1\cdot 0 & 2\cdot 1 + 1\cdot 2 \\ 0\cdot 2 + 2\cdot 0 & 0\cdot 1 + 2\cdot 2 \end{pmatrix}
= \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}
$$

$$
A^3 = A^2 A = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}\begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}
= \begin{pmatrix} 4\cdot 2 + 4\cdot 0 & 4\cdot 1 + 4\cdot 2 \\ 0\cdot 2 + 4\cdot 0 & 0\cdot 1 + 4\cdot 2 \end{pmatrix}
= \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}
$$

### Pattern

The diagonal entries are $2, 4, 8$, that is $2^n$. The upper right entries are $1, 4, 12$, that is $n\cdot 2^{n-1}$:

$$
A^n = \begin{pmatrix} 2^n & n\,2^{n-1} \\ 0 & 2^n \end{pmatrix}
$$

Check: for $n=2$, $2\cdot 2 = 4$. For $n=3$, $3\cdot 4 = 12$.

### Why the pattern arises

Write $A = 2I + N$ with

$$
N = \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix}, \qquad N^2 = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}
$$

Since $I$ commutes with $N$, the binomial expansion applies, and every term containing $N^2$ or a higher power vanishes:

$$
A^n = (2I+N)^n = 2^n I + n\,2^{n-1} N
$$

which is exactly the matrix above.
