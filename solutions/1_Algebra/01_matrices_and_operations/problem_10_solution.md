## Solution

### 1) Compute $`Ab_1`$ and $`Ab_2`$

```math
b_1=\begin{pmatrix}1\\-1\\3\end{pmatrix},\qquad
b_2=\begin{pmatrix}2\\0\\1\end{pmatrix}
```

```math
Ab_1=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix}\begin{pmatrix}1\\-1\\3\end{pmatrix}
=\begin{pmatrix}1\cdot1+2\cdot(-1)+0\cdot3\\0\cdot1+1\cdot(-1)+1\cdot3\end{pmatrix}
=\begin{pmatrix}-1\\2\end{pmatrix}
```

```math
Ab_2=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix}\begin{pmatrix}2\\0\\1\end{pmatrix}
=\begin{pmatrix}1\cdot2+2\cdot0+0\cdot1\\0\cdot2+1\cdot0+1\cdot1\end{pmatrix}
=\begin{pmatrix}2\\1\end{pmatrix}
```

### 2) Compute $`AB`$

$`A`$ is $`2\times3`$ and $`B`$ is $`3\times2`$, so $`AB`$ is $`2\times2`$.

```math
AB=\begin{pmatrix}
1\cdot1+2\cdot(-1)+0\cdot3 & 1\cdot2+2\cdot0+0\cdot1\\
0\cdot1+1\cdot(-1)+1\cdot3 & 0\cdot2+1\cdot0+1\cdot1
\end{pmatrix}
=\begin{pmatrix}-1&2\\2&1\end{pmatrix}
```

### 3) Comparison and explanation

```math
\text{column 1 of } AB=\begin{pmatrix}-1\\2\end{pmatrix}=Ab_1,\qquad
\text{column 2 of } AB=\begin{pmatrix}2\\1\end{pmatrix}=Ab_2
```

So $`AB=\begin{pmatrix}Ab_1&Ab_2\end{pmatrix}`$.

**Why this is always true.**

- **Entry rule:** The entry $`(AB)_{ij}`$ is (row $`i`$ of $`A`$) $`\cdot`$ (column $`j`$ of $`B`$). For a fixed $`j`$, the entries of column $`j`$ of $`AB`$ are the dot products of every row of $`A`$ with $`b_j`$. That is exactly the vector $`Ab_j`$.
- **Linear map view:** Let $`e_j`$ be the $`j`$-th standard basis vector. Then $`Be_j=b_j`$, so $`(AB)e_j=A(Be_j)=Ab_j`$. Multiplying by $`e_j`$ picks out column $`j`$, so column $`j`$ of $`AB`$ is $`Ab_j`$.
- **Meaning:** Applying $`B`$ and then $`A`$ to the basis vector $`e_j`$ gives $`Ab_j`$. The columns of $`AB`$ record where the basis vectors go under the combined transformation.

Each $`Ab_j`$ is also a combination of the columns of $`A`$ with the entries of $`b_j`$ as weights. For example, $`Ab_1=1\cdot a_1-1\cdot a_2+3\cdot a_3=\begin{pmatrix}-1\\2\end{pmatrix}`$.
