# Exercise 5. Matrix Times Vector

## Question

Let

$$A=\begin{pmatrix}2&-1\\1&3\end{pmatrix},\qquad x=\begin{pmatrix}4\\2\end{pmatrix}.$$

Compute $Ax$. Then express $Ax$ as a linear combination of the columns of $A$, with coefficients coming from the vector $x$.

## Solution

**Method 1: row by row.** Each component of $Ax$ is obtained by multiplying the corresponding entries of one row of $A$ and the vector $x$, and adding the products.

$$Ax=\begin{pmatrix}2&-1\\1&3\end{pmatrix}\begin{pmatrix}4\\2\end{pmatrix}
=\begin{pmatrix}2\cdot4+(-1)\cdot2\\ 1\cdot4+3\cdot2\end{pmatrix}
=\begin{pmatrix}8-2\\4+6\end{pmatrix}
=\begin{pmatrix}6\\10\end{pmatrix}.$$

**Method 2: column by column.** Now we regroup the same terms, collecting those that contain $4$ and those that contain $2$:

$$Ax=\begin{pmatrix}2\cdot4+(-1)\cdot2\\ 1\cdot4+3\cdot2\end{pmatrix}
=\begin{pmatrix}2\cdot4\\1\cdot4\end{pmatrix}+\begin{pmatrix}(-1)\cdot2\\3\cdot2\end{pmatrix}
=4\begin{pmatrix}2\\1\end{pmatrix}+2\begin{pmatrix}-1\\3\end{pmatrix}.$$

The number $4$ multiplies the first column of $A$ and the number $2$ multiplies the second column, because $4$ and $2$ are the corresponding entries of $x=(4,2)^T$. So $Ax$ is $4$ times the first column plus $2$ times the second column.

**Verification.**

$$4\begin{pmatrix}2\\1\end{pmatrix}+2\begin{pmatrix}-1\\3\end{pmatrix}
=\begin{pmatrix}8\\4\end{pmatrix}+\begin{pmatrix}-2\\6\end{pmatrix}
=\begin{pmatrix}6\\10\end{pmatrix},$$

which agrees with the row-by-row result. In general, $Ax=x_1\,a_1+x_2\,a_2$, where $a_1,a_2$ are the columns of $A$.
