# Exercise 8 — Geometric Interpretation of an Inverse Matrix

## 1. Problem Statement

Consider the scaling matrix

\[
S=
\begin{pmatrix}
2 & 0\\
0 & \frac12
\end{pmatrix}
\]

Find its inverse and explain the geometric meaning of the inverse transformation.

## 2. Theoretical Background and Concepts

A matrix can represent a geometric transformation.

A scaling matrix changes the size of a vector along the coordinate axes.

The inverse matrix reverses the original transformation.

If

\[
y=Sx
\]

then the original vector can be recovered using

\[
x=S^{-1}y
\]

## 3. Detailed Step-by-Step Solution

The given matrix is

\[
S=
\begin{pmatrix}
2 & 0\\
0 & \frac12
\end{pmatrix}
\]

Because it is a diagonal matrix, its inverse is obtained by taking the reciprocal of each diagonal element.

Therefore,

\[
\boxed{
S^{-1}=
\begin{pmatrix}
\frac12 & 0\\
0 & 2
\end{pmatrix}
}
\]

The original transformation doubles the x-coordinate and halves the y-coordinate.

The inverse transformation halves the x-coordinate and doubles the y-coordinate.

For example, consider the vector

\[
v=
\begin{pmatrix}
2\\
4
\end{pmatrix}
\]

Apply the scaling transformation:

\[
Sv=
\begin{pmatrix}
2 & 0\\
0 & \frac12
\end{pmatrix}
\begin{pmatrix}
2\\
4
\end{pmatrix}
=
\begin{pmatrix}
4\\
2
\end{pmatrix}
\]

Now apply the inverse transformation:

\[
S^{-1}
\begin{pmatrix}
4\\
2
\end{pmatrix}
=
\begin{pmatrix}
\frac12 & 0\\
0 & 2
\end{pmatrix}
\begin{pmatrix}
4\\
2
\end{pmatrix}
=
\begin{pmatrix}
2\\
4
\end{pmatrix}
\]

## 4. Verification and Consistency Checks

Multiply the scaling matrix by its inverse:

\[
SS^{-1}=
\begin{pmatrix}
2 & 0\\
0 & \frac12
\end{pmatrix}
\begin{pmatrix}
\frac12 & 0\\
0 & 2
\end{pmatrix}
\]

\[
SS^{-1}=
\begin{pmatrix}
1 & 0\\
0 & 1
\end{pmatrix}
=I
\]

The inverse transformation successfully restores the original vector.

Therefore, the inverse matrix reverses the scaling transformation.
