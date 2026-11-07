# Exercise 15. Associativity of Multiplication and Different Calculation Paths

## Question

Given

$$A=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix},\quad B=\begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix},\quad C=\begin{pmatrix}2&1\\0&-1\end{pmatrix}.$$

Compute $(AB)C$ and $A(BC)$. Compare the results and the number of intermediate operations. Explain what associativity of matrix multiplication means in this example.

## Solution

**Method.** Sizes: $A$ is $2\times3$, $B$ is $3\times2$, $C$ is $2\times2$. Both groupings are defined. Each entry of a product is a row-column sum.

### Grouping 1: $(AB)C$

$AB$ has size $2\times2$:

$$\begin{aligned}
(AB)_{11}&=1\cdot1+2\cdot2+0\cdot(-1)=5, & (AB)_{12}&=1\cdot0+2\cdot1+0\cdot3=2,\\
(AB)_{21}&=0\cdot1+1\cdot2+1\cdot(-1)=1, & (AB)_{22}&=0\cdot0+1\cdot1+1\cdot3=4.
\end{aligned}$$

$$AB=\begin{pmatrix}5&2\\1&4\end{pmatrix}.$$

Then

$$(AB)C=\begin{pmatrix}5&2\\1&4\end{pmatrix}\begin{pmatrix}2&1\\0&-1\end{pmatrix}
=\begin{pmatrix}5\cdot2+2\cdot0&5\cdot1+2\cdot(-1)\\1\cdot2+4\cdot0&1\cdot1+4\cdot(-1)\end{pmatrix}
=\begin{pmatrix}10&3\\2&-3\end{pmatrix}.$$

### Grouping 2: $A(BC)$

$BC$ has size $3\times2$:

$$\begin{aligned}
(BC)_{11}&=1\cdot2+0\cdot0=2, & (BC)_{12}&=1\cdot1+0\cdot(-1)=1,\\
(BC)_{21}&=2\cdot2+1\cdot0=4, & (BC)_{22}&=2\cdot1+1\cdot(-1)=1,\\
(BC)_{31}&=-1\cdot2+3\cdot0=-2, & (BC)_{32}&=-1\cdot1+3\cdot(-1)=-4.
\end{aligned}$$

$$BC=\begin{pmatrix}2&1\\4&1\\-2&-4\end{pmatrix}.$$

Then

$$A(BC)=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix}\begin{pmatrix}2&1\\4&1\\-2&-4\end{pmatrix}
=\begin{pmatrix}1\cdot2+2\cdot4+0\cdot(-2)&1\cdot1+2\cdot1+0\cdot(-4)\\0\cdot2+1\cdot4+1\cdot(-2)&0\cdot1+1\cdot1+1\cdot(-4)\end{pmatrix}
=\begin{pmatrix}10&3\\2&-3\end{pmatrix}.$$

### Comparison of the results

$$(AB)C=A(BC)=\begin{pmatrix}10&3\\2&-3\end{pmatrix}.$$

### Comparison of the number of operations

A product of an $m\times n$ matrix by an $n\times p$ matrix has $mp$ entries, each needing $n$ multiplications and $n-1$ additions. We count all scalar operations, including those involving zero entries.

| Step | Size | Multiplications | Additions |
|---|---|---|---|
| $AB$ | $(2\times3)(3\times2)$ | $4\cdot3=12$ | $4\cdot2=8$ |
| $(AB)C$ | $(2\times2)(2\times2)$ | $4\cdot2=8$ | $4\cdot1=4$ |
| **Total for $(AB)C$** | | **20** | **12** |
| $BC$ | $(3\times2)(2\times2)$ | $6\cdot2=12$ | $6\cdot1=6$ |
| $A(BC)$ | $(2\times3)(3\times2)$ | $4\cdot3=12$ | $4\cdot2=8$ |
| **Total for $A(BC)$** | | **24** | **14** |

So $(AB)C$ needs fewer scalar operations ($20$ vs. $24$ multiplications, $12$ vs. $14$ additions). The reason is the size of the intermediate matrix: $AB$ is only $2\times2$ (4 entries), while $BC$ is $3\times2$ (6 entries), so the second step of $(AB)C$ works with a smaller matrix.

### Meaning of associativity

Associativity says that $(AB)C=A(BC)$: the way we group the factors does not change the final matrix, as the identical results above show. The *order* of the factors $A,B,C$ must stay the same (matrix multiplication is not commutative), but we may choose which pair to multiply first. Since the result is the same, we can choose the cheaper path, which here is $(AB)C$.
