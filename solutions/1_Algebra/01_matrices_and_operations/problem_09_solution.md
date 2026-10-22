# Exercise 9. Order of Transformations: Scaling and Rotation

## Question

Let

$$
S = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix}, \qquad R = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}
$$

The matrix $S$ describes nonuniform scaling, while $R$ describes a $90^\circ$ counterclockwise rotation. For

$$
x = \begin{pmatrix} 1 \\ 2 \end{pmatrix}
$$

compute $RSx$ and $SRx$. Compare the results and explain geometrically why the order of these transformations matters.

## Solution

### Method

A product such as $RSx$ is evaluated from the right: first $Sx$, then $R$ is applied to that result. Each entry of a matrix-vector product is a row of the matrix paired with the vector: multiply corresponding entries and add.

### Computing RSx (scale first, then rotate)

First apply $S$ to $x$:

$$
Sx = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 1 \\ 2 \end{pmatrix}
= \begin{pmatrix} 2\cdot 1 + 0\cdot 2 \\ 0\cdot 1 + 1\cdot 2 \end{pmatrix}
= \begin{pmatrix} 2 \\ 2 \end{pmatrix}
$$

Then apply $R$ to $Sx$:

$$
R(Sx) = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}\begin{pmatrix} 2 \\ 2 \end{pmatrix}
= \begin{pmatrix} 0\cdot 2 + (-1)\cdot 2 \\ 1\cdot 2 + 0\cdot 2 \end{pmatrix}
= \begin{pmatrix} -2 \\ 2 \end{pmatrix}
$$

### Computing SRx (rotate first, then scale)

First apply $R$ to $x$:

$$
Rx = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}\begin{pmatrix} 1 \\ 2 \end{pmatrix}
= \begin{pmatrix} 0\cdot 1 + (-1)\cdot 2 \\ 1\cdot 1 + 0\cdot 2 \end{pmatrix}
= \begin{pmatrix} -2 \\ 1 \end{pmatrix}
$$

Then apply $S$ to $Rx$:

$$
S(Rx) = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} -2 \\ 1 \end{pmatrix}
= \begin{pmatrix} 2\cdot(-2) + 0\cdot 1 \\ 0\cdot(-2) + 1\cdot 1 \end{pmatrix}
= \begin{pmatrix} -4 \\ 1 \end{pmatrix}
$$

### Comparison

$$
RSx = \begin{pmatrix} -2 \\ 2 \end{pmatrix} \neq \begin{pmatrix} -4 \\ 1 \end{pmatrix} = SRx
$$

The two results are different vectors. They also have different lengths:

$$
\|RSx\| = \sqrt{(-2)^2 + 2^2} = \sqrt{8}, \qquad \|SRx\| = \sqrt{(-4)^2 + 1^2} = \sqrt{17}
$$

The original vector has length $\sqrt{5}$.

### Geometric explanation

The matrix $S$ stretches only the horizontal direction (by a factor $2$) and leaves the vertical direction alone. The matrix $R$ turns every vector by $90^\circ$ but does not change lengths. The order matters because rotation changes which direction of the vector is the one being stretched.

- **Scale first, then rotate ($RSx$).** The vector $x = (1, 2)$ has horizontal part $1$. Scaling doubles it, giving $(2, 2)$. Rotation then turns this vector without changing its length, so $\|RSx\| = \sqrt{8}$.
- **Rotate first, then scale ($SRx$).** The rotation sends $(1, 2)$ to $(-2, 1)$. The old vertical part $2$ now lies along the horizontal direction, which is exactly the direction that $S$ stretches. The larger part of the vector is doubled, giving $(-4, 1)$ and the longer length $\sqrt{17}$.

So in one order the stretch acts on the small horizontal part $1$, and in the other order it acts on the larger part $2$. In general the two products of matrices are

$$
RS = \begin{pmatrix} 0 & -1 \\ 2 & 0 \end{pmatrix}, \qquad SR = \begin{pmatrix} 0 & -2 \\ 1 & 0 \end{pmatrix}
$$

which are different matrices.

### Remark on when the order does not matter

For a diagonal scaling $D = \operatorname{diag}(s, t)$ and the given $90^\circ$ rotation $R$,

$$
RD = \begin{pmatrix} 0 & -t \\ s & 0 \end{pmatrix}, \qquad DR = \begin{pmatrix} 0 & -s \\ t & 0 \end{pmatrix}
$$

so $RD = DR$ exactly when $s = t$. Hence, for this $90^\circ$ rotation, a diagonal scaling commutes with it only when its two scale factors agree, that is, when the scaling is uniform.

This restriction is specific to this rotation. It is not true for every rotation: a $180^\circ$ rotation equals $-I$, which commutes with every matrix, including nonuniform scalings.

### Conclusion

$$
RSx = \begin{pmatrix} -2 \\ 2 \end{pmatrix}, \qquad SRx = \begin{pmatrix} -4 \\ 1 \end{pmatrix}
$$

The results differ, so the order of the scaling and the rotation matters.
