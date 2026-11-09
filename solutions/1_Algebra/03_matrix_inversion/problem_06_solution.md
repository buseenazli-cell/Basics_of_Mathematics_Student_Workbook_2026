# Exercise 6 — Solving a Linear System Using the Inverse

## 1. Problem Statement

Solve the following system of linear equations using the inverse matrix method:

\[
2x+y=5
\]

\[
x+3y=7
\]

## 2. Theoretical Background and Concepts

A system of linear equations can be represented as

\[
Ax=b
\]

If \(A\) is invertible, multiply both sides by \(A^{-1}\):

\[
A^{-1}Ax=A^{-1}b
\]

Since \(A^{-1}A=I\),

\[
x=A^{-1}b
\]

## 3. Detailed Step-by-Step Solution

Write the system in matrix form:

\[
A=
\begin{pmatrix}
2 & 1 \\
1 & 3
\end{pmatrix},
\qquad
b=
\begin{pmatrix}
5\\
7
\end{pmatrix}
\]

First, calculate the determinant:

\[
\det(A)=2(3)-1(1)=5
\]

Since the determinant is not zero, the inverse exists.

Calculate the inverse:

\[
A^{-1}=
\frac15
\begin{pmatrix}
3 & -1\\
-1 & 2
\end{pmatrix}
\]

Now calculate \(x=A^{-1}b\):

\[
x=
\frac15
\begin{pmatrix}
3 & -1\\
-1 & 2
\end{pmatrix}
\begin{pmatrix}
5\\
7
\end{pmatrix}
\]

\[
x=
\frac15
\begin{pmatrix}
15-7\\
-5+14
\end{pmatrix}
\]

\[
x=
\frac15
\begin{pmatrix}
8\\
9
\end{pmatrix}
\]

Therefore,

\[
\boxed{x=\frac85,\qquad y=\frac95}
\]

## 4. Verification and Consistency Checks

Substitute the values into the original equations.

First equation:

\[
2\left(\frac85\right)+\frac95
=\frac{16}{5}+\frac95
=\frac{25}{5}=5
\]

Second equation:

\[
\frac85+3\left(\frac95\right)
=\frac85+\frac{27}{5}
=\frac{35}{5}=7
\]

Both equations are satisfied.

Therefore, the solution is correct.
