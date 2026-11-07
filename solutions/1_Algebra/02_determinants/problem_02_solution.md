### Exercise 2 — Matrix Determinant & Property Check

#### Problem Statement

For matrix
$$A = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 2 & 1 & 5 \end{pmatrix}$$

compute $\det A$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

> **Why this exercise:** Teaches a basic method for $3\times3$ matrices and builds the habit of checking the result without adding a second full solution.

---

#### Solution

##### Step 1: Compute $\det A$ using Sarrus' Rule

Repeat the first two columns of $A$ to the right of the matrix:

$$\begin{pmatrix}
1 & 2 & -1 & \vert & 1 & 2 \\
0 & 3 & 4 & \vert & 0 & 3 \\
2 & 1 & 5 & \vert & 2 & 1
\end{pmatrix}$$

1. **Sum of down-diagonal products (left-to-right):**
   $$D_1 = (1 \cdot 3 \cdot 5) + (2 \cdot 4 \cdot 2) + (-1 \cdot 0 \cdot 1)$$
   $$D_1 = 15 + 16 + 0 = 31$$

2. **Sum of up-diagonal products (left-to-right):**
   $$D_2 = (2 \cdot 3 \cdot -1) + (1 \cdot 4 \cdot 1) + (5 \cdot 0 \cdot 2)$$
   $$D_2 = -6 + 4 + 0 = -2$$

3. **Subtract $D_2$ from $D_1$:**
   $$\det A = D_1 - D_2 = 31 - (-2) = 31 + 2 = 33$$

---

##### Step 2: Property Check (Row Operations)

**Property:** Row replacement operations of the form $R_i \to R_i + k R_j$ do not change the value of the determinant ($\det A' = \det A$).

Apply $R_3 \to R_3 - 2R_1$ to create a zero in column 1:

$$A' = \begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
0 & -3 & 7
\end{pmatrix}$$

Now expand along the first column:

$$\det A = 1 \cdot \det \begin{pmatrix} 3 & 4 \\ -3 & 7 \end{pmatrix} - 0 + 0$$

$$\det A = (3 \cdot 7) - (4 \cdot -3) = 21 - (-12) = 21 + 12 = 33$$

Both methods independently yield **33**, confirming the result.
