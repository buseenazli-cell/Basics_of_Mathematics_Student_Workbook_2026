# Problem Statement

For 

$$A=\begin{pmatrix}1&2&0\\0&3&1\\2&1&1\end{pmatrix}$$ 

compute $\det A$. Then form a matrix $B$ by swapping the first and second rows of $A$. First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

---

## Solution

### 1. Computation of $\det A$

We compute $\det A$ by Laplace expansion along the **first row** (or first column), taking advantage of the zero entry in row 1:

$$\det A = a_{11} C_{11} + a_{12} C_{12} + a_{13} C_{13}$$

* **Entry $a_{11} = 1$:**
  $$M_{11} = \det \begin{pmatrix} 3 & 1 \\ 1 & 1 \end{pmatrix} = (3)(1) - (1)(1) = 3 - 1 = 2$$
  $$a_{11} C_{11} = 1 \cdot (+1) \cdot 2 = 2$$

* **Entry $a_{12} = 2$:**
  $$M_{12} = \det \begin{pmatrix} 0 & 1 \\ 2 & 1 \end{pmatrix} = (0)(1) - (1)(2) = 0 - 2 = -2$$
  $$a_{12} C_{12} = 2 \cdot (-1) \cdot (-2) = 4$$

* **Entry $a_{13} = 0$:**
  $$a_{13} C_{13} = 0$$

Summing these terms:

$$\det A = 2 + 4 + 0 = 6$$

---

### 2. Construction of Matrix $B$ and Prediction of $\det B$

Swapping row 1 and row 2 of $A$ yields matrix $B$:

$$B = \begin{pmatrix}0&3&1\\1&2&0\\2&1&1\end{pmatrix}$$

**Prediction using Determinant Property:**
A fundamental property of determinants states that swapping any two rows (or columns) of a square matrix multiplies its determinant by $-1$:

$$\det(B) = -\det(A)$$

Since $\det A = 6$, we predict that:

$$\det B = -6$$

---

### 3. Verification of Prediction by Direct Calculation

We compute $\det B$ directly by cofactor expansion along its **first row**:

$$\det B = b_{11} C_{11} + b_{12} C_{12} + b_{13} C_{13}$$

* **Entry $b_{11} = 0$:**
  $$b_{11} C_{11} = 0$$

* **Entry $b_{12} = 3$:**
  $$M_{12} = \det \begin{pmatrix} 1 & 0 \\ 2 & 1 \end{pmatrix} = (1)(1) - (0)(2) = 1 - 0 = 1$$
  $$b_{12} C_{12} = 3 \cdot (-1) \cdot 1 = -3$$

* **Entry $b_{13} = 1$:**
  $$M_{13} = \det \begin{pmatrix} 1 & 2 \\ 2 & 1 \end{pmatrix} = (1)(1) - (2)(2) = 1 - 4 = -3$$
  $$b_{13} C_{13} = 1 \cdot (+1) \cdot (-3) = -3$$

Summing the terms gives:

$$\det B = 0 + (-3) + (-3) = -6$$

### Conclusion

The direct calculation confirms $\det B = -6$, which matches our prediction based on the row-swap property of determinants.
