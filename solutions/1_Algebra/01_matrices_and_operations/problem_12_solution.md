## Solution

### Computing $`A^2`$, $`A^3`$, $`A^4`$

```math
A^2=\begin{pmatrix}1&1\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}
=\begin{pmatrix}1&2\\0&1\end{pmatrix}
```

```math
A^3=A^2A=\begin{pmatrix}1&2\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}
=\begin{pmatrix}1&3\\0&1\end{pmatrix}
```

```math
A^4=A^3A=\begin{pmatrix}1&3\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}
=\begin{pmatrix}1&4\\0&1\end{pmatrix}
```

### Conjecture

The top-right entry equals the exponent, so

```math
A^n=\begin{pmatrix}1&n\\0&1\end{pmatrix}\qquad (n\ge 1)
```

### Proof by induction

**Base case** ($`n=1`$): $`A^1=\begin{pmatrix}1&1\\0&1\end{pmatrix}=A`$, so the formula holds.

**Inductive step.** Assume the formula holds for some $`n`$:

```math
A^n=\begin{pmatrix}1&n\\0&1\end{pmatrix}
```

Multiply by $`A`$:

```math
A^{n+1}=A^nA=\begin{pmatrix}1&n\\0&1\end{pmatrix}\begin{pmatrix}1&1\\0&1\end{pmatrix}
=\begin{pmatrix}1\cdot1+n\cdot0 & 1\cdot1+n\cdot1\\0\cdot1+1\cdot0 & 0\cdot1+1\cdot1\end{pmatrix}
=\begin{pmatrix}1&n+1\\0&1\end{pmatrix}
```

This is exactly the formula with $`n`$ replaced by $`n+1`$. Hence, by
