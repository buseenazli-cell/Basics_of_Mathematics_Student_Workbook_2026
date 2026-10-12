## Solution

In a product of matrices, the rightmost matrix acts first. So $`RSx`$ means "scale, then rotate", and $`SRx`$ means "rotate, then scale".

### Computing $`RSx`$ (scale first, then rotate)

```math
Sx=\begin{pmatrix}2&0\\0&1\end{pmatrix}\begin{pmatrix}1\\2\end{pmatrix}=\begin{pmatrix}2\\2\end{pmatrix}
```

```math
R(Sx)=\begin{pmatrix}0&-1\\1&0\end{pmatrix}\begin{pmatrix}2\\2\end{pmatrix}=\begin{pmatrix}-2\\2\end{pmatrix}
```

### Computing $`SRx`$ (rotate first, then scale)

```math
Rx=\begin{pmatrix}0&-1\\1&0\end{pmatrix}\begin{pmatrix}1\\2\end{pmatrix}=\begin{pmatrix}-2\\1\end{pmatrix}
```

```math
S(Rx)=\begin{pmatrix}2&0\\0&1\end{pmatrix}\begin{pmatrix}-2\\1\end{pmatrix}=\begin{pmatrix}-4\\1\end{pmatrix}
```

### Check with the product matrices

```math
RS=\begin{pmatrix}0&-1\\2&0\end{pmatrix},\qquad
SR=\begin{pmatrix}0&-2\\1&0\end{pmatrix}
```

```math
RSx=\begin{pmatrix}-2\\2\end{pmatrix},\qquad
SRx=\begin{pmatrix}-4\\1\end{pmatrix}
```

## Comparison

| Order | Meaning | Result | Length |
|:---:|:---:|:---:|:---:|
| $`RSx`$ | scale, then rotate | $`(-2,\ 2)`$ | $`\sqrt{8}`$ |
| $`SRx`$ | rotate, then scale | $`(-4,\ 1)`$ | $`\sqrt{17}`$ |

```math
RSx=\begin{pmatrix}-2\\2\end{pmatrix}\neq\begin{pmatrix}-4\\1\end{pmatrix}=SRx
```

The two results differ in both direction and length, because $`RS\neq SR`$: the matrices do not commute.

## Geometric explanation

$`S`$ stretches only the $`x`$-direction (by a factor of 2) and leaves the $`y`$-direction unchanged, so it treats the two axes differently. $`R`$ turns every vector by $`90^\circ`$, so it sends the $`x`$-axis to the $`y`$-axis.

- **$`RSx`$:** The plane is first stretched horizontally, and then the stretched picture is rotated. The long direction ends up **vertical**. The unit circle becomes an ellipse whose long axis lies along the $`y`$-axis.
- **$`SRx`$:** The plane is first rotated, which leaves the unit circle a circle, and then stretched horizontally. The unit circle becomes an ellipse whose long axis lies along the $`x`$-axis.

| Vector | $`RS`$ | $`SR`$ |
|:---:|:---:|:---:|
| $`e_1=(1,0)`$ | $`(0,\ 2)`$ | $`(0,\ 1)`$ |
| $`e_2=(0,1)`$ | $`(-1,\ 0)`$ | $`(-2,\ 0)`$ |

In $`RS`$, the stretch hits the $`x`$-direction before the rotation moves it to the vertical. In $`SR`$, the rotation first moves $`e_2`$ onto the $`x`$-axis, where $`S`$ then doubles it.

Rotation and scaling commute only when the scaling is uniform ($`S=cI`$), because then no direction is treated differently from another.
