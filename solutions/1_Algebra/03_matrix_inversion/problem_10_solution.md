# Exercise 10 — Inverse of a Diagonal Matrix

## 1. Problem Statement

Consider the diagonal matrix

\[
D=
\begin{pmatrix}
2 & 0 & 0\\
0 & -3 & 0\\
0 & 0 & 5
\end{pmatrix}
\]

Find its inverse.

Also determine whether the following matrix has an inverse:

\[
E=
\begin{pmatrix}
2 & 0 & 0\\
0 & 0 & 0\\
0 & 0 & 5
\end{pmatrix}
\]

## 2. Theoretical Background and Concepts

A diagonal matrix is invertible if all its diagonal elements are non-zero.

The inverse of a diagonal matrix is calculated by taking the reciprocal of every diagonal element.

For example,

\[
D^{-1}=
\begin{pmatrix}
\frac{1}{d_1} & 0 & 0\\
0 & \frac{1}{d_2} & 0\\
0 & 0 & \frac{1}{d_3}
\end{pmatrix}
\]

If any diagonal element is zero, the matrix is singular.

## 3. Detailed Step-by-Step Solution

For matrix \(D\):

\[
D=
\begin{pmatrix}
2 & 0 & 0\\
0 & -3 & 0\\
0 & 0 & 5
\end{pmatrix}
\]

Take the reciprocal of each diagonal element:

\[
2\rightarrow\frac12
\]

\[
-3\rightarrow-\frac13
\]

\[
5\rightarrow\frac15
\]

Therefore,

\[
\boxed{
D^{-1}=
\begin{pmatrix}
\frac12 & 0 & 0\\
0 & -\frac13 & 0\\
0 & 0 & \frac15
\end{pmatrix}
}
\]

Now consider matrix \(E\):

\[
E=
\begin{pmatrix}
2 & 0 & 0\\
0 & 0 & 0\\
0 & 0 & 5
\end{pmatrix}
\]

Its determinant is

\[
\det(E)=2(0)(5)=0
\]

Since the determinant is zero, \(E\) is singular.

Therefore,

\[
\boxed{E^{-1}\text{ does not exist}}
\]

## 4. Verification and Consistency Checks

Verify the inverse of \(D\):

\[
DD^{-1}=
\begin{pmatrix}
2 & 0 & 0\\
0 & -3 & 0\\
0 & 0 & 5
\end{pmatrix}
\begin{pmatrix}
\frac12 & 0 & 0\\
0 & -\frac13 & 0\\
0 & 0 & \frac15
\end{pmatrix}
\]

\[
DD^{-1}=
\begin{pmatrix}
1 & 0 & 0\\
0 & 1 & 0\\
0 & 0 & 1
\end{pmatrix}
=I
\]

The inverse of \(D\) is correct.

Matrix \(E\) has a zero diagonal element and determinant zero, so it cannot have an inverse.
