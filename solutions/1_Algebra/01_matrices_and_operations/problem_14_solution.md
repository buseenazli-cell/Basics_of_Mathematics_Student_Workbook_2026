# Exercise 14

## Problem Statement

The matrix for a rotation through an angle $\theta$ is 

$$R(\theta) = \begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix}.$$

Compute $R(\alpha)R(\beta)$ and, using the angle-sum formulas for sine and cosine, show that $R(\alpha)R(\beta) = R(\alpha+\beta)$. Explain the result geometrically.

---

## Solution

To compute the product $R(\alpha)R(\beta)$, we multiply the two matrices row-by-column:

$$R(\alpha)R(\beta) = \begin{pmatrix} \cos\alpha & -\sin\alpha \\ \sin\alpha & \cos\alpha \end{pmatrix} \begin{pmatrix} \cos\beta & -\sin\beta \\ \sin\beta & \cos\beta \end{pmatrix}$$

We calculate each entry of the resulting $2 \times 2$ matrix individually:

- **Entry $(1,1)$ (Row 1 $\times$ Column 1):**
  $$(R(\alpha)R(\beta))_{11} = \cos\alpha\cos\beta + (-\sin\alpha)\sin\beta = \cos\alpha\cos\beta - \sin\alpha\sin\beta$$

- **Entry $(1,2)$ (Row 1 $\times$ Column 2):**
  $$(R(\alpha)R(\beta))_{12} = \cos\alpha(-\sin\beta) + (-\sin\alpha)\cos\beta = -(\sin\alpha\cos\beta + \cos\alpha\sin\beta)$$

- **Entry $(2,1)$ (Row 2 $\times$ Column 1):**
  $$(R(\alpha)R(\beta))_{21} = \sin\alpha\cos\beta + \cos\alpha\sin\beta$$

- **Entry $(2,2)$ (Row 2 $\times$ Column 2):**
  $$(R(\alpha)R(\beta))_{22} = \sin\alpha(-\sin\beta) + \cos\alpha\cos\beta = \cos\alpha\cos\beta - \sin\alpha\sin\beta$$

Combining these entries into matrix form gives:

$$R(\alpha)R(\beta) = \begin{pmatrix} \cos\alpha\cos\beta - \sin\alpha\sin\beta & -(\sin\alpha\cos\beta + \cos\alpha\sin\beta) \\ \sin\alpha\cos\beta + \cos\alpha\sin\beta & \cos\alpha\cos\beta - \sin\alpha\sin\beta \end{pmatrix}$$

We now apply the trigonometric angle-sum identities:
- $\cos(\alpha + \beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta$
- $\sin(\alpha + \beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta$

Substituting these formulas into the matrix entries yields:

$$R(\alpha)R(\beta) = \begin{pmatrix} \cos(\alpha+\beta) & -\sin(\alpha+\beta) \\ \sin(\alpha+\beta) & \cos(\alpha+\beta) \end{pmatrix} = R(\alpha+\beta)$$

### Geometric Explanation

Geometrically, applying the matrix $R(\beta)$ to a vector rotates it counterclockwise about the origin by an angle $\beta$. Multiplying the result by $R(\alpha)$ then rotates the vector by a further angle $\alpha$ counterclockwise. 

Thus, the product $R(\alpha)R(\beta)$ represents performing a rotation by $\beta$ followed by a rotation by $\alpha$. Since successive rotations in a two-dimensional plane add together, the combined effect is a single rotation through the total angle $\alpha + \beta$, which is precisely represented by the rotation matrix $R(\alpha + \beta)$.
