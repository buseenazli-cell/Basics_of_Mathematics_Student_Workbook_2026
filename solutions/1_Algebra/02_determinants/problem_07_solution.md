# Problem Statement

Suppose that for a $3 \times 3$ matrix $A$, $\det A = -4$. Compute $\det(2A)$, $\det(A^T)$, $\det(A^2)$, and $\det(-A)$. Justify each answer using the appropriate property.

---

## Solution

We are given that $A$ is an $n \times n$ square matrix with $n = 3$ and its determinant is:

$$\det A = -4$$

We compute each requested determinant using the fundamental algebraic properties of determinants.

---

### 1. Computation of $\det(2A)$

* **Property:** For any $n \times n$ matrix $A$ and scalar $c$, scaling the matrix by $c$ scales every row by $c$, which multiplies the determinant by $c^n$:
  $$\det(cA) = c^n \cdot \det A$$

* **Calculation:** Here $c = 2$ and $n = 3$:
  $$\det(2A) = 2^3 \cdot \det A = 8 \cdot (-4) = -32$$

---

### 2. Computation of $\det(A^T)$

* **Property:** Transposing a matrix interchanges its rows and columns, which leaves the value of the determinant unchanged:
  $$\det(A^T) = \det A$$

* **Calculation:**
  $$\det(A^T) = -4$$

---

### 3. Computation of $\det(A^2)$

* **Property:** The determinant of a product of matrices equals the product of their individual determinants:
  $$\det(AB) = \det A \cdot \det B$$
  Therefore, for powers of a matrix, $\det(A^k) = (\det A)^k$.

* **Calculation:**
  $$\det(A^2) = (\det A)^2 = (-4)^2 = 16$$

---

### 4. Computation of $\det(-A)$

* **Property:** The negative matrix $-A$ is equivalent to scalar multiplication by $c = -1$. Using the scalar property $\det(cA) = c^n \cdot \det A$:
  $$\det(-A) = (-1)^n \cdot \det A$$

* **Calculation:** Since $A$ is a $3 \times 3$ matrix ($n = 3$, an odd dimension):
  $$\det(-A) = (-1)^3 \cdot \det A = (-1) \cdot (-4) = 4$$

---

## Summary Table

| Expression | Applicable Determinant Property | Calculation | Final Result |
| :--- | :--- | :--- | :---: |
| **$\det(2A)$** | $\det(cA) = c^n \cdot \det A \quad (n=3, c=2)$ | $2^3 \cdot (-4) = 8 \cdot (-4)$ | **$-32$** |
| **$\det(A^T)$** | $\det(A^T) = \det A$ | $\det A$ | **$-4$** |
| **$\det(A^2)$** | $\det(A^2) = (\det A)^2$ | $(-4)^2$ | **$16$** |
| **$\det(-A)$** | $\det(-A) = (-1)^n \cdot \det A \quad (n=3)$ | $(-1)^3 \cdot (-4) = -1 \cdot (-4)$ | **$4$** |
