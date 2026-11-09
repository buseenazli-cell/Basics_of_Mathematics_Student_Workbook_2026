# Exercise 2 — Finding an Inverse Using the Formula

## 1. Problem Statement

Given the matrix

\[
A = \begin{pmatrix} 3 & 2 \\ 5 & 4 \end{pmatrix}
\]

Find its inverse using the \(2 \times 2\) inverse formula.

## 2. Theoretical Background and Concepts

For a matrix

\[
A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}
\]

the determinant is

\[
\det(A) = ad-bc
\]

If the determinant is not zero, the inverse exists and is calculated as

\[
A^{-1} =
\frac{1}{ad-bc}
\begin{pmatrix} d & -b \\ -c & a \end{pmatrix}
\]

## 3. Detailed Step-by-Step Solution

First, calculate the determinant:

\[
\det(A) = 3(4)-2(5)
\]

\[
\det(A) = 12-10=2
\]

Since the determinant is not zero, the inverse exists.

Now substitute the values into the inverse formula:

\[
A^{-1} =
\frac{1}{2}
\begin{pmatrix} 4 & -2 \\ -5 & 3 \end{pmatrix}
\]

Multiply each element by \(1/2\):

\[
\boxed{
A^{-1} =
\begin{pmatrix}
2 & -1 \\
-\frac{5}{2} & \frac{3}{2}
\end{pmatrix}
}
\]

## 4. Verification and Consistency Checks

Multiply \(A\) by its inverse:

\[
AA^{-1} =
\begin{pmatrix} 3 & 2 \\ 5 & 4 \end{pmatrix}
\begin{pmatrix} 2 & -1 \\ -\frac{5}{2} & \frac{3}{2} \end{pmatrix}
\]

\[
=
\begin{pmatrix}
6-5 & -3+3 \\
10-10 & -5+6
\end{pmatrix}
\]

\[
AA^{-1} =
\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}
= I
\]

The result is the identity matrix, so the inverse is correct.
