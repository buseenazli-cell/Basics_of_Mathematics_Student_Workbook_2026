# Exercise 13. Powers of the Fibonacci Matrix

## Question

Let

$$
F = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}
$$

Compute $F^2$, $F^3$, $F^4$ and $F^5$, observe the pattern, and explain how it is related to the Fibonacci numbers $1, 1, 2, 3, 5, 8, \dots$

## Solution

### Method

Each entry of a product is a row of the left factor paired with a column of the right factor: multiply corresponding entries and add. We multiply by $F$ on the right to get each next power.

### Computing F squared

$$
F^2 = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}\begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}
= \begin{pmatrix} 1\cdot 1 + 1\cdot 1 & 1\cdot 1 + 1\cdot 0 \\ 1\cdot 1 + 0\cdot 1 & 1\cdot 1 + 0\cdot 0 \end{pmatrix}
= \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}
$$

### A reusable update rule

Multiplying a row $(u, v)$ on the right by $F$ gives

$$
(u, v)\begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = (u\cdot 1 + v\cdot 1,\; u\cdot 1 + v\cdot 0) = (u + v,\; u)
$$

So the new first entry is the sum of the old two entries, and the new second entry is the old first entry. Since $F^{n+1} = F^n F$, this rule is applied to each row of $F^n$.

For example, going from $F^2$ to $F^3$:

$$
(2, 1) \mapsto (2 + 1,\; 2) = (3, 2), \qquad (1, 1) \mapsto (1 + 1,\; 1) = (2, 1)
$$

so

$$
F^3 = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}
$$

### The remaining powers

Applying the same rule again:

$$
F^4 = \begin{pmatrix} 3+2 & 3 \\ 2+1 & 2 \end{pmatrix} = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix}, \qquad
F^5 = \begin{pmatrix} 5+3 & 5 \\ 3+2 & 3 \end{pmatrix} = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}
$$

### Pattern and the Fibonacci numbers

Every power contains consecutive Fibonacci numbers:

$$
F^n = \begin{pmatrix} f_{n+1} & f_n \\ f_n & f_{n-1} \end{pmatrix}
$$

where $f_0 = 0$, $f_1 = f_2 = 1$ and $f_{k+1} = f_k + f_{k-1}$.

The update rule explains why. The first row of $F^n$ is $(f_{n+1}, f_n)$, and the rule turns it into $(f_{n+1} + f_n,\; f_{n+1}) = (f_{n+2}, f_{n+1})$, which is the first row of $F^{n+1}$. The addition in the rule is exactly the Fibonacci recurrence.

### Conclusion

$$
F^2 = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}, \quad
F^3 = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}, \quad
F^4 = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix}, \quad
F^5 = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}
$$
