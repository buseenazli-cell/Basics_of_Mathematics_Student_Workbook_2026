# Exercise 1 — Determinant of a 2×2 Matrix

## Problem Statement

Compute 

$$\det\begin{pmatrix}3&-2\\5&4\end{pmatrix},\qquad \det\begin{pmatrix}1&7\\2&14\end{pmatrix}.$$ 

Which matrix is invertible? Justify your answer.

---

## Solution

The determinant of a general $2 \times 2$ matrix $M = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$ is given by the formula:

$$\det(M) = ad - bc$$

---

### 1. Computation of First Determinant

Let $A = \begin{pmatrix}3&-2\\5&4\end{pmatrix}$. Applying the $2 \times 2$ determinant formula:

$$\det(A) = (3)(4) - (-2)(5) = 12 - (-10) = 12 + 10 = 22$$

---

### 2. Computation of Second Determinant

Let $B = \begin{pmatrix}1&7\\2&14\end{pmatrix}$. Applying the $2 \times 2$ determinant formula:

$$\det(B) = (1)(14) - (7)(2) = 14 - 14 = 0$$

---

### 3. Invertibility Analysis

A square matrix is **invertible** (non-singular) if and only if its determinant is non-zero ($\det \neq 0$).

* For matrix $A$: $\det(A) = 22 \neq 0$, so **matrix $A$ is invertible**.
* For matrix $B$: $\det(B) = 0$, so **matrix $B$ is singular (not invertible)**.

**Justification:** 
The invertibility of a matrix requires its rows (or columns) to be linearly independent. In matrix $B$, the second row $\begin{pmatrix}2 & 14\end{pmatrix}$ is exactly twice the first row $\begin{pmatrix}1 & 7\end{pmatrix}$, making the rows linearly dependent and causing the area of the transformed unit square (the determinant) to collapse to zero. Because $\det(B) = 0$, an inverse matrix $B^{-1}$ does not exist. Conversely, since $\det(A) = 22 \neq 0$, $A$ preserves a non-zero area scale factor and thus possesses a unique matrix inverse $A^{-1}$.
