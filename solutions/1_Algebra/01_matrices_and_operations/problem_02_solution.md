# Exercise 2

## Problem Statement

For 

$$A=\begin{pmatrix}1&2\\-1&3\end{pmatrix},\qquad B=\begin{pmatrix}4&-2\\0&5\end{pmatrix}$$

compute $A+B$, $A-B$, and $3A-2B$. Explain why matrix addition is possible only for matrices of the same size.

---

## Solution

### 1. Computation of $A+B$

Matrix addition is performed entrywise by adding corresponding elements of $A$ and $B$:

$$A+B = \begin{pmatrix}1&2\\-1&3\end{pmatrix} + \begin{pmatrix}4&-2\\0&5\end{pmatrix} = \begin{pmatrix} 1+4 & 2+(-2) \\ -1+0 & 3+5 \end{pmatrix} = \begin{pmatrix}5&0\\-1&8\end{pmatrix}$$

---

### 2. Computation of $A-B$

Matrix subtraction is performed entrywise by subtracting corresponding elements of $B$ from $A$:

$$A-B = \begin{pmatrix}1&2\\-1&3\end{pmatrix} - \begin{pmatrix}4&-2\\0&5\end{pmatrix} = \begin{pmatrix} 1-4 & 2-(-2) \\ -1-0 & 3-5 \end{pmatrix} = \begin{pmatrix}-3&4\\-1&-2\end{pmatrix}$$

---

### 3. Computation of $3A-2B$

First, scalar multiplication is applied to both matrices by multiplying every entry of $A$ by $3$ and every entry of $B$ by $2$:

$$3A = 3\begin{pmatrix}1&2\\-1&3\end{pmatrix} = \begin{pmatrix}3&6\\-3&9\end{pmatrix}$$

$$2B = 2\begin{pmatrix}4&-2\\0&5\end{pmatrix} = \begin{pmatrix}8&-4\\0&10\end{pmatrix}$$

Now, subtracting $2B$ from $3A$:

$$3A-2B = \begin{pmatrix}3&6\\-3&9\end{pmatrix} - \begin{pmatrix}8&-4\\0&10\end{pmatrix} = \begin{pmatrix} 3-8 & 6-(-4) \\ -3-0 & 9-10 \end{pmatrix} = \begin{pmatrix}-5&10\\-3&-1\end{pmatrix}$$

---

### 4. Why Matrix Addition Requires Same Sizes

Matrix addition is defined component-wise (or entry-by-entry), meaning the entry in row $i$ and column $j$ of the sum matrix $A+B$ is defined as:

$$(A+B)_{ij} = a_{ij} + b_{ij}$$

For this operation to be mathematically defined, every entry $a_{ij}$ in $A$ must have a corresponding entry $b_{ij}$ in $B$. If two matrices have different dimensions (different numbers of rows or columns), there will be entries in one matrix with no corresponding entry in the other. Consequently, addition (and subtraction) is undefined unless both matrices have the exact same size ($m \times n$).
