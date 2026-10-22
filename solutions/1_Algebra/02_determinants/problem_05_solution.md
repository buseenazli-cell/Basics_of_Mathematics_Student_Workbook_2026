# Problem Statement

For 

$$A=\begin{pmatrix}1&2&3\\2&1&0\\-1&4&2\end{pmatrix}$$ 

find $\det A$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

---

## Solution

To compute $\det A$ using row operations, we apply Gaussian elimination to reduce $A$ to an upper triangular matrix $U$. We track how each type of elementary row operation affects the determinant based on the following properties:

1. **Row Addition ($R_i \leftarrow R_i + k R_j$):** Does **not change** the determinant ($\det = \det$).
2. **Row Swap ($R_i \leftrightarrow R_j$):** Multiplies the determinant by **$-1$**.
3. **Row Scaling ($R_i \leftarrow k R_i$):** Multiplies the determinant by **$k$**.

---

### Step 1: Create zeros in Column 1 below the pivot

We start with the initial matrix:

$$A = \begin{pmatrix}1&2&3\\2&1&0\\-1&4&2\end{pmatrix}$$

We eliminate the entries below $a_{11} = 1$:
* Apply $R_2 \leftarrow R_2 - 2R_1$
* Apply $R_3 \leftarrow R_3 + R_1$

Since row addition operations do not change the determinant, $\det A$ remains unchanged:

$$\det A = \det \begin{pmatrix} 1 & 2 & 3 \\ 2 - 2(1) & 1 - 2(2) & 0 - 2(3) \\ -1 + 1 & 4 + 2 & 2 + 3 \end{pmatrix} = \det \begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 6 & 5 \end{pmatrix}$$

* **Determinant effect:** $\det A = \det A_1$, where $A_1 = \begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 6 & 5 \end{pmatrix}$.

---

### Step 2: Create zero in Column 2 below the pivot

Next, we eliminate the entry below $a_{22} = -3$ in row 3:
* Apply $R_3 \leftarrow R_3 + 2R_2$

Again, this is a row addition operation ($R_i \leftarrow R_i + k R_j$), so it does **not change** the determinant:

$$\det A = \det \begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 6 + 2(-3) & 5 + 2(-6) \end{pmatrix} = \det \begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 0 & -7 \end{pmatrix}$$

We have now transformed $A$ into an upper triangular matrix:

$$U = \begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 0 & -7 \end{pmatrix}$$

* **Determinant effect:** Since only row additions were performed throughout the process, $\det A = \det U$.

---

### Step 3: Compute the Determinant of the Upper Triangular Matrix

The determinant of an upper triangular matrix is the product of its main diagonal elements:

$$\det U = (1) \cdot (-3) \cdot (-7) = 21$$

### Conclusion

Since no row swaps or scalar multiplications of rows were performed, the determinant remained invariant at every step:

$$\det A = \det U = 21$$
