# Exercise 14 — A Matrix That Is Its Own Inverse

## 1. Problem Statement

Suppose that a square matrix \(A\) satisfies

\[
A^2=I
\]

Prove that

\[
A^{-1}=A
\]

Give an example of such a matrix that is not equal to \(I\) or \(-I\).

## 2. Theoretical Background and Concepts

A matrix is its own inverse if multiplying it by itself gives the identity matrix.

By definition,

\[
AA^{-1}=I
\]

If

\[
A^2=I
\]

then

\[
AA=I
\]

Therefore, \(A\) satisfies the definition of its own inverse.

Such a matrix is called an involutory matrix.

## 3. Detailed Step-by-Step Solution

We are given:

\[
A^2=I
\]

By the definition of matrix powers:

\[
A^2=AA
\]

Therefore,

\[
AA=I
\]

The inverse of a matrix is the matrix that produces the identity when multiplied by the original matrix.

Since \(A\cdot A=I\), it follows that

\[
\boxed{A^{-1}=A}
\]

Now consider the example:

\[
A=
\begin{pmatrix}
1 & 0\\
0 & -1
\end{pmatrix}
\]

Calculate its square:

\[
A^2=
\begin{pmatrix}
1 & 0\\
0 & -1
\end{pmatrix}
\begin{pmatrix}
1 & 0\\
0 & -1
\end{pmatrix}
\]

\[
A^2=
\begin{pmatrix}
1 & 0\\
0 & 1
\end{pmatrix}
=I
\]

This matrix satisfies the given condition.

Also,

\[
A\neq I
\]

and

\[
A\neq -I
\]

## 4. Verification and Consistency Checks

The example satisfies

\[
A^2=I
\]

Therefore,

\[
AA=I
\]

and its inverse is itself:

\[
\boxed{
A^{-1}=
\begin{pmatrix}
1 & 0\\
0 & -1
\end{pmatrix}
}
\]

The proof and the example confirm the result.
