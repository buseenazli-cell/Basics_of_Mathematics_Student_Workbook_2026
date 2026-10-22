# Exercise 7. Identity and Zero Matrices, and Powers of a Matrix

## Question

Let

$$
A = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}
$$

Compute $AI$, $IA$, $A+0$, $A^2$ and $A^3$, where $I$ is the $2\times 2$ identity matrix and $0$ is the $2\times 2$ zero matrix. Explain the roles of the matrices $I$ and $0$, and describe the pattern you observe in successive powers of $A$.

## Solution

### Method

Each entry of a product is obtained by pairing a row of the left matrix with a column of the right matrix: multiply corresponding entries and add. Matrix addition is done entry by entry.

### The roles of I and 0

$$
I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}, \qquad 0 = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}
$$

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
A + 0 = \begin{pmatrix} 2+0 & 1+0 \\ 0+0 & 2+0 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = A
$$

So $AI = IA = A$ and $A + 0 = A$. The identity matrix $I$ is the neutral element for multiplication: it plays the role of the number $1$. The zero matrix $0$ is the neutral element for addition: it plays the role of the number $0$. Multiplying by $I$ or adding $0$ leaves $A$ unchanged.

### Powers of A

$$
A^2 = AA = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}\begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}
= \begin{pmatrix} 2\cdot 2 + 1\cdot 0 & 2\cdot 1 + 1\cdot 2 \\ 0\cdot 2 + 2\cdot 0 & 0\cdot 1 + 2\cdot 2 \end{pmatrix}
= \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}
$$

$$
A^3 = A^2 A = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}\begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}
= \begin{pmatrix} 4\cdot 2 + 4\cdot 0 & 4\cdot 1 + 4\cdot 2 \\ 0\cdot 2 + 4\cdot 0 & 0\cdot 1 + 4\cdot 2 \end{pmatrix}
= \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}
$$

### Observed pattern

| Power | Matrix | Diagonal entries | Upper right entry |
|:-----:|:------:|:----------------:|:-----------------:|
| $A^1$ | $\begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$ | $2$ | $1$ |
| $A^2$ | $\begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}$ | $4$ | $4$ |
| $A^3$ | $\begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}$ | $8$ | $12$ |

The matrix stays upper triangular, the diagonal entries are $2, 4, 8$, that is $2^n$, and the upper right entries are $1, 4, 12$, that is $n\cdot 2^{n-1}$ (check: $1\cdot 1$, $2\cdot 2$, $3\cdot 4$). This suggests

$$
A^n = \begin{pmatrix} 2^n & n\,2^{n-1} \\ 0 & 2^n \end{pmatrix}
$$

### Why the pattern arises

Suppose the formula holds for some $n$. Multiply by $A$ once more:

$$
A^{n+1} = A^n A = \begin{pmatrix} 2^n & n\,2^{n-1} \\ 0 & 2^n \end{pmatrix}\begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}
= \begin{pmatrix} 2^n\cdot 2 + n\,2^{n-1}\cdot 0 & 2^n\cdot 1 + n\,2^{n-1}\cdot 2 \\ 0\cdot 2 + 2^n\cdot 0 & 0\cdot 1 + 2^n\cdot 2 \end{pmatrix}
$$

The diagonal entries become $2^{n+1}$, and the upper right entry is

$$
2^n + n\,2^n = (n+1)\,2^n
$$

Hence

$$
A^{n+1} = \begin{pmatrix} 2^{n+1} & (n+1)\,2^{n} \\ 0 & 2^{n+1} \end{pmatrix}
$$

which is the same formula with $n$ replaced by $n+1$. The formula holds for $n = 1$, and each step carries it to the next power, so it holds for every integer $n \geq 1$.

The same pattern can be seen by writing $A = 2I + N$ with

$$
N = \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix}, \qquad N^2 = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}
$$

Since $I$ commutes with $N$, the binomial expansion applies, and all terms containing $N^2$ or higher powers vanish:

$$
A^n = (2I + N)^n = 2^n I + n\,2^{n-1} N
$$

The factor $n$ appears because $N$ can be chosen from any one of the $n$ factors.

### Conclusion

$AI = IA = A$ and $A + 0 = A$, while

$$
A^2 = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}, \qquad A^3 = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}, \qquad A^n = \begin{pmatrix} 2^n & n\,2^{n-1} \\ 0 & 2^n \end{pmatrix}
$$
