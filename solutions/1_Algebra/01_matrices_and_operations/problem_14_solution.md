# Exercise 14. Rotation Matrices

## Question

The matrix for a rotation through an angle $\theta$ is

$$R(\theta)=\begin{pmatrix}\cos\theta&-\sin\theta\\\sin\theta&\cos\theta\end{pmatrix}.$$

Compute $R(\alpha)R(\beta)$ and, using the angle-sum formulas for sine and cosine, show that

$$R(\alpha)R(\beta)=R(\alpha+\beta).$$

Explain the result geometrically.

## Solution

**Method.** We multiply the two matrices using row-column sums, and then recognize the entries as the angle-sum formulas

$$\cos(\alpha+\beta)=\cos\alpha\cos\beta-\sin\alpha\sin\beta,\qquad \sin(\alpha+\beta)=\sin\alpha\cos\beta+\cos\alpha\sin\beta.$$

**The entries of the product.**

$$R(\alpha)R(\beta)=\begin{pmatrix}\cos\alpha&-\sin\alpha\\\sin\alpha&\cos\alpha\end{pmatrix}\begin{pmatrix}\cos\beta&-\sin\beta\\\sin\beta&\cos\beta\end{pmatrix}$$

$$=\begin{pmatrix}
\cos\alpha\cos\beta+(-\sin\alpha)\sin\beta & \cos\alpha(-\sin\beta)+(-\sin\alpha)\cos\beta\\[2pt]
\sin\alpha\cos\beta+\cos\alpha\sin\beta & \sin\alpha(-\sin\beta)+\cos\alpha\cos\beta
\end{pmatrix}.$$

Simplifying and regrouping each entry:

$$=\begin{pmatrix}
\cos\alpha\cos\beta-\sin\alpha\sin\beta & -(\sin\alpha\cos\beta+\cos\alpha\sin\beta)\\[2pt]
\sin\alpha\cos\beta+\cos\alpha\sin\beta & \cos\alpha\cos\beta-\sin\alpha\sin\beta
\end{pmatrix}.$$

**Applying the angle-sum identities.** The entries $(1,1)$ and $(2,2)$ equal $\cos(\alpha+\beta)$, the entry $(2,1)$ equals $\sin(\alpha+\beta)$, and the entry $(1,2)$ equals $-\sin(\alpha+\beta)$. Therefore

$$R(\alpha)R(\beta)=\begin{pmatrix}\cos(\alpha+\beta)&-\sin(\alpha+\beta)\\\sin(\alpha+\beta)&\cos(\alpha+\beta)\end{pmatrix}=R(\alpha+\beta).$$

**Geometric explanation.** For a vector $x$, the product $R(\alpha)R(\beta)x=R(\alpha)\bigl(R(\beta)x\bigr)$ means: first rotate $x$ by the angle $\beta$, and then rotate the result by the angle $\alpha$. The rightmost matrix acts first. The total effect of turning by $\beta$ and then by $\alpha$ is a single rotation by the angle $\alpha+\beta$, which is what the identity says. So matrix multiplication of rotations corresponds to adding angles. Since $\alpha+\beta=\beta+\alpha$, we also get $R(\beta)R(\alpha)=R(\alpha+\beta)$, so plane rotations commute with each other.
