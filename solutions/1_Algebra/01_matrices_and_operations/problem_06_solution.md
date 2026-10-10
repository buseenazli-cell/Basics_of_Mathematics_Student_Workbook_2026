## Solution

### 1. Transposes

```math
A^T=\begin{pmatrix}1&4\\2&5\\3&6\end{pmatrix},\qquad
B^T=\begin{pmatrix}1&2&-1\\0&1&3\end{pmatrix}
```

### 2. Product $AB$

```math
AB=\begin{pmatrix}1&2&3\\4&5&6\end{pmatrix}\begin{pmatrix}1&0\\2&1\\-1&3\end{pmatrix}
```

```math
AB=\begin{pmatrix}1\cdot 1+2\cdot 2+3\cdot(-1) & 1\cdot 0+2\cdot 1+3\cdot 3\\ 4\cdot 1+5\cdot 2+6\cdot(-1) & 4\cdot 0+5\cdot 1+6\cdot 3\end{pmatrix}
=\begin{pmatrix}2&11\\8&23\end{pmatrix}
```

### 3. Verification of $(AB)^T = B^T A^T$

**Left-hand side:**

```math
(AB)^T=\begin{pmatrix}2&8\\11&23\end{pmatrix}
```

**Right-hand side:**

```math
B^TA^T=\begin{pmatrix}1&2&-1\\0&1&3\end{pmatrix}\begin{pmatrix}1&4\\2&5\\3&6\end{pmatrix}
```

```math
B^TA^T=\begin{pmatrix}1\cdot 1+2\cdot 2+(-1)\cdot 3 & 1\cdot 4+2\cdot 5+(-1)\cdot 6\\ 0\cdot 1+1\cdot 2+3\cdot 3 & 0\cdot 4+1\cdot 5+3\cdot 6\end{pmatrix}
=\begin{pmatrix}2&8\\11&23\end{pmatrix}
```

**Conclusion:** Both sides are equal, so

```math
(AB)^T = B^TA^T = \begin{pmatrix}2&8\\11&23\end{pmatrix}
```
