# Exercise 9. Composing Transformations

## Question

Let

$$S=\begin{pmatrix}2&0\\0&1\end{pmatrix},\qquad R=\begin{pmatrix}0&-1\\1&0\end{pmatrix}.$$

The matrix $S$ describes nonuniform scaling, while $R$ describes a $90^\circ$ counterclockwise rotation. For

$$x=\begin{pmatrix}1\\2\end{pmatrix}$$

compute $RSx$ and $SRx$. Compare the results and explain geometrically why the order of these transformations matters.

## Solution

**Method.** $RSx$ means $R(Sx)$: first apply $S$, then $R$. Similarly $SRx=S(Rx)$: first rotate, then scale. Each matrix-vector product is computed by row-column sums.

**Computing $RSx$.**

Stage 1 (apply $S$):

$$Sx=\begin{pmatrix}2&0\\0&1\end{pmatrix}\begin{pmatrix}1\\2\end{pmatrix}=\begin{pmatrix}2\cdot1+0\cdot2\\0\cdot1+1\cdot2\end{pmatrix}=\begin{pmatrix}2\\2\end{pmatrix}.$$

Stage 2 (apply $R$ to the result):

$$R(Sx)=\begin{pmatrix}0&-1\\1&0\end{pmatrix}\begin{pmatrix}2\\2\end{pmatrix}=\begin{pmatrix}0\cdot2+(-1)\cdot2\\1\cdot2+0\cdot2\end{pmatrix}=\begin{pmatrix}-2\\2\end{pmatrix}.$$

**Computing $SRx$.**

Stage 1 (apply $R$):

$$Rx=\begin{pmatrix}0&-1\\1&0\end{pmatrix}\begin{pmatrix}1\\2\end{pmatrix}=\begin{pmatrix}0\cdot1+(-1)\cdot2\\1\cdot1+0\cdot2\end{pmatrix}=\begin{pmatrix}-2\\1\end{pmatrix}.$$

Stage 2 (apply $S$ to the result):

$$S(Rx)=\begin{pmatrix}2&0\\0&1\end{pmatrix}\begin{pmatrix}-2\\1\end{pmatrix}=\begin{pmatrix}2\cdot(-2)+0\cdot1\\0\cdot(-2)+1\cdot1\end{pmatrix}=\begin{pmatrix}-4\\1\end{pmatrix}.$$

**Comparison.**

$$RSx=\begin{pmatrix}-2\\2\end{pmatrix}\neq\begin{pmatrix}-4\\1\end{pmatrix}=SRx.$$

**Geometric explanation.** $S$ stretches only the horizontal direction (by a factor of $2$) and leaves the vertical direction unchanged.

- In $RSx$, the vector is stretched horizontally first, and *then* rotated. The stretched direction (the $x$-axis) is turned into the $y$-axis, so after the rotation the stretching shows up vertically.
- In $SRx$, the vector is rotated first, so the part of the vector that was vertical now points horizontally. Only then is the horizontal direction stretched, so the stretch acts on a different part of the vector.

Rotation changes which direction is stretched, so the two orders give different results.

**Restriction of the conclusion.** For the given $90^\circ$ rotation $R$ and a diagonal scaling $D=\begin{pmatrix}s&0\\0&t\end{pmatrix}$ we have

$$RD=\begin{pmatrix}0&-t\\s&0\end{pmatrix},\qquad DR=\begin{pmatrix}0&-s\\t&0\end{pmatrix},$$

so $RD=DR$ only when $s=t$, that is, when the scaling is uniform. This is a statement about the $90^\circ$ rotation only; it is not true for every rotation. For example, the $180^\circ$ rotation is $-I$, which commutes with every matrix, including nonuniform scalings.
