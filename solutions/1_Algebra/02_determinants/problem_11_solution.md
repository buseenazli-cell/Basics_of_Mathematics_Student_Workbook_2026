# Exercise — Computing Determinant via Row Operations

## 1. Problem Statement

Compute 

$$\det\begin{pmatrix}1&2&3\\1&3&4\\1&4&6\end{pmatrix}$$

by first performing row operations that create as many zeros as possible. State which operations do not change the determinant.

---

## 2. Theoretical Background and Concepts

1. **Elementary Row Operations and Determinants:**
   - **Row Addition ($R_i \leftarrow R_i + k R_j$):** Adding a scalar multiple of one row to another **does not change** the determinant ($\det A' = \det A$).
   - **Row Swap ($R_i \leftrightarrow R_j$):** Interchanging two rows multiplies the determinant by **$-1$**.
   - **Row Scaling ($R_i \leftarrow k R_i$):** Multiplying a row by a non-zero scalar $k$ multiplies the determinant by **$k$**.

2. **Determinant of a Triangular Matrix:**
   If a matrix is reduced to an upper triangular form (all entries below the main diagonal are zero), its determinant is simply the product of its main diagonal entries:
   
   $$\det U = u_{11} \cdot u_{22} \cdots u_{nn}$$

---

## 3. Detailed Step-by-Step Solution

Let matrix $A$ be:

$$A = \begin{pmatrix}1&2&3\\1&3&4\\1&4&6\end{pmatrix}$$

### Step 1: Create zeros in Column 1

We use row addition operations ($R_i \leftarrow R_i + k R_j$) to introduce zeros below $a_{11} = 1$:
* Apply $R_2 \leftarrow R_2 - R_1$
* Apply $R_3 \leftarrow R_3 - R_1$

> **Rule:** Subtracting a multiple of one row from another **does not change** the determinant value.

$$\det A = \det \begin{pmatrix} 1 & 2 & 3 \\ 1 - 1 & 3 - 2 & 4 - 3 \\ 1 - 1 & 4 - 2 & 6 - 3 \end{pmatrix} = \det \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 2 & 3 \end{pmatrix}$$

### Step 2: Create zero in Column 2 below the second pivot

Now, we use $a_{22} = 1$ as a pivot to eliminate the entry below it in row 3:
* Apply $R_3 \leftarrow R_3 - 2R_2$

> **Rule:** This operation is also a row addition operation ($R_3 \leftarrow R_3 + (-2)R_2$), so the determinant **remains unchanged**.

$$\det A = \det \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 2 - 2(1) & 3 - 2(1) \end{pmatrix} = \det \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 0 & 1 \end{pmatrix}$$

### Step 3: Compute the Determinant of the Triangular Matrix

The matrix is now in **upper triangular form**:

$$U = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 0 & 1 \end{pmatrix}$$

Since only row addition operations were used throughout the entire reduction process, $\det A = \det U$.

Multiplying the diagonal elements:

$$\det A = (1) \cdot (1) \cdot (1) = 1$$

---

## 4. Verification and Consistency Checks

* **Operations Summary:**  
  The operations performed were $R_2 \leftarrow R_2 - R_1$, $R_3 \leftarrow R_3 - R_1$, and $R_3 \leftarrow R_3 - 2R_2$. All of these are row addition operations ($R_i \leftarrow R_i + k R_j$), which **do not change the determinant**.

* **Verification via Cofactor Expansion (along Column 1):**  
  Expanding the reduced matrix along the first column:
  
  $$\det A = 1 \cdot \det \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = 1 \cdot ((1)(1) - (1)(0)) = 1$$

* **Verification via Sarrus' Rule on Original Matrix $A$:**  
  $$\det A = (1\cdot 3\cdot 6 + 2\cdot 4\cdot 1 + 3\cdot 1\cdot 4) - (3\cdot 3\cdot 1 + 2\cdot 1\cdot 6 + 1\cdot 4\cdot 4)$$
  $$\det A = (18 + 8 + 12) - (9 + 12 + 16) = 38 - 37 = 1$$

All methods yield the exact same result ($\det A = 1$), verifying both the step-by-step reduction and the consistency of the final value.
