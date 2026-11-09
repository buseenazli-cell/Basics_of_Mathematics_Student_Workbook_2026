# Exercise 7 — Inverse of a Product of Matrices

## 1. Problem Statement

Given the matrices

\[
A=
\begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix},
\qquad
B=
\begin{pmatrix}
2 & 0\\
0 & 3
\end{pmatrix}
\]

Find the inverse of \(AB\).

Also verify the result using the inverse product property.

## 2. Theoretical Background and Concepts

For two invertible matrices \(A\) and \(B\), the inverse of their product is

\[
(AB)^{-1}=B^{-1}A^{-1}
\]

The order of the matrices is reversed.

In general,

\[
(AB)^{-1}\neq A^{-1}B^{-1}
\]

## 3. Detailed Step-by-Step Solution

First, calculate \(AB\):

\[
AB=
\begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix}
\begin{pmatrix}
2 & 0\\
0 & 3
\end{pmatrix}
\]

\[
AB=
\begin{pmatrix}
2 & 3\\
0 & 3
\end{pmatrix}
\]

Calculate its inverse:

\[
(AB)^{-1}
=
\frac{1}{2(3)-3(0)}
\begin{pmatrix}
3 & -3\\
0 & 2
\end{pmatrix}
\]

\[
\boxed{
(AB)^{-1}=
\begin{pmatrix}
\frac12 & -\frac12\\
0 & \frac13
\end{pmatrix}
}
\]

Now verify using the inverse product property.

First calculate \(A^{-1}\):

\[
A^{-1}=
\begin{pmatrix}
1 & -1\\
0 & 1
\end{pmatrix}
\]

Then calculate \(B^{-1}\):

\[
B^{-1}=
\begin{pmatrix}
\frac12 & 0\\
0 & \frac13
\end{pmatrix}
\]

Using the property:

\[
(AB)^{-1}=B^{-1}A^{-1}
\]

\[
=
\begin{pmatrix}
\frac12 & 0\\
0 & \frac13
\end{pmatrix}
\begin{pmatrix}
1 & -1\\
0 & 1
\end{pmatrix}
\]

\[
=
\begin{pmatrix}
\frac12 & -\frac12\\
0 & \frac13
\end{pmatrix}
\]

## 4. Verification and Consistency Checks

Both methods produce the same inverse:

\[
\boxed{
(AB)^{-1}=
\begin{pmatrix}
\frac12 & -\frac12\\
0 & \frac13
\end{pmatrix}
}
\]

The inverse product property is verified.
