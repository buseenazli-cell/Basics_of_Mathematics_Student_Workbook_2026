# Exercise 12 — Properties of Inverse Matrices

## 1. Problem Statement

Given

\[
A^{-1}=
\begin{pmatrix}
2 & -1\\
-3 & 2
\end{pmatrix}
\]

Find the following matrices:

1. \((3A)^{-1}\)
2. \((A^T)^{-1}\)
3. \((A^2)^{-1}\)

## 2. Theoretical Background and Concepts

Several important inverse matrix properties are used in this exercise.

**Scalar multiplication:**

\[
(kA)^{-1}=\frac{1}{k}A^{-1}
\]

for \(k\neq0\).

**Transpose:**

\[
(A^T)^{-1}=(A^{-1})^T
\]

**Matrix powers:**

\[
(A^n)^{-1}=(A^{-1})^n
\]

These properties allow us to calculate inverses without finding the original matrix first.

## 3. Detailed Step-by-Step Solution

### Part 1: Find \((3A)^{-1}\)

Using the scalar multiplication property:

\[
(3A)^{-1}=\frac13A^{-1}
\]

Substitute the given matrix:

\[
(3A)^{-1}
=
\frac13
\begin{pmatrix}
2 & -1\\
-3 & 2
\end{pmatrix}
\]

Therefore,

\[
\boxed{
(3A)^{-1}
=
\begin{pmatrix}
\frac23 & -\frac13\\
-1 & \frac23
\end{pmatrix}
}
\]

### Part 2: Find \((A^T)^{-1}\)

Using the transpose property:

\[
(A^T)^{-1}=(A^{-1})^T
\]

Transpose the given inverse:

\[
(A^T)^{-1}
=
\begin{pmatrix}
2 & -3\\
-1 & 2
\end{pmatrix}
\]

Therefore,

\[
\boxed{
(A^T)^{-1}
=
\begin{pmatrix}
2 & -3\\
-1 & 2
\end{pmatrix}
}
\]

### Part 3: Find \((A^2)^{-1}\)

Using the matrix power property:

\[
(A^2)^{-1}=(A^{-1})^2
\]

Calculate:

\[
(A^{-1})^2
=
\begin{pmatrix}
2 & -1\\
-3 & 2
\end{pmatrix}
\begin{pmatrix}
2 & -1\\
-3 & 2
\end{pmatrix}
\]

\[
=
\begin{pmatrix}
4+3 & -2-2\\
-6-6 & 3+4
\end{pmatrix}
\]

Therefore,

\[
\boxed{
(A^2)^{-1}
=
\begin{pmatrix}
7 & -4\\
-12 & 7
\end{pmatrix}
}
\]

## 4. Verification and Consistency Checks

The results follow directly from the inverse matrix properties.

For scalar multiplication:

\[
(3A)\left(\frac13A^{-1}\right)=I
\]

For the transpose:

\[
A^T(A^{-1})^T=(A^{-1}A)^T=I
\]

For the matrix square:

\[
A^2(A^{-1})^2
=A(AA^{-1})A^{-1}
=AA^{-1}
=I
\]

All three results satisfy the corresponding inverse matrix properties.
