\documentclass{article}
\usepackage{amsmath}
\begin{document}

\[
A=\begin{pmatrix}2&-1\\1&3\end{pmatrix},\qquad
x=\begin{pmatrix}4\\2\end{pmatrix}
\]

\textbf{Computing $Ax$:}
\[
Ax=\begin{pmatrix}2&-1\\1&3\end{pmatrix}\begin{pmatrix}4\\2\end{pmatrix}
=\begin{pmatrix}2\cdot 4+(-1)\cdot 2\\ 1\cdot 4+3\cdot 2\end{pmatrix}
=\begin{pmatrix}6\\10\end{pmatrix}
\]

\textbf{As a linear combination of the columns of $A$:}
\[
Ax = 4\begin{pmatrix}2\\1\end{pmatrix}+2\begin{pmatrix}-1\\3\end{pmatrix}
=\begin{pmatrix}8\\4\end{pmatrix}+\begin{pmatrix}-2\\6\end{pmatrix}
=\begin{pmatrix}6\\10\end{pmatrix}
\]

\end{document}
