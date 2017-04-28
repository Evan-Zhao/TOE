# Minkowski spacetime

 

## Overview

 

- Minkowski spacetime has an *origin*, in order to make it vector space. The "central" event does not exist physically, origin is only for mathematical convenience.


- Minkowski space is 

- - 4-dimensional vector space (isomorphic to $\mathbb{R}^4$) 

  - equipped with a 

  - - nondegenerate, symmetric bilinear form on the tangent space at each point
    - called the *Minkowski inner product*
    - with a metric signature either $(−,+,+,+)$ or $(+,−,−,−)$

  - the tangent space at each event is a vector space of the same dimension as spacetime, $4$.


- Minkowski space is "flat", in the same way Euclidean space is, but does not have a *positive-definite* metric; in other words, some vector in this space could have negative metric, hence it is called a *pseudo-Euclidean* space. 



## Minkowski Metric

The [Special Relativity Invariant]() is the spacetime interval kept invariant in reference frame change, $\pm \left( c^2 (t_1-t_2)^2 - (x_1-x_2)^2 - (y_1-y_2)^2 - (z_1-z_2)^2 \right)$

Calculating the distance between any event and the"origin" yields $ || v ||^2 = \pm (c^2 t^2 - x^2 - y^2 - z^2)$; this quadratic form further yields a bilinear form: $ u \cdot v = \pm (c^2 t_1 t_2 - x_1x_2-y_1y_2-z_1z_2)$. 

The metric tensor is either of the following two according to different conventions:

1. $ \eta = \pm \begin{pmatrix} -1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix}$

   Accordingly, the speed of light is carriedin the event vector, not the tensor; $v = (ct, x, y, z)$. 

2. $ \eta = \pm \begin{pmatrix} -c^2 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix}$

   Then $v=(t,x,y,z)$. 

### Metric Signature

The pm sign correponds to the metric signature $(-,+,+,+)$ and $(+,-,-,-)$ respectively. 

In general, mathematicians and general relativists prefer the former to yield a positive sign, while particle physicists tend to use the latter. 

## Standard Basis

The bases are 4 normalized, mutually perpendicular vectors $(e_0,e_1,e_2,e_3)$, with $e_0$ carrying a negative modular; $||e_0||=-1||;e_i||=1, i\neq 0$. 

With regard to the standard basis, a vector can be written in components as $(v_0,v_1,v_2,v_3)$, $v_0$ is the *timelike* component and $v_1,v_2,v_3$ are the *spacelike* components. 

A common practice is to group the components of a vector in 1-3, as $v=(v_t,\boldsymbol{v}_s)$.  

## Lorentz Transformation

Just as [Galilean Transformation](onenote:#Newtonian%20Mechanics&section-id={01DC8783-DCD3-4A17-8B7E-F58C81978E01}&page-id={D0E228A9-D12E-447D-8547-28E5BF5B352C}&object-id={9F3381EE-917B-0CE1-1C02-FD859A886A30}&79&base-path=https://d.docs.live.net/3777c38dfdd80854/Documents/yifan's%20Notebook/Quick%20Notes.one) is a group acting on elements in Galilean spacetime, Lorentz Transformation is its counterpart on Minkowski spacetime. 

1. The mere translation of reference frame has the same form as that in Galilean     Transformation.

 

1. When there     is a relative speed between two reference frames, such transformation is     called a Lorentz Boost, and the behavior is different from that in Galilean     Transformation.

 

### Lorentz Factor

Thecoefficient associated to the ratio of length contraction and time dilation iscalled Lorentz factor, 

![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image013.png)

 

For convenience, the parameter  is alsofrequently used.![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image014.png)

 

### Lorentz Boost

Physically motivated, if a reference frame  is boostedwith speed  relative toa "stationary" frame  along -axis, then a event  in  will be , where![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image015.png)

![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image016.png)

 

TheLorentz transformations can also be derived in a way that resembles circularrotations in 3d space using the hyperbolicrotation, which could be unfamiliar to us.

 

### Lorentz Boost as Matrix

Due tothe spacetime invariance, we would require a Lorentz boost matrix to satisfy

![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image017.png)

 

This would give , similar to the case we had whendiscussing [Euclidean Group](onenote:#Newtonian%20Mechanics&section-id={01DC8783-DCD3-4A17-8B7E-F58C81978E01}&page-id={D0E228A9-D12E-447D-8547-28E5BF5B352C}&object-id={9F3381EE-917B-0CE1-1C02-FD859A886A30}&5B&base-path=https://d.docs.live.net/3777c38dfdd80854/Documents/yifan's%20Notebook/Quick%20Notes.one).![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image018.png)

 

We can write  cutting its dimensions into 3-1, that is![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image019.png)

![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image020.png)

 

From , we get  which implies  or .![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image021.png)

###  

### Homogeneous Lorentz Group

TheLorentz Group is the group of all Lorentz transformations which has 4subgroups, they come from two choices in space reflection (direct and indirectisometry, [EuclideanGroup](onenote:#Newtonian%20Mechanics&section-id={01DC8783-DCD3-4A17-8B7E-F58C81978E01}&page-id={D0E228A9-D12E-447D-8547-28E5BF5B352C}&object-id={9F3381EE-917B-0CE1-1C02-FD859A886A30}&5B&base-path=https://d.docs.live.net/3777c38dfdd80854/Documents/yifan's%20Notebook/Quick%20Notes.one)) and time symmetry.

 

| Intersection, ∩                          | Antichronous (or  non-orthochronous) LTs  ![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image022.png) | Orthochronous LTs  ![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image023.png) |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| Proper LTs  ![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image024.png) | Proper antichronous LTs                  | Proper orthochronous LTs                 |
| Improper LTs  ![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image025.png) | Improper antichronous LTs                | Improper orthochronous LTs               |

 

It can beshown that the composition of any two Lorentz transformations always has thepositive determinant and positive inequality, a properorthochronous transformation.

 

Therefore, the sets , ,, and all form subgroups, but the other sets involving the improperand/or antichronous properties do not form subgroups.![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image026.png)

 

### Proper orthochronous LTs

The boostmatrix for a proper orthochronous LT is 

![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image027.png)

where .![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image028.png)

 

In morecompact form, 

![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image029.png)

 

Hence it's more apparent that  is symmetric.![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image030.png)

 

### Communication of LTs

Apparently, if  then  commutes with .![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image031.png)

 

In moregeneral cases, when two boost are composed, the result is not a pure boost, buta boost followed (or preceded by) a rotation,and the two boost does not necessarily commute.

 

, where  is a pure space rotation matrix, in the samesense as in Galilean transformation.![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image032.png)

 

It is actually a complex procedure to relate  to the original speeds  and .![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image033.png)

 

### General LTs

A general Lorentz Transform includes a rotation and a boost, denotedas . ![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image034.png)

 

It is notnecessarily symmetric (as the boost) or orthogonal (as the rotation).

 

### The SO+(3,1) Generators

Taking the infinitesimal boost/rotation (by taking derivative ofthese at ) in  directions produces  fundamental matrices,  tranlational and  rotational.![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image035.png)

 

![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image036.png)

![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image037.png)

 

Thesereveal the fundamental symmetry of Minkowski spacetime.

 

### Inhomogeneous Lorentz group

If inaddition, translation in space/time is also considered, inhomogeneous Lorentzgroup could be more helpful.

 

In transformation , where  is the translation term,  is the behavior of this inhomogeneous Lorentz transformation,instead of merely .![img](file:///C:/Users/yifan/AppData/Local/Temp/msohtmlclip1/01/clip_image038.png)

 

This isalso called the Poincare Transformation.