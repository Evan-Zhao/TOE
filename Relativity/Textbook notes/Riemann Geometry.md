# Riemann Geometry

$$
\newcommand{\R}{\mathbb{R}}
\newcommand{\C}{\mathbb{C}}
\newcommand{\T}{\mathcal{T}}
$$

## Manifold

### Definition

A manifold $M$ is a set together with some subsets of this set, denoted as $\{O_\alpha\}$, such that:

![](Manifold_1.png)

We'll only be considering manifolds that are *Hausdroff* and *paracompact*, which are explained in Appendix A of the textbook.

### Diffeomorphism

Two manifolds $M$ (charts $\{\psi\}$) and $N$ (charts $\{\psi'\}$)are diffeomorphic iff there exists a function $f: M \to N$, so that $\forall \alpha \forall \beta \quad \psi'_\alpha \circ f \circ \psi_\beta^{-1} \in C^\infty$.

### Tangent Space

#### Directional Derivative

* In flat space $\R^n$, a vector is naturally equivalent to a *directional derivative operator*, by 

  $$v \to \sum v^\mu \frac{\partial}{\partial x^\mu}$$

* There are two properties special about this operator:

  1. Linearity, $v(f + g) = v(f) + v(g)$;
  2. Leibnitz rule, $v(f g) = f v(g) + g v(f)$.

#### Tangent Vector

* We'll *define a tangent vector on manifold* as a directional derivative operator by having it obey these two rules.
* Consequence: 
  * property 1 shows that tangent vector at given point $p$ forms a vector space: **tangent space**.
  * Theorem 2.2.1: the dimension of tangent space at any $p$ is the same as the dimension of manifold.

#### Tangent Space, Basis

<div id="tangent_space_basis"></div>

* Theorem 2.2.1 yields the *coordinate basis* of the tangent space at $p$, $T_p$, as
  $$
  X_\mu(f) = \left. \frac{\partial}{\partial x^\mu} (f \circ\psi^{-1}) \right|_{\psi(p)}
  $$
  This basis *vary with the chart*, but will be linearly independent and span $n$ dimension.

  Any vector $v$ on the manifold can be expressed as a linear combination of $X_\mu$, with
  $$
  v=\sum v(x^\mu \circ \psi) X_\mu
  $$
  With $x^\mu$ the coordinate map, $x^\mu : x \to x^\mu$.

* Usually $X_\mu$ is denoted as simply $\frac{\partial} {\partial x^\mu}$, displaying the fact that the existence of $\psi$ (chart) is often ignored.

* Change of basis is needed when shifting between different charts. Chain rule:
  $$
  X_\mu = \sum_{\nu} \frac{\partial x'^\nu}{\partial x^\mu} X_\nu'
  $$

* Vector transformation law (contravariant vectors):
  $$
  v'^\nu = \sum_{\nu} \frac{\partial x'^\nu}{\partial x^\mu} v^\mu
  $$





### Curve

A curve on a manifold is given by $\gamma:\R \to M$, as in flat space $\R^n$.

The tangent vector of this curve can be found in $\R^n$ using charts:
$$
T_\gamma(f) = \sum_{\mu} \frac{d \gamma_{\R}}{d t} X_\mu(f); \\
T_\gamma = \sum_{\mu} \frac{d \gamma_{\R}}{d t} X_\mu
$$
where $\gamma_\R = \psi \circ \gamma$. (In textbook this thing is written as $x^\mu$, perhaps in the sense that curve in $\R^n$ is contravariant.)

With respect to the basis vectors, the components of tangent vector are
$$
T^\mu = \frac{d \gamma_\R}{d t}; T = D \gamma_\R \cdot X
$$
Curves are important because it defines a *connection* between tangent spaces at different points of the manifold which are otherwise not related, defining a *parallel transport* of a vector at $p$ towards $q$ along it.

### Tangent Field

By picking out a vector $v$ from the tangent space $V_p$ at every $p$, one get a tangent field on a manifold. The tangent field is then a function
$$
v: M \to TM \qquad v(p) \in V_p
$$
where $TM$ is the tangent bundle of $M$. This will be explained later.

$v(p)$ is also denoted as $v|_p$ because $v|_p$ is also itself a function, and we may wish to append its argument, like in $v|_p (f)$.

While it's yet impossible to relate tangent vectors at different points, there is a natural notion of smoothness in a vector field: since $v|_p$ can be applied onto functions, $v$ is called *smooth* iff
$$
\forall f \in C^\infty \quad \left( v|_\cdot (f): M \to \R \right) \in C^\infty
$$
Also, $v$ is smooth iff its components $v^\mu$ are all smooth ($v^\mu: M \to \R$).

### "Infinitesimal Displacement"

To see tangent vectors as *infinitesimal displacement* as we have pointed out, the following concept will help.

#### Diffeomorphism Group

A *one-parameter group of diffeomorphisms*, $\phi$, is defined as a $C^\infty$ map $\phi : \R \times M \to M$, such that

1. With respect to second argument (with first fixed, i.e., $\phi_t : M \to M$): $\forall t, \phi_t$ is a diffeomorphism.
2. With respect to first argument, these diffeomorphisms form a group, by
   * $\phi_0 = I$
   * $\forall t, s \in \R, \phi_t \circ \phi_s = \phi_{t+s}$

This $\phi$ can be understood as a *smooth transformation* of this manifold regarding $t$.

The orbit of a point $p$ in this transformation is a curve $\phi_\cdot(p): \R \to M$, which is also called an *orbit* for $\phi_t$. Since $\phi_t$ is diffeomorphism onto itself, all these orbits embed in $M$.

Define a tangent field $v$ , so that $v|_p$ is tangent to curve $\phi_\cdot (p)$ at  $p$; then $v$ will be a field of *infinitesimal displacement* because it describes the direction every point is moving in under $\phi$-transformation.

#### Integral Curve

Given a vector field $v$, we'd like to find the transformation $\phi$; this can be solved similarly as finding the *integral curve* in $\R^n$.

(This case on $\R^n$ is discussed in VV286.)

Generally speaking, finding integral curve on manifold reduces to solving the following system:
$$
\frac{d \gamma^\mu}{d t} = v^\mu(\gamma^1, \cdots, \gamma^n)
$$
Or more compactly (from VV286 slides, P77):
$$
D\gamma(t) = v \circ \gamma(t)
$$
Hence the reduced problem much resembles finding an integral curve in $\R^n$.

### Commutator

Given two *smooth* vector fields $u$ and $v$, one can derive another vector field, called the *commutator* of $u$ and $v$, 
$$
[v,u](f)=v[u(f)]-u[v(f)]
$$
Two vector fields occuring in same coordinate basis have a *vanishing commutator*, when we say the two vector fields *commute*, similar to the partial derivative commutativity in $\R^n$:
$$
\frac{\partial}{\partial u} \frac{\partial}{\partial v} = \frac{\partial}{\partial v} \frac{\partial}{\partial u}
$$


## Tensor

Vector has *linear* property; **tensor** arises when one considers *multilinear* properties.

Below are some *linear objects* that we are already familiar with in physics.

### Dual Vector

A collection of $n$ numbers which is only meaningful when *going with a basis*.

#### Field Strength as Dual Vector

Instance: in a magnetic field, the magnetic strength in specified direction is measured and recorded as a scalar.

Assume, then, the measurement directions $e_1, \cdots, e_n$ *form a basis* in the space, then the corresponding strength in each direction, $e^1, \cdots, e^n$ together with the basis decides the magnetic field.

The magnetic field itself is a **dual vector** because it *transforms a basis vector into a number*.

Similarly, electrical field, etc., are also dual vectors.

#### Contravariance

A vector (such as basis) transforms *covariantly*, while a dual vector transforms *contravariantly*.

We have mentioned contravariant transformation rule previously.

#### Dual Space Back and Forth

Dual vectors live in the **dual space** of a vector space, denoted as $V^*$. 

We usually see a field strength quantity as a *vector* instead of a *dual vector*, but we're actually under the assistance of **inner product**:

If the field strength is $\boldsymbol{B}$ which is seen as a vector, then we can only decide the scalar strength in a given direction using *inner product*, as
$$
B_{v} = \langle \boldsymbol{B}, \boldsymbol{v} \rangle
$$
Later we'll show that an inner product (more generally, a **metric**) enables the back and forth *transformation between covariant and contravariant quantities*. 

Conversely, a *vector* field strength is useless if the given space is not a metric space.

### Dual Space

For main content, consult VV285.

Since the basis of $V^*$ is decided by the choice of basis in $V$,  we say that $V$ and $V^*$ are *not naturally isomorphic*, in that the isomorphism between $V$ and $V^*$ rely on *preferred basis*.

We'll see that a *metric* actually determine this isomorphism as well, that's why metric enables the conversion between covariance and contravariance.

### Double Dual Space

A **double dual space**, denoted as $V^{**}$, contains elements that
$$
v^{**} \in V^{**} \Rightarrow \forall \omega^* \in V^*, \quad v^{**}(\omega^*) = \omega^*(v)
$$
This $V^{**}$ is isomorphic to $V$ with no need to add any extra structure; they are *naturally isomorphic*.

Therefore, $V^{**}$ contains no extra information than $V$, but it is a convenient way to define *pullback*.

### Tensor Definition

A tensor $T$ of type $(k,l)$ is a *multilinear map* 
$$
T: \underbrace{V^* \times \cdots \times V^*}_k \times \underbrace{V\times \cdots \times V}_l \to \R
$$
Given $k$ dual vectors and $l$ vectors it will produce a number, and it is linear in its all arguments.

A tensor of type $(1,0)$ actually belongs to $V^{**}$, because its signature is 
$$
T_{(1,0)}: V^* \to \R
$$
But it has a naturally correspondent element in $V$.

### Tensor Space

Apparently tensors of the same type forms a linear space, $\mathcal{T}(k,l)$.

A tensor is uniquely decided by evaluating it against a basis in $V$ together with a basis in $V^*$, i.e., by filling $k$ slots with $n$ dual vectors and $l$ slots with $n$ vectors.

There are $n^{k+l}$ ways to evaluate this tensor, which is also the dimension of this vector space.

### Operations

#### Contraction

Reduce an order in both covariant and contravariant dimensions, at *specified entry*, by
$$
C: \T(k,l) \to \T(k-1,l-1), CT = \sum_{\sigma=1}^{n} T(\cdots, v^{\sigma^*},\cdots; \cdots, v_\sigma, \cdots )
$$
The contraction of a $(1,1)$ tensor is just the *trace* of the tensor, since if written as a matrix:
$$
\sum_{\sigma=1}^n T(e^{\sigma^*},e_\sigma)=\sum_{\sigma=1}^n e^{\sigma^*} \cdot T \cdot e_\sigma = \sum_{\sigma=1}^n e^{\sigma^*} T_{\cdot \sigma} = \sum_{\sigma=1}^n T_{\sigma \sigma}
$$

#### Outer Product

Outer product $\otimes$ combines two tensors into a tensor:
$$
\begin{align}
\otimes: \T(l,k) \times \T(l',k') &\to \T(l+l',k+k') \\
(T\otimes T') (v^1,\cdots, v^{l+l'};v_1,\cdots, v_{k+k'}) &= T(v^1,\cdots, v^{l};v_1,\cdots, v_{k}) \cdot T'(v^{l+1},\cdots, v^{l};v_{k+1},\cdots, v_{k})
\end{align}
$$
Apparently, outer product **does not commute**. (Similar to the non-commutativity of matrices.)

##### Tensor Decomposition

Outer product provides a way to construct tensor from outer product of vectors and dual vectors. 

A tensor that can be represented as such a product is called **simple**; otherwise, it can be always represented as a *linear combination* of simple tensors:
$$
T = \sum_{\mu_1 = 1}^n \cdots \sum_{\mu_k = 1}^n  \sum_{\nu_1 = 1}^n \cdots \sum_{\nu_l = 1}^n T^{\mu_1\cdots \mu_k}_{\nu_1\cdots \nu_l} e_{\mu_1} \otimes \cdots \otimes e_{\mu_{k}} \otimes e^{\nu_1} \otimes \cdots \otimes e^{\nu_l}
$$
Recall that in a $n$-dimensional vector space, the dimension of tensor space $\T(l,k)$ is $n^{l+k}$.

By picking out $l$ from $n$ dual vector basis and $k$ from $n$ vector basis and taking their outer product, we can apparently get $n^{k+l}$ simple tensors as the *basis of tensor space*.

##### Simple Tensors

Not all tensors are simple. 

~~Proof eliminated~~

### Components

In the expansion
$$
T = \sum_{\mu_1 = 1}^n \cdots \sum_{\mu_k = 1}^n  \sum_{\nu_1 = 1}^n \cdots \sum_{\nu_l = 1}^n T^{\mu_1\cdots \mu_k}_{\nu_1\cdots \nu_l} e_{\mu_1} \otimes \cdots \otimes e_{\mu_{k}} \otimes e^{\nu_1} \otimes \cdots \otimes e^{\nu_l}
$$
Scalar $T^{\mu_1\cdots \mu_k}_{\nu_1\cdots \nu_l}$ is called the **component** of $T$ (with respect to basis $\{e_{\mu}\}$). 

This allows the *multi-dimensional array comprehension* of tensor, which may be useful in actual calculation.

In components expression, we can rewrite the two operations above.

Contraction:
$$
CT = \sum_{\sigma = 1}^n T^{\mu_1 \cdots \sigma \cdots \mu_k}_{\nu_1 \cdots \sigma \cdots \nu_l}
$$
Tensor product:
$$
(T \otimes T')^{\mu_1 \cdots \mu_{k+k'}}_{\nu_1 \cdots \nu_{l+l'}} = T^{\mu_1 \cdots \mu_{k}}_{\nu_1 \cdots \nu_{l}} T'^{\mu_{k+1} \cdots \mu_{k+k'}}_{\nu_l \cdots \nu_{l+l'}}
$$

### Covariance, Contravariance

Dual vectors are also called **covectors**. *Co-* is a common prefix denoting *duality*.

In our discussion, the dual space of tangent space $T_p$ at point $p$ of the manifold is called **cotangent** space $T_p^*$. Its elements $v^* \in T_p^*$ are called **cotangent vector**, much as $v \in T_p$ is called tangent vector.

Ordinary vectors, such as elements in tangent space, are also called **contravariant vectors** because they (more precisely, their components) are subject to *contravariant transformation law*:
$$
v'^\nu = \sum_{\mu} \frac{\partial x'^\nu}{\partial x^\mu} v^\mu
$$
We have mentioned this under the heading [Tangent Space, Basis](#tangent_space_basis).

Conversely, covectors are subject to *covariant law*, 
$$
\omega'_{\nu} = \sum_{\mu} \frac{\partial x^\mu}{\partial x'^\nu} \omega_\mu
$$
which just states that it transforms *in opposite direction* than ordinary vectors.

Interestingly, *components* of contravariant vectors are written with super-index ($v^\mu$), while contravariant vectors themselves are written with sub-index (such as basis, $e_\mu$); vice versa.

For an additional material on covariance and contravariance, consult [covariance and contravariance](transformation.md).

#### Tensor Transformation Law

A tensor of type $(k,l)​$ transforms in both directions:
$$
T'^{\mu'_1\cdots \mu'_k}_{\nu'_1\cdots \nu'_l} = \sum_{\mu_1 = 1}^n \cdots \sum_{\mu_k = 1}^n  \sum_{\nu_1 = 1}^n \cdots \sum_{\nu_l = 1}^n T^{\mu_1\cdots \mu_k}_{\nu_1\cdots \nu_l} \frac{\partial x'^{\mu'_1}}{\partial x^{\mu_1}} \cdots \frac{\partial x^{\nu_l}}{\partial x'^{\nu'_l}}
$$
But notice that its covariant entry transforms *contravariantly*, and contravariant entry *covariantly*.

This is because *covariant vectors* transform covariantly, and covariance (provided by covariant *vectors*) should pair with contravariance (provided by covariant *slots*); vice versa.

#### Transformation and Notation

|                        | Covariance                              | Contravariance                      |
| ---------------------- | --------------------------------------- | ----------------------------------- |
| 1-rank name            | Dual vector (covector)                  | Vector                              |
| 1-rank instance        | $V^*$ basis $dx^\mu$                    | $V$ basis $\partial/\partial x^\mu$ |
| In tensor type $(k,l)$ | $(\cdot, l)$ (first entry)              | $(k,\cdot)$ (second entry)          |
| Components index       | sub-index ($\omega_\mu$)                | super-index ($v^\mu$)               |
| Self index             | super-index ($\boldsymbol{\omega}^\mu$) | sub-index ($\boldsymbol{e}_{\mu}$)  |

### Tensor Field

A tensor field (on manifold) is an assignment
$$
T: M \to \T(k,l)
$$
while a smooth tensor field is defined similarly as the smooth of vector field: if $T$ is smooth then for all smooth vector and covector fields $v_1, \cdots, v_l; \omega^1, \cdots, \omega^k$, 
$$
T(v_1, \cdots, v_l; \omega^1, \cdots, \omega^k) \in C^\infty
$$

### Metric

Conceptually, a metric should contain information on "infinitesimal *squared* distance" of an "infinitesimal displacement".

Denoted by $g$, a metric of a space is formally
$$
g:
$$
