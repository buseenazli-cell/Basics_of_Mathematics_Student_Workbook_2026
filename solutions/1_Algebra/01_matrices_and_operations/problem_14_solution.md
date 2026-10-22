# Exercise 14

## Question

For an angle $\theta$, let

$$
R(\theta) = \begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix}
$$

Compute $R(\alpha)R(\beta)$ and use the angle-sum identities to show that $R(\alpha)R(\beta) = R(\alpha+\beta)$. Explain what this product means geometrically.

## Solution

### The product

Multiply row by column:

$$
R(\alpha)R(\beta) = \begin{pmatrix} \cos\alpha\cos\beta - \sin\alpha\sin\beta & -\cos\alpha\sin\beta - \sin\alpha\cos\beta \\ \sin\alpha\cos\beta + \cos\alpha\sin\beta & -\sin\alpha\sin\beta + \cos\alpha\cos\beta \end{pmatrix}
$$

### Angle-sum identities

$$
\cos(\alpha+\beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta
$$

$$
\sin(\alpha+\beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta
$$

The (1,1) and (2,2) entries equal $\cos(\alpha+\beta)$. The (2,1) entry equals $\sin(\alpha+\beta)$, and the (1,2) entry equals $-\sin(\alpha+\beta)$. Therefore

$$
R(\alpha)R(\beta) = \begin{pmatrix} \cos(\alpha+\beta) & -\sin(\alpha+\beta) \\ \sin(\alpha+\beta) & \cos(\alpha+\beta) \end{pmatrix} = R(\alpha+\beta)
$$

### Geometric meaning

In the product $R(\alpha)R(\beta)$, applied to a vector $x$ as $R(\alpha)\bigl(R(\beta)x\bigr)$, the right factor acts first. So the product is the rotation by $\beta$ followed by the rotation by $\alpha$. The result is one rotation by the total angle $\alpha+\beta$.
