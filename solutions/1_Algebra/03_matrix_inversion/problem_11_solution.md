# Exercise 11 — Parameter Values for Invertibility

## 1. Problem Statement

Consider the matrix

\[
A(t)=
\begin{pmatrix}
1 & t\\
t & 1
\end{pmatrix}
\]

Determine the values of \(t\) for which the matrix is invertible.

Find its inverse when it exists.

## 2. Theoretical Background and Concepts

A square matrix is invertible if and only if its determinant is not zero.

For a \(2 \times 2\) matrix,

\[
\det(A)=ad-bc
\]

The inverse is

\[
A^{-1}=
\frac{1}{\det(A)}
\begin{pmatrix}
d & -b\\
-c & a
\end{pmatrix}
\]

## 3. Detailed Step-by-Step Solution

First, calculate the determinant:

\[
\det(A(t))=1(1)-t(t)
\]

\[
\det(A(t))=1-t^2
\]

The matrix is invertible when

\[
1-t^2\neq0
\]

Factor the expression:

\[
(1-t)(1+t)\neq0
\]

Therefore,

\[
t\neq1
\]

and

\[
t\neq-1
\]

The matrix is invertible for all real values of \(t\), except \(t=1\) and \(t=-1\).

Now calculate the inverse:

\[
A(t)^{-1}
=
\frac{1}{1-t^2}
\begin{pmatrix}
1 & -t\\
-t & 1
\end{pmatrix}
\]

Thus,

\[
\boxed{
A(t)^{-1}
=
\frac{1}{1-t^2}
\begin{pmatrix}
1 & -t\\
-t & 1
\end{pmatrix},
\quad t\neq\pm1
}
\]

## 4. Verification and Consistency Checks

Multiply the matrix by its inverse:

\[
A(t)A(t)^{-1}
=
\frac{1}{1-t^2}
\begin{pmatrix}
1 & t\\
t & 1
\end{pmatrix}
\begin{pmatrix}
1 & -t\\
-t & 1
\end{pmatrix}
\]

\[
=
\frac{1}{1-t^2}
\begin{pmatrix}
1-t^2 & 0\\
0 & 1-t^2
\end{pmatrix}
\]

\[
=
\begin{pmatrix}
1 & 0\\
0 & 1
\end{pmatrix}
=I
\]

This verification is valid when \(t\neq\pm1\).

At \(t=1\) and \(t=-1\), the determinant is zero, so the inverse does not exist.
