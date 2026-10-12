## Solution

### Computing $RSx$ (scale first, then rotate)

$$
Sx=\begin{pmatrix}2&0\\0&1\end{pmatrix}\begin{pmatrix}1\\2\end{pmatrix}=\begin{pmatrix}2\\2\end{pmatrix}
$$

$$
R(Sx)=\begin{pmatrix}0&-1\\1&0\end{pmatrix}\begin{pmatrix}2\\2\end{pmatrix}=\begin{pmatrix}-2\\2\end{pmatrix}
$$

### Computing $SRx$ (rotate first, then scale)

$$
Rx=\begin{pmatrix}0&-1\\1&0\end{pmatrix}\begin{pmatrix}1\\2\end{pmatrix}=\begin{pmatrix}-2\\1\end{pmatrix}
$$

$$
S(Rx)=\begin{pmatrix}2&0\\0&1\end{pmatrix}\begin{pmatrix}-2\\1\end{pmatrix}=\begin{pmatrix}-4\\1\end{pmatrix}
$$

### Check with the product matrices

$$
RS=\begin{pmatrix}0&-1\\2&0\end{pmatrix},\qquad
SR=\begin{pmatrix}0&-2\\1&0\end{pmatrix}
$$

$$
RSx=\begin{pmatrix}-2\\2\end{pmatrix},\qquad
SRx=\begin{pmatrix}-4\\1\end{pmatrix}
$$

## Comparison

$$
RSx=\begin{pmatrix}-2\\2\end{pmatrix}\neq\begin{pmatrix}-4\\1\end{pmatrix}=SRx
$$

Since $RS\neq SR$, the matrices do not commute. The lengths also differ: $\|RSx\|=\sqrt{8}$ and $\|SRx\|=\sqrt{17}$.

| Order | Meaning | Result | Length |
|:---:|:---:|:---:|:---:|
| $RSx$ | scale, then rotate | $(-2,\,2)$ | $\sqrt{8}$ |
| $SRx$ | rotate, then scale | $(-4,\,1)$ | $\sqrt{17}$ |

## Geometric explanation

$S$ stretches only along the $x$-axis (by a factor of 2) and leaves the $y$-direction unchanged, so it treats the coordinate axes differently. $R$ turns every vector by $90^\circ$, so the $x$-axis becomes the $y$-axis.

- **$RSx$:** The plane is stretched horizontally first, then rotated. The stretched direction ends up **vertical**, so the unit circle becomes an ellipse with its long axis along the $y$-axis.
- **$SRx$:** The plane is rotated first, then stretched horizontally. The stretch acts on the already rotated vector, so the unit circle becomes an ellipse with its long axis along the $x$-axis.

Rotation and nonuniform scaling commute only when the scaling is uniform ($S=cI$), because then no direction is treated differently from another.
