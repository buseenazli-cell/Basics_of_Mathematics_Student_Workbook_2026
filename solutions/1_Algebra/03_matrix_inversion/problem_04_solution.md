# Exercise 4 — Finding an Inverse Using Gauss-Jordan Elimination

## 1. Problem Statement

Given the matrix

\[
A = \begin{pmatrix} 1 & 2 \\ 3 & 5 \end{pmatrix}
\]

Find its inverse using Gauss-Jordan elimination.

## 2. Theoretical Background and Concepts

Gauss-Jordan elimination is a method used to calculate the inverse of a square matrix.

First, create an augmented matrix:

\[
[A \mid I]
\]

Then perform elementary row operations until the left side becomes the identity matrix.

The right side will become the inverse:

\[
[A \mid I] \longrightarrow [I \mid A^{-1}]
\]

## 3. Detailed Step-by-Step Solution

Start with the augmented matrix:

\[
\left[
\begin{array}{cc|cc}
1 & 2 & 1 & 0 \\
3 & 5 & 0 & 1
\end{array}
\right]
\]

**Step 1:** Eliminate the 3 below the first pivot.

\[
R_2 \rightarrow R_2-3R_1
\]

\[
\left[
\begin{array}{cc|cc}
1 & 2 & 1 & 0 \\
0 & -1 & -3 & 1
\end{array}
\right]
\]

**Step 2:** Make the second pivot equal to 1.

\[
R_2 \rightarrow -R_2
\]

\[
\left[
\begin{array}{cc|cc}
1 & 2 & 1 & 0 \\
0 & 1 & 3 & -1
\end{array}
\right]
\]

**Step 3:** Eliminate the 2 above the second pivot.

\[
R_1 \rightarrow R_1-2R_2
\]

\[
\left[
\begin{array}{cc|cc}
1 & 0 & -5 & 2 \\
0 & 1 & 3 & -1
\end{array}
\right]
\]

The left side is now the identity matrix.

Therefore, the right side is the inverse.

\[
\boxed{
A^{-1} =
\begin{pmatrix}
-5 & 2 \\
3 & -1
\end{pmatrix}
}
\]

## 4. Verification and Consistency Checks

Multiply the original matrix by the calculated inverse:

\[
AA^{-1} =
\begin{pmatrix} 1 & 2 \\ 3 & 5 \end{pmatrix}
\begin{pmatrix} -5 & 2 \\ 3 & -1 \end{pmatrix}
\]

\[
=
\begin{pmatrix}
-5+6 & 2-2 \\
-15+15 & 6-5
\end{pmatrix}
\]

\[
AA^{-1} =
\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}
=I
\]

The result confirms that the calculated inverse is correct.
