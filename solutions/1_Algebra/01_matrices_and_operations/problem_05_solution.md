# Exercise 5. Matrix Times Vector

## Question

Let

$$
A = \begin{pmatrix} 2 & -1 \\ 1 & 3 \end{pmatrix}, \qquad x = \begin{pmatrix} 4 \\ 2 \end{pmatrix}
$$

Compute $Ax$. Then express $Ax$ as a linear combination of the columns of $A$, with coefficients coming from the vector $x$.

## Solution

### Row form

Each component of $Ax$ is obtained by taking one row of $A$, multiplying its entries by the corresponding entries of $x$, and adding the results.

$$
Ax = \begin{pmatrix} 2 & -1 \\ 1 & 3 \end{pmatrix}\begin{pmatrix} 4 \\ 2 \end{pmatrix}
= \begin{pmatrix} 2\cdot 4 + (-1)\cdot 2 \\ 1\cdot 4 + 3\cdot 2 \end{pmatrix}
= \begin{pmatrix} 8 - 2 \\ 4 + 6 \end{pmatrix}
= \begin{pmatrix} 6 \\ 10 \end{pmatrix}
$$

### Column form

Now regroup the same terms by columns instead of rows. The first column of $A$ is multiplied only by the first entry of $x$, which is $4$, and the second column of $A$ is multiplied only by the second entry of $x$, which is $2$:

$$
\begin{pmatrix} 2\cdot 4 + (-1)\cdot 2 \\ 1\cdot 4 + 3\cdot 2 \end{pmatrix}
= \begin{pmatrix} 2\cdot 4 \\ 1\cdot 4 \end{pmatrix} + \begin{pmatrix} (-1)\cdot 2 \\ 3\cdot 2 \end{pmatrix}
= 4\begin{pmatrix} 2 \\ 1 \end{pmatrix} + 2\begin{pmatrix} -1 \\ 3 \end{pmatrix}
$$

So $Ax$ is $4$ times the first column of $A$ plus $2$ times the second column of $A$, because $4$ and $2$ are the corresponding entries of $x$.

Check:

$$
4\begin{pmatrix} 2 \\ 1 \end{pmatrix} + 2\begin{pmatrix} -1 \\ 3 \end{pmatrix}
= \begin{pmatrix} 8 \\ 4 \end{pmatrix} + \begin{pmatrix} -2 \\ 6 \end{pmatrix}
= \begin{pmatrix} 6 \\ 10 \end{pmatrix}
$$

This agrees with the row form.

### Conclusion

$$
Ax = \begin{pmatrix} 6 \\ 10 \end{pmatrix} = 4\begin{pmatrix} 2 \\ 1 \end{pmatrix} + 2\begin{pmatrix} -1 \\ 3 \end{pmatrix}
$$

In general, $Ax$ is always a linear combination of the columns of $A$, with the entries of $x$ as the coefficients.
