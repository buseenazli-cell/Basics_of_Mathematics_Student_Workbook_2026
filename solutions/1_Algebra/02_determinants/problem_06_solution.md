# Problem Statement

For 

$$A(t)=\begin{pmatrix}t&1\\2&t\end{pmatrix}$$ 

find all values of $t$ for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

---

## Solution

### 1. Calculation of the Determinant

A square matrix $A(t)$ is parameterized by $t$. We compute its determinant using the standard formula for a $2 \times 2$ matrix, $\det \begin{pmatrix} a & b \\ c & d \end{pmatrix} = ad - bc$:

$$\det A(t) = (t)(t) - (1)(2) = t^2 - 2$$

---

### 2. Finding the Values of $t$ for Non-Invertibility

A square matrix is **not invertible** (also called singular) if and only if its determinant is equal to zero:

$$\det A(t) = 0$$

Setting our expression for the determinant to zero gives:

$$t^2 - 2 = 0$$

Solving for $t$:

$$t^2 = 2 \implies t = \pm\sqrt{2}$$

Thus, the matrix $A(t)$ is not invertible for **$t = \sqrt{2}$** and **$t = -\sqrt{2}$**.

---

### 3. Explanation of the Relationship to $\det A(t) = 0$

The invertibility of a matrix depends directly on whether its determinant is non-zero due to the following core algebraic and geometric properties:

1. **Algebraic Property (Formula for Inverse):**  
   The formula for the inverse of a $2 \times 2$ matrix $M = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$ is given by:
   $$M^{-1} = \frac{1}{\det M} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}$$
   If $\det A(t) = 0$, computing $A(t)^{-1}$ would require dividing by zero ($\frac{1}{0}$), which is mathematically undefined. Therefore, no inverse matrix exists when the determinant is zero.

2. **Geometric Property (Linear Independence and Area):**  
   The absolute value of $\det A(t)$ represents the scaling factor by which the transformation $A(t)$ alters areas in $\mathbb{R}^2$.
   * When $t = \pm\sqrt{2}$, the determinant becomes zero, meaning the two rows (and columns) of $A(t)$ become linearly dependent scalar multiples of each other.
   * For example, at $t = \sqrt{2}$, Row 2 ($\begin{pmatrix}2 & \sqrt{2}\end{pmatrix}$) is exactly $\sqrt{2}$ times Row 1 ($\begin{pmatrix}\sqrt{2} & 1\end{pmatrix}$).
   * Geometrically, this linear dependence collapses the 2D plane onto a 1D line, shrinking all areas to $0$. Since a line cannot be uniquely mapped back into a 2D plane, the operation is non-reversible (non-invertible).

---

### Conclusion

The matrix $A(t)$ fails to be invertible precisely when **$t = \pm\sqrt{2}$**, because these are the exact values that cause $\det A(t) = 0$.
