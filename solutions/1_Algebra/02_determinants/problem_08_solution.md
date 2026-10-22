# Problem Statement

Let $A, B$ be square matrices such that $\det A = 3$ and $\det B = -5$. Compute $\det(AB)$, $\det(BA)$ and, if it exists, $\det(A^{-1}B)$. Explain why the first two results are equal even though usually $AB \neq BA$.

---

## Solution

We are given two $n \times n$ square matrices $A$ and $B$ with their respective determinants:

$$\det A = 3, \qquad \det B = -5$$

---

### 1. Computation of $\det(AB)$

* **Property:** The determinant of a product of two square matrices is equal to the product of their individual determinants:
  $$\det(AB) = \det A \cdot \det B$$

* **Calculation:**
  $$\det(AB) = (3) \cdot (-5) = -15$$

---

### 2. Computation of $\det(BA)$

* **Property:** Applying the multiplicative property of determinants again:
  $$\det(BA) = \det B \cdot \det A$$

* **Calculation:**
  $$\det(BA) = (-5) \cdot (3) = -15$$

---

### 3. Computation of $\det(A^{-1}B)$

* **Existence:** A matrix $A$ is invertible if and only if its determinant is non-zero ($\det A \neq 0$). Since $\det A = 3 \neq 0$, the inverse matrix $A^{-1}$ exists.

* **Property:** The determinant of an inverse matrix is the reciprocal of the determinant of the original matrix:
  $$\det(A^{-1}) = \frac{1}{\det A}$$

* **Calculation:** Using the product property together with the inverse property:
  $$\det(A^{-1}B) = \det(A^{-1}) \cdot \det B = \frac{1}{\det A} \cdot \det B = \frac{1}{3} \cdot (-5) = -\frac{5}{3}$$

---

### 4. Explanation: Why $\det(AB) = \det(BA)$ Even Though $AB \neq BA$

In general, matrix multiplication is non-commutative, meaning $AB \neq BA$ as matrices. The matrix $AB$ and the matrix $BA$ are usually completely different matrices with different entries.

However, their determinants are always equal ($\det(AB) = \det(BA)$) because:

1. **Scalar Commutativity:** The determinant operation converts matrices (which do not commute under multiplication) into real numbers (scalars).
2. **Real Number Properties:** Multiplication of real numbers is commutative ($x \cdot y = y \cdot x$). 

Therefore:

$$\det(AB) = \det A \cdot \det B = \det B \cdot \det A = \det(BA)$$

While matrix multiplication does not allow changing the order of matrices ($AB \neq BA$), real number multiplication allows swapping the scalar determinant values ($\det A \cdot \det B = \det B \cdot \det A$), guaranteeing that the overall determinants are always identical.

---

## Summary Table

| Expression | Applicable Determinant Property | Calculation | Final Result |
| :--- | :--- | :--- | :---: |
| **$\det(AB)$** | $\det(AB) = \det A \cdot \det B$ | $(3) \cdot (-5)$ | **$-15$** |
| **$\det(BA)$** | $\det(BA) = \det B \cdot \det A$ | $(-5) \cdot (3)$ | **$-15$** |
| **$\det(A^{-1}B)$** | $\det(A^{-1}B) = \frac{1}{\det A} \cdot \det B$ | $\frac{1}{3} \cdot (-5)$ | **$-\frac{5}{3}$** |
