## Solution

### Route 1: $`(AB)C`$

**Step 1: compute $`AB`$** ($`2\times3`$ times $`3\times2`$ gives $`2\times2`$)

```math
AB=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix}\begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix}
=\begin{pmatrix}
1\cdot1+2\cdot2+0\cdot(-1) & 1\cdot0+2\cdot1+0\cdot3\\
0\cdot1+1\cdot2+1\cdot(-1) & 0\cdot0+1\cdot1+1\cdot3
\end{pmatrix}
=\begin{pmatrix}5&2\\1&4\end{pmatrix}
```

**Step 2: multiply by $`C`$**

```math
(AB)C=\begin{pmatrix}5&2\\1&4\end{pmatrix}\begin{pmatrix}2&1\\0&-1\end{pmatrix}
=\begin{pmatrix}
5\cdot2+2\cdot0 & 5\cdot1+2\cdot(-1)\\
1\cdot2+4\cdot0 & 1\cdot1+4\cdot(-1)
\end{pmatrix}
=\begin{pmatrix}10&3\\2&-3\end{pmatrix}
```

### Route 2: $`A(BC)`$

**Step 1: compute $`BC`$** ($`3\times2`$ times $`2\times2`$ gives $`3\times2`$)

```math
BC=\begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix}\begin{pmatrix}2&1\\0&-1\end{pmatrix}
=\begin{pmatrix}
1\cdot2+0\cdot0 & 1\cdot1+0\cdot(-1)\\
2\cdot2+1\cdot0 & 2\cdot1+1\cdot(-1)\\
-1\cdot2+3\cdot0 & -1\cdot1+3\cdot(-1)
\end{pmatrix}
=\begin{pmatrix}2&1\\4&1\\-2&-4\end{pmatrix}
```

**Step 2: multiply $`A`$ by $`BC`$**

```math
A(BC)=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix}\begin{pmatrix}2&1\\4&1\\-2&-4\end{pmatrix}
=\begin{pmatrix}
1\cdot2+2\cdot4+0\cdot(-2) & 1\cdot1+2\cdot1+0\cdot(-4)\\
0\cdot2+1\cdot4+1\cdot(-2) & 0\cdot1+1\cdot1+1\cdot(-4)
\end{pmatrix}
=\begin{pmatrix}10&3\\2&-3\end{pmatrix}
```

### Comparison of the results

```math
(AB)C=\begin{pmatrix}10&3\\2&-3\end{pmatrix}=A(BC)
```

Both groupings give the same $`2\times2`$ matrix.

### Comparison of the number of operations

Each entry of a product of an $`m\times n`$ and an $`n\times p`$ matrix needs $`n`$ multiplications and $`n-1`$ additions. Zeros are counted like any other entry.

| Route | Step | Size | Multiplications | Additions |
|:---:|:---:|:---:|:---:|:---:|
| $`(AB)C`$ | $`AB`$ | $`2\times3\cdot3\times2`$ | $`4\cdot3=12`$ | $`4\cdot2=8`$ |
| | $`(AB)C`$ | $`2\times2\cdot2\times2`$ | $`4\cdot2=8`$ | $`4\cdot1=4`$ |
| | **Total** | | **20** | **12** |
| $`A(BC)`$ | $`BC`$ | $`3\times2\cdot2\times2`$ | $`6\cdot2=12`$ | $`6\cdot1=6`$ |
| | $`A(BC)`$ | $`2\times3\cdot3\times2`$ | $`4\cdot3=12`$ | $`4\cdot2=8`$ |
| | **Total** | | **24** | **14** |

The final matrices are equal, but $`(AB)C`$ is cheaper here (20 against 24 multiplications). The reason is that $`AB`$ is only $`2\times2`$, while $`BC`$ is $`3\times2`$ and is larger.

### What associativity means here

Associativity says that the grouping of the factors does not change the product:

```math
(AB)C=A(BC)
```

- **Same result.** The parentheses only decide which two matrices are multiplied first. Both routes compute the same matrix $`ABC`$, so the brackets can be dropped and we can simply write $`ABC`$.
- **Linear map view.** Take a vector $`x\in\mathbb{R}^2`$. Then $`C`$ sends $`x`$ to $`Cx`$, $`B`$ sends that to $`BCx\in\mathbb{R}^3`$, and $`A`$ sends it to $`ABCx\in\mathbb{R}^2`$. In both routes the same three maps are applied in the same order, $`C`$ first, then $`B`$, then $`A`$:

```math
\big((AB)C\big)x=(AB)(Cx)=A\big(B(Cx)\big)=A\big((BC)x\big)=\big(A(BC)\big)x
```

  The grouping only decides whether we combine two maps into one matrix first, not what happens to $`x`$.
- **Order is still fixed.** Associativity allows moving the brackets, not the matrices. $`ABC`$ is in general different from $`ACB`$ or $`CBA`$, since matrix multiplication is not commutative (and here $`AC`$ is not even defined, because $`A`$ has 3 columns and $`C`$ has 2 rows).
- **Practical use.** Since the result does not depend on the grouping, we can choose the grouping with the fewest operations, as the table above shows.
