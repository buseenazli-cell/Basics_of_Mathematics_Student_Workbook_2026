# Exercise 9 — Solving a Matrix Equation

## 1. Problem Statement

Given the matrix equation

\[
AX=B
\]

where

\[
A=
\begin{pmatrix}
1 & 2\\
0 & 1
\end{pmatrix},
\qquad
B=
\begin{pmatrix}
3 & 1\\
2 & 4
\end{pmatrix}
\]

Find the unknown matrix \(X\).

## 2. Theoretical Background and Concepts

To solve a matrix equation

\[
AX=B
\]

multiply both sides from the left by \(A^{-1}\):

\[
A^{-1}AX=A^{-1}B
\]

Since \(A^{-1}A=I\),

\[
X=A^{-1}B
\]

## 3. Detailed Step-by-Step Solution

First, calculate the determinant of \(A\):

\[
\det(A)=1(1)-2(0)=1
\]

Since the determinant is not zero, \(A^{-1}\) exists.

Calculate the inverse:

\[
A^{-1}=
\begin{pmatrix}
1 & -2\\
0 & 1
\end{pmatrix}
\]

Now calculate \(X=A^{-1}B\):

\[
X=
\begin{pmatrix}
1 & -2\\
0 & 1
\end{pmatrix}
\begin{pmatrix}
3 & 1\\
2 & 4
\end{pmatrix}
\]

\[
X=
\begin{pmatrix}
3-4 & 1-8\\
2 & 4
\end{pmatrix}
\]

Therefore,

\[
\boxed{
X=
\begin{pmatrix}
-1 & -7\\
2 & 4
\end{pmatrix}
}
\]

## 4. Verification and Consistency Checks

Substitute the result into the original equation:

\[
AX=
\begin{pmatrix}
1 & 2\\
0 & 1
\end{pmatrix}
\begin{pmatrix}
-1 & -7\\
2 & 4
\end{pmatrix}
\]

\[
AX=
\begin{pmatrix}
-1+4 & -7+8\\
2 & 4
\end{pmatrix}
\]

\[
AX=
\begin{pmatrix}
3 & 1\\
2 & 4
\end{pmatrix}
=B
\]

The original equation is satisfied.

Therefore, the calculated matrix \(X\) is correct.
