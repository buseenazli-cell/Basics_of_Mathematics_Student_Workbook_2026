## Solution

### Computing $`F^2`$, $`F^3`$, $`F^4`$, $`F^5`$

```math
F^2=\begin{pmatrix}1&1\\1&0\end{pmatrix}\begin{pmatrix}1&1\\1&0\end{pmatrix}
=\begin{pmatrix}2&1\\1&1\end{pmatrix}
```

```math
F^3=F^2F=\begin{pmatrix}2&1\\1&1\end{pmatrix}\begin{pmatrix}1&1\\1&0\end{pmatrix}
=\begin{pmatrix}3&2\\2&1\end{pmatrix}
```

```math
F^4=F^3F=\begin{pmatrix}3&2\\2&1\end{pmatrix}\begin{pmatrix}1&1\\1&0\end{pmatrix}
=\begin{pmatrix}5&3\\3&2\end{pmatrix}
```

```math
F^5=F^4F=\begin{pmatrix}5&3\\3&2\end{pmatrix}\begin{pmatrix}1&1\\1&0\end{pmatrix}
=\begin{pmatrix}8&5\\5&3\end{pmatrix}
```

### Comparison with the Fibonacci sequence

Let $`F_0=0,\ F_1=1,\ F_2=1,\ F_3=2,\ F_4=3,\ F_5=5,\ F_6=8,\ \dots`$

| Power | Matrix | In terms of Fibonacci numbers |
|:---:|:---:|:---:|
| $`F^1`$ | $`\begin{pmatrix}1&1\\1&0\end{pmatrix}`$ | $`\begin{pmatrix}F_2&F_1\\F_1&F_0\end{pmatrix}`$ |
| $`F^2`$ | $`\begin{pmatrix}2&1\\1&1\end{pmatrix}`$ | $`\begin{pmatrix}F_3&F_2\\F_2&F_1\end{pmatrix}`$ |
| $`F^3`$ | $`\begin{pmatrix}3&2\\2&1\end{pmatrix}`$ | $`\begin{pmatrix}F_4&F_3\\F_3&F_2\end{pmatrix}`$ |
| $`F^4`$ | $`\begin{pmatrix}5&3\\3&2\end{pmatrix}`$ | $`\begin{pmatrix}F_5&F_4\\F_4&F_3\end{pmatrix}`$ |
| $`F^5`$ | $`\begin{pmatrix}8&5\\5&3\end{pmatrix}`$ | $`\begin{pmatrix}F_6&F_5\\F_5&F_4\end{pmatrix}`$ |

The entries of every power are consecutive Fibonacci numbers. The observed pattern is

```math
F^n=\begin{pmatrix}F_{n+1}&F_n\\F_n&F_{n-1}\end{pmatrix}\qquad (n\ge 1)
```

The off-diagonal entries equal $`F_n`$, the top-left entry is $`F_{n+1}`$, and the bottom-right entry is $`F_{n-1}`$.

### Multiplying a vector by $`F`$

```math
F\begin{pmatrix}a\\b\end{pmatrix}
=\begin{pmatrix}1&1\\1&0\end{pmatrix}\begin{pmatrix}a\\b\end{pmatrix}
=\begin{pmatrix}a+b\\a\end{pmatrix}
```

### Why this is one recurrence step

Take two consecutive Fibonacci numbers as the vector $`\begin{pmatrix}F_{k+1}\\F_k\end{pmatrix}`$, that is $`a=F_{k+1}`$ and $`b=F_k`$. Then

```math
F\begin{pmatrix}F_{k+1}\\F_k\end{pmatrix}
=\begin{pmatrix}F_{k+1}+F_k\\F_{k+1}\end{pmatrix}
=\begin{pmatrix}F_{k+2}\\F_{k+1}\end{pmatrix}
```

- **First row** $`(1,\ 1)`$: creates the sum of the two consecutive terms, $`a+b=F_{k+1}+F_k=F_{k+2}`$. This is the new term.
- **Second row** $`(1,\ 0)`$: keeps the first term, $`a=F_{k+1}`$, and discards $`b`$. This is the term that must be remembered for the next step.

So the new pair is again two consecutive terms, and the step can be repeated. Starting from $`\begin{pmatrix}F_1\\F_0\end{pmatrix}=\begin{pmatrix}1\\0\end{pmatrix}`$:

```math
F^n\begin{pmatrix}1\\0\end{pmatrix}=\begin{pmatrix}F_{n+1}\\F_n\end{pmatrix}
```

This explains the matrix powers above: $`F^n`$ applies the recurrence step $`n`$ times, and its first column is $`\begin{pmatrix}F_{n+1}\\F_n\end{pmatrix}`$.

### Check by induction

If $`F^n=\begin{pmatrix}F_{n+1}&F_n\\F_n&F_{n-1}\end{pmatrix}`$, then

```math
F^{n+1}=F^nF=\begin{pmatrix}F_{n+1}+F_n&F_{n+1}\\F_n+F_{n-1}&F_n\end{pmatrix}
=\begin{pmatrix}F_{n+2}&F_{n+1}\\F_{n+1}&F_n\end{pmatrix}
```

which is the formula for $`n+1`$.
