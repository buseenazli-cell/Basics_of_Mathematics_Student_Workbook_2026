## Solution

Compute both products:

```math
AB=\begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}a&b\\c&d\end{pmatrix}
=\begin{pmatrix}a+c&b+d\\c&d\end{pmatrix}
```

```math
BA=\begin{pmatrix}a&b\\c&d\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}
=\begin{pmatrix}a&a+b\\c&c+d\end{pmatrix}
```

### Conditions for $`AB=BA`$

Compare the entries:

| Entry | $`AB`$ | $`BA`$ | Condition |
|:---:|:---:|:---:|:---:|
| $`(1,1)`$ | $`a+c`$ | $`a`$ | $`c=0`$ |
| $`(1,2)`$ | $`b+d`$ | $`a+b`$ | $`d=a`$ |
| $`(2,1)`$ | $`c`$ | $`c`$ | always true |
| $`(2,2)`$ | $`d`$ | $`c+d`$ | $`c=0`$ |

Therefore

```math
AB=BA \iff c=0 \ \text{ and } \ d=a
```

while $`a`$ and $`b`$ are arbitrary.

### General form of $`B`$

```math
B=\begin{pmatrix}a&b\\0&a\end{pmatrix}
=a\begin{pmatrix}1&0\\0&1\end{pmatrix}+b\begin{pmatrix}0&1\\0&0\end{pmatrix}
=aI+bN,\qquad a,b\in\mathbb{R}
```

where $`N=\begin{pmatrix}0&1\\0&0\end{pmatrix}`$. Note that $`A=I+N`$,
