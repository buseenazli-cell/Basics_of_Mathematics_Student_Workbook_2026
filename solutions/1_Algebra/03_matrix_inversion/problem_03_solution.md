# Exercise 3 — Singular Matrix

## 1. Problem Statement

Given the matrix

\[
A = \begin{pmatrix} 2 & 4 \\ 1 & 2 \end{pmatrix}
\]

Determine whether the matrix has an inverse. Explain your answer.

## 2. Theoretical Background and Concepts

A square matrix is invertible if and only if its determinant is not zero.

If

\[
\det(A)=0
\]

the matrix is called singular and does not have an inverse.

For a \(2 \times 2\) matrix,

\[
\det(A)=ad-bc
\]

## 3. Detailed Step-by-Step Solution

Calculate the determinant:

\[
\det(A)=2(2)-4(1)
\]

\[
\det(A)=4-4=0
\]

Since the determinant is zero, the matrix is singular.

We can also observe that the first row is twice the second row:

\[
(2,4)=2(1,2)
\]

Therefore, the rows are linearly dependent.

## 4. Verification and Consistency Checks

The determinant is

\[
\det(A)=0
\]

This means that the matrix does not have full rank and cannot be inverted.

\[
\boxed{A^{-1}\text{ does not exist}}
\]

The matrix is singular.
