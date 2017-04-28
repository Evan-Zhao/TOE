## Newtonian Mechanics

### Galilean invariance

Two axioms:

1. There exists an *absolute space*, in which Newton's laws are true. An inertial frame is a reference frame in relative uniform motion to absolute space.
2. All inertial frames share a *universal time*.

### Euclidean Space

#### Euclidean Space: $\mathbb{R}^n$

#### Euclidean Group

Euclidean Group for $\mathbb{R}^n$ is denoted as $E(n)$ or $ISO(n)$; its elements (isometries) are called the *Euclidean Motion*.

$E(n)$ has $n(n+1)/2$ degrees of freedom; of these, $n$ degrees are from translational motion, and the remaining from rotational motion.

A subgroup $E^+(n)$ is the motion preserving orientation, called *direct* isometry, or *rigid motions*, because these are motions that can occur on a rigid body; in fact, we know from classical mechanics that the *rigid body motion*, a curve in $E(n)$, will always stay in $E^+(n)$, because the determinant cannot jump from $+1$ to $-1$.

Similarly, $E^-(n)$ is the subgroup of motion called *indirect isometry*.  

The subgroup $E^+(n)$ is of index $2$, meaning that there is a one-on-one relationship between $E^+(n)$ and $E^-(n)$.

The set in $E(n)$ is isomorphic to $\text{Mat}(n\times n) \times \mathbb{R}^n$, hence a Euclidean motion is representable with a pair $(A,b)$.

### Galilean Transformation

A transformation needs to consider space and time; Galilean transformation consider time as independent from space, hence denote a spacetime event as

$$ \begin{pmatrix} x \\ t \end{pmatrix} \in \mathbb{R}^n \times \mathbb{R} \simeq \mathbb{R}^{n+1}$$ 

However, in order to write a transformation as a matrix conveniently, the spacetime event is usually written as $\begin{pmatrix} x \\ t \\1 \end{pmatrix}$ (appending a $1$ is the common practice to form an affine space), and a group action can be written as

$$\begin{pmatrix} R & \boldsymbol{v} & \boldsymbol{x_0} \\ 0 & 1 & t_0 \\ 0 & 0 & 1 \end{pmatrix} \begin{pmatrix} \boldsymbol{x} \\ t \\ 1 \end{pmatrix} = \begin{pmatrix} R \boldsymbol{x} + \boldsymbol{v} t + \boldsymbol{x_0} \\ t + t_0 \\ 1 \end{pmatrix}$$ 

$\begin{pmatrix} R & \boldsymbol{v} & \boldsymbol{x_0} \\ 0 & 1 & t_0 \\ 0 & 0 & 1 \end{pmatrix}$ is then a transformation, and these transformations form the group $\text{Gal}(n)$.

$\text{Gal}(n)$ has some named subgroups that have physical sense. 

![](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image013.png)

$\text{Gal}(4)$ spans $10$ dimensions. 

### Relationship to Relativity

1. In Newtonian spacetime, space distance is purely spatial, and time difference is purely of time.


1. All Galilean transformations preserve the 3-dimensional Euclidean distance and time difference respectively.

These changes in the spacetime of *general relativity*, where space and time are interwoven.