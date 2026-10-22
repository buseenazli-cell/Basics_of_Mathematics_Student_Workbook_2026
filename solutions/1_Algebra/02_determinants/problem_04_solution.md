# Problem Statement

Without expanding the determinant, compute 

$$\det\begin{pmatrix}2&4&1\\0&-3&5\\0&0&7\end{pmatrix}.$$ 

State the rule for an arbitrary triangular matrix and explain it using this example.

---

## Solution

### 1. Computation of the Determinant

The given matrix is an **upper triangular matrix** because all entries below the main diagonal are zero:

$$A = \begin{pmatrix} 2 & 4 & 1 \\ 0 & -3 & 5 \\ 0 & 0 & 7 \end{pmatrix}$$

By the triangular matrix determinant rule, the determinant is simply the product of the diagonal entries:

$$\det A = (2) \cdot (-3) \cdot (7) = -42$$

---

### 2. General Rule for an Arbitrary Triangular Matrix

For any $n \times n$ triangular matrix $T$ (upper triangular, lower triangular, or diagonal):

$$T = \begin{pmatrix} 
t_{11} & t_{12} & \cdots & t_{1n} \\ 
0 & t_{22} & \cdots & t_{2n} \\ 
\vdots & \vdots & \ddots & \vdots \\ 
0 & 0 & \cdots & t_{nn} 
\end{pmatrix}$$

The determinant is equal to the product of its main diagonal elements:

$$\det T = \prod_{i=1}^{n} t_{ii} = t_{11} \cdot t_{22} \cdots t_{nn}$$

---

### 3. Explanation Using the Given Example

We can understand why this rule holds by observing what happens if we apply standard cofactor expansion along the first column iteratively:

1. **First Expansion (along Column 1):**
   In the first column, all entries below $a_{11} = 2$ are zero. Thus, the expansion reduces to a single non-zero term involving the top-left entry and its minor matrix:

   $$\det A = 2 \cdot \det \begin{pmatrix} -3 & 5 \\ 0 & 7 \end{pmatrix}$$

2. **Second Expansion (on the remaining $2 \times 2$ matrix):**
   The remaining $2 \times 2$ submatrix is also upper triangular. Calculating its determinant gives:

   $$\det \begin{pmatrix} -3 & 5 \\ 0 & 7 \end{pmatrix} = (-3)(7) - (5)(0) = (-3)(7)$$

3. **Final Result:**
   Substituting this back yields the product of all three diagonal elements:

   $$\det A = 2 \cdot (-3) \cdot 7 = -42$$

Because the zeros eliminate all off-diagonal cofactor products at every step, the determinant of any triangular matrix always collapses into the product of its main diagonal entries.
