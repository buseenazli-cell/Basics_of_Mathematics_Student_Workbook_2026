# Exercise 1 — Definition of the Inverse

## 1. Problem Statement

Given the matrices

\[
A = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix},
\qquad
B = \begin{pmatrix} 1 & -1 \\ -1 & 2 \end{pmatrix}
\]

Determine whether \(B\) is the inverse of \(A\).

## 2. Theoretical Background and Concepts

A square matrix \(B\) is the inverse of a square matrix \(A\) if

\[
AB = BA = I
\]

where \(I\) is the identity matrix.

For a \(2 \times 2\) matrix, the identity matrix is

\[
I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}
\]

## 3. Detailed Step-by-Step Solution

First, calculate \(AB\):

\[
AB =
\begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}
\begin{pmatrix} 1 & -1 \\ -1 & 2 \end{pmatrix}
\]

\[
AB =
\begin{pmatrix}
2(1)+1(-1) & 2(-1)+1(2) \\
1(1)+1(-1) & 1(-1)+1(2)
\end{pmatrix}
\]

\[
AB =
\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}
= I
\]

Now calculate \(BA\):

\[
BA =
\begin{pmatrix} 1 & -1 \\ -1 & 2 \end{pmatrix}
\begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}
\]

\[
BA =
\begin{pmatrix}
1(2)+(-1)(1) & 1(1)+(-1)(1) \\
(-1)(2)+2(1) & (-1)(1)+2(1)
\end{pmatrix}
\]

\[
BA =
\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}
= I
\]

## 4. Verification and Consistency Checks

Both matrix products give the identity matrix:

\[
AB = I
\]

\[
BA = I
\]

Therefore,

\[
\boxed{B = A^{-1}}
\]

The matrix \(B\) is the inverse of \(A\).
