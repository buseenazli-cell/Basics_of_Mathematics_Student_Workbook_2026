# Exercise 15

## Problem Statement

Given 

$$A=\begin{pmatrix}1&2&0\\0&1&1\end{pmatrix},\quad B=\begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix},\quad C=\begin{pmatrix}2&1\\0&-1\end{pmatrix}.$$ 

Compute $(AB)C$ and $A(BC)$. Compare the results and the number of intermediate operations. Explain what associativity of matrix multiplication means in this example.

---

## Solution

### 1. Computation of $(AB)C$

First, we compute the intermediate product $AB$. $A$ is a $2 \times 3$ matrix and $B$ is a $3 \times 2$ matrix, so $AB$ is a $2 \times 2$ matrix:

$$AB = \begin{pmatrix}1&2&0\\0&1&1\end{pmatrix} \begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix}$$

Calculating each entry by taking the dot product of rows of $A$ and columns of $B$:
- $(AB)_{11} = 1(1) + 2(2) + 0(-1) = 1 + 4 + 0 = 5$
- $(AB)_{12} = 1(0) + 2(1) + 0(3) = 0 + 2 + 0 = 2$
- $(AB)_{21} = 0(1) + 1(2) + 1(-1) = 0 + 2 - 1 = 1$
- $(AB)_{22} = 0(0) + 1(1) + 1(3) = 0 + 1 + 3 = 4$

Thus,
$$AB = \begin{pmatrix}5&2\\1&4\end{pmatrix}$$

Now, we multiply $(AB)$ by $C$:

$$(AB)C = \begin{pmatrix}5&2\\1&4\end{pmatrix} \begin{pmatrix}2&1\\0&-1\end{pmatrix}$$

- $((AB)C)_{11} = 5(2) + 2(0) = 10 + 0 = 10$
- $((AB)C)_{12} = 5(1) + 2(-1) = 5 - 2 = 3$
- $((AB)C)_{21} = 1(2) + 4(0) = 2 + 0 = 2$
- $((AB)C)_{22} = 1(1) + 4(-1) = 1 - 4 = -3$

So,
$$(AB)C = \begin{pmatrix}10&3\\2&-3\end{pmatrix}$$

---

### 2. Computation of $A(BC)$

First, we compute the intermediate product $BC$. $B$ is a $3 \times 2$ matrix and $C$ is a $2 \times 2$ matrix, so $BC$ is a $3 \times 2$ matrix:

$$BC = \begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix} \begin{pmatrix}2&1\\0&-1\end{pmatrix}$$

Calculating each entry:
- $(BC)_{11} = 1(2) + 0(0) = 2 + 0 = 2$
- $(BC)_{12} = 1(1) + 0(-1) = 1 + 0 = 1$
- $(BC)_{21} = 2(2) + 1(0) = 4 + 0 = 4$
- $(BC)_{22} = 2(1) + 1(-1) = 2 - 1 = 1$
- $(BC)_{31} = -1(2) + 3(0) = -2 + 0 = -2$
- $(BC)_{32} = -1(1) + 3(-1) = -1 - 3 = -4$

Thus,
$$BC = \begin{pmatrix}2&1\\4&1\\-2&-4\end{pmatrix}$$

Now, we multiply $A$ by $(BC)$:

$$A(BC) = \begin{pmatrix}1&2&0\\0&1&1\end{pmatrix} \begin{pmatrix}2&1\\4&1\\-2&-4\end{pmatrix}$$

- $(A(BC))_{11} = 1(2) + 2(4) + 0(-2) = 2 + 8 + 0 = 10$
- $(A(BC))_{12} = 1(1) + 2(1) + 0(-4) = 1 + 2 + 0 = 3$
- $(A(BC))_{21} = 0(2) + 1(4) + 1(-2) = 0 + 4 - 2 = 2$
- $(A(BC))_{22} = 0(1) + 1(1) + 1(-4) = 0 + 1 - 4 = -3$

So,
$$A(BC) = \begin{pmatrix}10&3\\2&-3\end{pmatrix}$$

---

### 3. Comparison of Results

Comparing both expressions:

$$(AB)C = A(BC) = \begin{pmatrix}10&3\\2&-3\end{pmatrix}$$

Both groupings yield the exact same final matrix, illustrating the associativity property of matrix multiplication.

---

### 4. Comparison of Intermediate Operations

In matrix multiplication of an $m \times n$ matrix and an $n \times p$ matrix:
- Number of scalar multiplications = $m \cdot n \cdot p$
- Number of scalar additions = $m \cdot (n - 1) \cdot p$
- Total arithmetic operations = $m \cdot (2n - 1) \cdot p$

*(Note: Scalar operations involving zero entries are included in standard dense operations counts).*

| Operation Grouping | First Multiplication | Second Multiplication | Total Scalar Multiplications | Total Scalar Additions | Total Scalar Operations |
| :--- | :--- | :--- | :---: | :---: | :---: |
| **$(AB)C$** | $AB$: $(2 \times 3) \times (3 \times 2) \implies 2 \cdot 3 \cdot 2 = 12$ mults, $2 \cdot 2 \cdot 2 = 8$ adds | $(AB)C$: $(2 \times 2) \times (2 \times 2) \implies 2 \cdot 2 \cdot 2 = 8$ mults, $2 \cdot 1 \cdot 2 = 4$ adds | $12 + 8 = \mathbf{20}$ | $8 + 4 = \mathbf{12}$ | $\mathbf{32}$ |
| **$A(BC)$** | $BC$: $(3 \times 2) \times (2 \times 2) \implies 3 \cdot 2 \cdot 2 = 12$ mults, $3 \cdot 1 \cdot 2 = 6$ adds | $A(BC)$: $(2 \times 3) \times (3 \times 2) \implies 2 \cdot 3 \cdot 2 = 12$ mults, $2 \cdot 2 \cdot 2 = 8$ adds | $12 + 12 = \mathbf{24}$ | $6 + 8 = \mathbf{14}$ | $\mathbf{38}$ |

**Conclusion on operation counts:** 
Calculating $(AB)C$ requires fewer scalar operations ($32$ total scalar operations) than $A(BC)$ ($38$ total scalar operations). This is because computing $AB$ first creates a smaller $2 \times 2$ intermediate matrix, whereas computing $BC$ first produces a larger $3 \times 2$ intermediate matrix.

---

### 5. Associativity Meaning in Matrix Multiplication

In linear algebra, associativity means that when multiplying three (or more) matrices in sequence, the **grouping of operations does not change the final result**, provided that the order of the matrices remains the same:

$$(AB)C = A(BC)$$

Geometrically, each matrix represents a linear transformation. $C$ transforms vectors, $B$ transforms the result, and $A$ transforms that result. Associativity guarantees that whether we first combine $A$ and $B$ into a composite transformation $(AB)$ or combine $B$ and $C$ into $(BC)$, applying them sequentially to any vector yields the exact same final vector. Furthermore, computationally, it allows us to choose the grouping that requires fewer arithmetic operations without affecting numerical correctness.
