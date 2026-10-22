# Exercise 13

## Question

Let

$$
F = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}
$$

Compute $F^2, F^3, F^4, F^5$, observe the pattern, and explain how it is related to the Fibonacci numbers $1, 1, 2, 3, 5, 8, \dots$

## Solution

### Computing F squared

Each entry is a row of the left factor times a column of the right factor:

$$
F^2 = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}\begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}
= \begin{pmatrix} 1\cdot 1 + 1\cdot 1 & 1\cdot 1 + 1\cdot 0 \\ 1\cdot 1 + 0\cdot 1 & 1\cdot 1 + 0\cdot 0 \end{pmatrix}
= \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}
$$

### A reusable update rule

To get the next power we multiply by $F$ on the right. A row $(u, v)$ becomes

$$
(u, v)\begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = (u\cdot 1 + v\cdot 1,\; u\cdot 1 + v\cdot 0) = (u + v,\; u)
$$

So the new first entry is the sum of the old two, and the new second entry is the old first entry. For example, going from $F^2$ to $F^3$:

$$
(2, 1) \mapsto (2+1,\, 2) = (3, 2), \qquad (1, 1) \mapsto (1+1,\, 1) = (2, 1)
$$

### The remaining powers

$$
F^3 = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}, \qquad
F^4 = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix}, \qquad
F^5 = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}
$$

### Pattern

Every power contains consecutive Fibonacci numbers:

$$
F^n = \begin{pmatrix} f_{n+1} & f_n \\ f_n & f_{n-1} \end{pmatrix}
$$

where $f_1 = f_2 = 1$ and $f_{k+1} = f_k + f_{k-1}$. The update rule above is exactly this recurrence: each new row is the sum of the two previous Fibonacci numbers followed by the larger of the two.
