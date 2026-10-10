## Matrix-Vector Product

Let

```math
A=\begin{pmatrix}2&-1\\1&3\end{pmatrix},\qquad
x=\begin{pmatrix}4\\2\end{pmatrix}
```

### Computing $Ax$

```math
Ax=\begin{pmatrix}2&-1\\1&3\end{pmatrix}\begin{pmatrix}4\\2\end{pmatrix}
=\begin{pmatrix}2\cdot 4+(-1)\cdot 2\\ 1\cdot 4+3\cdot 2\end{pmatrix}
=\begin{pmatrix}6\\10\end{pmatrix}
```

### As a linear combination of the columns of $A$

```math
Ax = 4\begin{pmatrix}2\\1\end{pmatrix}+2\begin{pmatrix}-1\\3\end{pmatrix}
=\begin{pmatrix}8\\4\end{pmatrix}+\begin{pmatrix}-2\\6\end{pmatrix}
=\begin{pmatrix}6\\10\end{pmatrix}
```

**Result:** $Ax = 4\,a_1 + 2\,a_2 = \begin{pmatrix}6\\10\end{pmatrix}$,
where $a_1=\begin{pmatrix}2\\1\end{pmatrix}$ and $a_2=\begin{pmatrix}-1\\3\end{pmatrix}$ are the columns of $A$.
