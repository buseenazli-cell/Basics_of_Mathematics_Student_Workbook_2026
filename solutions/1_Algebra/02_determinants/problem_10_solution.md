# Exercise — Row Dependence and Determinants

## 1. Problem Statement

Without carrying out a full determinant calculation, explain why 

$$\det\begin{pmatrix}1&2&3\\2&4&6\\0&1&5\end{pmatrix}=0.$$

Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

---

## 2. Theoretical Background and Concepts

1. **Linear Dependence of Rows:**  
   A set of row vectors is linearly dependent if at least one row can be expressed as a scalar multiple or linear combination of the other rows.

2. **Zero Determinant Property:**  
   If a square matrix has linearly dependent rows (or columns), its determinant is identically zero ($\det A = 0$). Specifically, if one row is a scalar multiple of another ($R_j = k R_i$), the determinant vanishes.

3. **Invertibility Criterion:**  
   A square matrix $A$ is **invertible** if and only if its determinant is non-zero ($\det A \neq 0$). Consequently, if $\det A = 0$, the matrix is **non-invertible** (singular), meaning its rows do not span the full space and its associated linear transformation collapses dimensions.

---

## 3. Detailed Step-by-Step Solution

Let the given matrix be $A$:

$$A = \begin{pmatrix}1&2&3\\2&4&6\\0&1&5\end{pmatrix}$$

We denote the rows of $A$ as:
* $R_1 = \begin{pmatrix} 1 & 2 & 3 \end{pmatrix}$
* $R_2 = \begin{pmatrix} 2 & 4 & 6 \end{pmatrix}$
* $R_3 = \begin{pmatrix} 0 & 1 & 5 \end{pmatrix}$

### Step 1: Identifying Linear Dependence

Comparing $R_1$ and $R_2$ entry by entry:

$$R_2 = \begin{pmatrix} 2 & 4 & 6 \end{pmatrix} = 2 \cdot \begin{pmatrix} 1 & 2 & 3 \end{pmatrix} = 2 R_1$$

Row 2 is an exact scalar multiple of Row 1 ($R_2 = 2R_1$). Therefore, the rows of matrix $A$ are **linearly dependent**.

### Step 2: Explaining Why $\det A = 0$

By the properties of determinants, applying the elementary row operation $R_2 \leftarrow R_2 - 2R_1$ does not change the value of the determinant:

$$\det A = \det \begin{pmatrix} 1 & 2 & 3 \\ 2 - 2(1) & 4 - 2(2) & 6 - 2(3) \\ 0 & 1 & 5 \end{pmatrix} = \det \begin{pmatrix} 1 & 2 & 3 \\ 0 & 0 & 0 \\ 0 & 1 & 5 \end{pmatrix}$$

Since the modified matrix contains an entire row of zeros ($R_2 = \mathbf{0}$), expanding along Row 2 gives:

$$\det A = 0$$

### Step 3: Connection to Non-Invertibility

Because $R_2 = 2R_1$, Row 2 provides no independent direction in $\mathbb{R}^3$. As a result:

1. **Rank Deficiency:** The rank of matrix $A$ is at most $2$, which is strictly less than its dimension ($n = 3$).
2. **Singularity:** By the Invertible Matrix Theorem, a matrix is invertible if and only if its rank equals its dimension ($\text{rank}(A) = n$) or equivalently $\det A \neq 0$.
3. **Geometric Collapse:** The linear transformation represented by $A$ maps 3D space onto a 2D plane (or line), flattening volume to zero. Because information is lost during this collapse, the transformation cannot be uniquely reversed, rendering matrix $A$ **non-invertible** (singular).

---

## 4. Verification and Consistency Checks

* **Linear Dependence Check:**  
  $$2 R_1 - R_2 + 0 R_3 = 2\begin{pmatrix}1&2&3\end{pmatrix} - \begin{pmatrix}2&4&6\end{pmatrix} + \begin{pmatrix}0&0&0\end{pmatrix} = \begin{pmatrix}0&0&0\end{pmatrix}$$  
  Since non-zero scalar coefficients exist that sum the rows to the zero vector, linear dependence is rigorously verified.

* **Determinant Property Consistency:**  
  * Row dependence $\implies$ Zero determinant ($\det A = 0$).
  * Zero determinant ($\det A = 0$) $\implies$ Non-invertibility ($A^{-1}$ does not exist).
  * All theoretical criteria align consistently without requiring explicit Sarrus or cofactor calculations.
