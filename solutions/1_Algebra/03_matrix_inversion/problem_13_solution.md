# Exercise 13 — Order of Matrix Multiplication

## 1. Problem Statement

Given the scaling matrix

\[
S=
\begin{pmatrix}
2 & 0\\
0 & 1
\end{pmatrix}
\]

and the shear matrix

\[
H=
\begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix}
\]

Define

\[
T=HS
\]

Find \(T^{-1}\) and verify the correct order of multiplication.

## 2. Theoretical Background and Concepts

The inverse of a product of two invertible matrices is

\[
(AB)^{-1}=B^{-1}A^{-1}
\]

The order is reversed when calculating the inverse.

Matrix multiplication is generally not commutative:

\[
AB\neq BA
\]

Therefore, the order of the inverse matrices is important.

## 3. Detailed Step-by-Step Solution

First, calculate \(T=HS\):

\[
T=
\begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix}
\begin{pmatrix}
2 & 0\\
0 & 1
\end{pmatrix}
\]

\[
T=
\begin{pmatrix}
2 & 1\\
0 & 1
\end{pmatrix}
\]

Now calculate the inverses separately.

For matrix \(S\):

\[
S^{-1}=
\begin{pmatrix}
\frac12 & 0\\
0 & 1
\end{pmatrix}
\]

For matrix \(H\):

\[
H^{-1}=
\begin{pmatrix}
1 & -1\\
0 & 1
\end{pmatrix}
\]

Since \(T=HS\), the inverse is

\[
T^{-1}=(HS)^{-1}=S^{-1}H^{-1}
\]

Substitute the matrices:

\[
T^{-1}
=
\begin{pmatrix}
\frac12 & 0\\
0 & 1
\end{pmatrix}
\begin{pmatrix}
1 & -1\\
0 & 1
\end{pmatrix}
\]

\[
\boxed{
T^{-1}=
\begin{pmatrix}
\frac12 & -\frac12\\
0 & 1
\end{pmatrix}
}
\]

Now consider the incorrect order:

\[
H^{-1}S^{-1}
=
\begin{pmatrix}
1 & -1\\
0 & 1
\end{pmatrix}
\begin{pmatrix}
\frac12 & 0\\
0 & 1
\end{pmatrix}
\]

\[
=
\begin{pmatrix}
\frac12 & -1\\
0 & 1
\end{pmatrix}
\]

This is different from the correct inverse.

## 4. Verification and Consistency Checks

Verify the correct inverse:

\[
TT^{-1}
=
\begin{pmatrix}
2 & 1\\
0 & 1
\end{pmatrix}
\begin{pmatrix}
\frac12 & -\frac12\\
0 & 1
\end{pmatrix}
\]

\[
=
\begin{pmatrix}
1 & -1+1\\
0 & 1
\end{pmatrix}
\]

\[
TT^{-1}
=
\begin{pmatrix}
1 & 0\\
0 & 1
\end{pmatrix}
=I
\]

The correct order gives the identity matrix.

Therefore,

\[
\boxed{T^{-1}=S^{-1}H^{-1}}
\]

The order of multiplication must be reversed.
