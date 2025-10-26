---

title: "Blog 7—The Unification of General Relativity with Cosmology."
date: 2025-10-26
categories: [Astrophysics, Cosmology, General Relativity, Spacetime Fabric, FLRW Metric]
use_math: true
layout: single
author_profile: true
read_time: true
comments: true
excerpt: "One of the biggest triumphs of physics is the emergence of General Relativity. When it is tied with Cosmology, we can model the universe with unprecedented accuracy. Today, we discuss the metric that lies at the heart of it all."

---

## Introduction
In modern cosmology, everything begins with a metric, which is a mathematical recipe for measuring distances and intervals in spacetime. Just as Pythagoras’ theorem tells us how to measure straight lines in flat space (see blog 5), general relativity tells us how to measure distances and times in a curved, evolving universe.

One of the most powerful and widely used metrics in cosmology is the Friedmann–Lemaître–Robertson–Walker (FLRW) metric. It captures the most fundamental symmetries of our universe: that it looks the same everywhere (homogeneity) and in every direction (isotropy). These symmetries means that the universe is unchanged under rotation and translation. These assumptions may sound bold, but astonishingly, astronomical observations such as the cosmic microwave background (CMB) and the large-scale distribution of galaxies confirm them to remarkable precision. 

In today’s blog, we’ll take a step-by-step look at how the FLRW metric is built from symmetry arguments, and then attempt to calculate the curvature of the metric. This is a natural progression of blog 5, and unifies general relativity with cosmology. The satisfaction of our assumptions naturally give rise to 3 cases, which will be elegantly encompassed in the final form of the FLRW metric.


## Case 1: The Flat Universe
We begin by reminding ourselves that spacetime is inherently 4-dimensional, with 3 for space and 1 for time, and so it will be represented by a $$4 \times 4$$ matrix. The Minkowski metric lays out the basic structure for a flat universe:
    
$$
g_{\mu\nu} =
\begin{bmatrix}
-1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1
\end{bmatrix}
$$

which you can treat as a baseline metric tensor for spacetime illustrations. The method of determining distance for any metric $$g_{\mu\nu}$$ has already been discussed in blog 5. This particular metric has the mostly positive convention, meaning that all space-related components are written with positive signs and time has a negative sign. This distinction is important in order to distinguish between time and space, mathematically. Similarly, one can also follow a mostly negative convention where the signs are inverted, but the mathematics remains the same. 

Following the assumptions, the most obvious choice of shape would be a flat universe. 

### The Flat Universe in Spherical Coordinates
The Minkowski metric can be written in the form of spherical coordinates:

$$
g_{\mu\nu} =
\begin{bmatrix}
-1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & r^2 & 0 \\
0 & 0 & 0 & (r\sin{\theta})^2
\end{bmatrix}
$$

This is the polar coordinate form, which arises from a Jacobian matrix transformation and you might have studied it if you have taken an introduction to calculus course. Since this post focuses on the cosmological side, I will not derive this transformation here. 


## Case 2: The Spherical Universe
    
The assumption of homogeneity and isotropy can also be applied to a spherical surface, which by design has rotational symmetry and can easily accommodate translational symmetry also. In order to describe it mathematically, we need to be able to draw spheres using just equations, which is an interesting journey to embark on.

### Constructing Higher-Dimensional Spheres

Let's now see what a sphere looks like as you progress from low dimensions, to high ones. Any shape that satisfies the equation:

$$
\sum_{i=1}^{i>2} x_i^2=r^2
$$

automatically qualifies as a sphere where $$x_i$$ is the basis parameter for a system and r is the radius of the sphere. Let's begin with the simplest case: a 1-Sphere, also referred to as a circle in 2 dimensions. Two dimensions imply that we will have 2 basis parameters where:
$$x_i=x, \quad and \quad x_j=y$$

Now it becomes a matter of selection x and y, as functions of r and $$\theta$$ to ensure that the condition of a sphere is satisfied. If we choose:

$$ 
x=r\cos{\theta} ,\quad y=r\sin{\theta}
$$

then squaring both sides and adding them yields:

$$
x^2+y^2=(r\cos\theta)^2+(r\sin\theta)^2
= r^2(\cos^2\theta+\sin^2\theta)=r^2\cdot 1=r^2,
$$
  
which satisfies the equation of a sphere. 
Extending this concept to 3 dimensions gives us 3 parameters (x, y and z), which now need to be defined as functions of 3 polar coordinates (r,$$\theta$$ and $$\varphi$$). By letting 

$$ 
x = r\cos\theta, \quad
y = r\sin\theta\cos\varphi, \quad
z = r\sin\theta\sin\varphi
$$

and repeating the procedure of squaring all side and adding them up, we get:

$$
\begin{aligned}
x^2 + y^2 + z^2
&= (r\cos\theta)^2 + (r\sin\theta\cos\varphi)^2 + (r\sin\theta\sin\varphi)^2 \\
&= r^2\cos^2\theta + r^2\sin^2\theta(\cos^2\varphi + \sin^2\varphi) \\
&= r^2\cos^2\theta + r^2\sin^2\theta \cdot 1 \\
&= r^2(\cos^2\theta + \sin^2\theta) \\
&= r^2.
\end{aligned}
$$

This is a 3-dimensional sphere, which is the most popular shape in the universe, since everything from atoms to stars, planets and globular clusters are spheres. And under this case, it might be true that the universe itself might be a sphere.

But, we need a 4-dimensional analogue to this sphere, which will now requires 4 Euclidean parameters (x,y,z and t) to be described as functions of 4 polar coordinate parameters (r, $$\theta$$, $$\varphi$$ and $$\xi$$). We can extend the pattern and select the Euclidean coordinates as:

$$
x = r\cos\theta 
$$

$$
y = r\sin\theta\cos\varphi
$$

$$
z = r\sin\theta\sin\varphi\cos\xi
$$

$$
t = r\sin\theta\sin\varphi\sin\xi
$$

Now we form the sum of squares and simplify:

$$
\begin{aligned}
x^2 + y^2 + z^2 + t^2
&=(r\cos\theta)^2 + (r\sin\theta\cos\varphi)^2 + (r\sin\theta\sin\varphi\cos\xi)^2 + (r\sin\theta\sin\varphi\sin\xi)^2 \\
&= r^2\cos^2\theta + r^2\sin^2\theta\cos^2\varphi + r^2\sin^2\theta\sin^2\varphi\cos^2\xi + r^2\sin^2\theta\sin^2\varphi\sin^2\xi \\
&= r^2\cos^2\theta + r^2\sin^2\theta\cos^2\varphi + r^2\sin^2\theta\sin^2\varphi\big(\cos^2\xi+\sin^2\xi\big) \\
&= r^2\cos^2\theta + r^2\sin^2\theta\cos^2\varphi + r^2\sin^2\theta\sin^2\varphi \\
&= r^2\cos^2\theta + r^2\sin^2\theta\big(\cos^2\varphi+\sin^2\varphi\big) \\
&= r^2\cos^2\theta + r^2\sin^2\theta\cdot 1 \\
&= r^2\big(\cos^2\theta+\sin^2\theta\big) \\
&= r^2 \cdot 1 = r^2.
\end{aligned}
$$

Hence, every point (x,y,z,t) given by the above parameterization satisfies

$$
x^2+y^2+z^2+t^2 = r^2,
$$

which is the defining equation of the 3-sphere of radius r embedded in 4 dimensions.

<!-- The Sphereical Universe -->
<p align="center">
  <img src="/assets/images/Adobe Express - SphericalUniversePicture.gif" width="500" alt="The Continuity Equation"/>
  <br><em>Figure 1: A Visualization of the Spherical Universe embedded in the aforementioned mathematics. It can be identified by 2 intersecting smiles or 2 intersecting frowns.</em>
</p>

Technically, this pattern can be extended to whatever dimensions you want, but for our purposes, we can stop here. This encapsulates the beauty of mathematics, since it does not fail even where our sense do. There is no intuitive way we can visualize anything with 4 dimensions or more, but by following mathematical patterns, we see that mathematics has no limits.  Now, let's define the partial derivatives for all the Euclidean parameters with respect to the polar coordinate parameters as they will help us in constructing the matrix later on.

### Computing the Partial Derivatives

The partial derivative with respect to $$\theta$$ is given by: 

$$
\frac{\partial}{\partial\theta}
\big(x,y,z,t\big)=
\begin{pmatrix}
\frac{\partial x}{\partial\theta}\\
\frac{\partial y}{\partial\theta}\\
\frac{\partial z}{\partial\theta}\\
\frac{\partial t}{\partial\theta}
\end{pmatrix}=
\begin{pmatrix}
-r\sin\theta\\
r\cos\theta\cos\varphi\\
r\cos\theta\sin\varphi\cos\xi\\
r\cos\theta\sin\varphi\sin\xi
\end{pmatrix}
$$

The partial derivative with respect to $$\varphi$$ is given by:

$$
\frac{\partial}{\partial\varphi}
\big(x,y,z,t\big)=
\begin{pmatrix}
0\\
\frac{\partial y}{\partial\varphi}\\
\frac{\partial z}{\partial\varphi}\\
\frac{\partial t}{\partial\varphi}
\end{pmatrix}=
\begin{pmatrix}
0\\
-r\sin\theta\sin\varphi\\
r\sin\theta\cos\varphi\cos\xi\\
r\sin\theta\cos\varphi\sin\xi
\end{pmatrix}.
$$

The partial derivative with respect to $$\xi$$ is given by:

$$
\frac{\partial}{\partial\xi}
\big(x,y,z,t\big)=
\begin{pmatrix}
0\\
0\\
\frac{\partial z}{\partial\xi}\\
\frac{\partial t}{\partial\xi}
\end{pmatrix}=
\begin{pmatrix}
0\\
0\\
-r\sin\theta\sin\varphi\sin\xi\\
r\sin\theta\sin\varphi\cos\xi
\end{pmatrix}.
$$

We can construct the metric tensor using these partial derivatives.

The induced metric on the 3-sphere in 4 dimensions is given by computing the coordinate basis vectors $$\partial_\theta$$, $$\partial_\varphi$$, $$\partial_\xi$$ and taking their dot products:

$$
g_{ij} = \partial_i \mathbf{X}\cdot \partial_j \mathbf{X},\qquad
\mathbf{X}(\theta,\varphi,\xi)=(x,y,z,t).
$$

Since we have already established that the metric tensor is essentially a 'ruler' that molds itself to the geometry involved (see blog 5), it makes sense for it to be displayed as a dot product of the basis vectors which are partial derivatives operators in their respective directions. 
Let's now display the derivatives:

$$
\partial_\theta X=
\begin{pmatrix}
-r\sin\theta \\
r\cos\theta\cos\varphi \\
r\cos\theta\sin\varphi\cos\xi \\
r\cos\theta\sin\varphi\sin\xi
\end{pmatrix},\qquad
\partial_\varphi\mathbf{X}=
\begin{pmatrix}
0 \\
-r\sin\theta\sin\varphi \\
r\sin\theta\cos\varphi\cos\xi \\
r\sin\theta\cos\varphi\sin\xi
\end{pmatrix},
$$

$$
\partial_\xi\mathbf{X}=
\begin{pmatrix}
0 \\
0 \\
-r\sin\theta\sin\varphi\sin\xi \\
r\sin\theta\sin\varphi\cos\xi
\end{pmatrix}.
$$

### The Diagonal Components

We compute the three diagonal metric components $$g_{\theta\theta},g_{\varphi\varphi},g_{\xi\xi}$$.

$$
\begin{aligned}
g_{\theta\theta}
&= \partial_\theta\mathbf{X}\cdot\partial_\theta\mathbf{X} \\
&= r^2\sin^2\theta + r^2\cos^2\theta\cos^2\varphi + r^2\cos^2\theta\sin^2\varphi(\cos^2\xi+\sin^2\xi) \\
&= r^2\sin^2\theta + r^2\cos^2\theta\big(\cos^2\varphi+\sin^2\varphi\big) \\
&= r^2\sin^2\theta+\cos^2\theta) 
= r^2.
\end{aligned}
$$

$$
\begin{aligned}
g_{\varphi\varphi}
&= \partial_\varphi\mathbf{X}\cdot\partial_\varphi\mathbf{X} \\
&= r^2\sin^2\theta\sin^2\varphi + r^2\sin^2\theta\cos^2\varphi(\cos^2\xi+\sin^2\xi) \\
&= r^2\sin^2\theta\big(\sin^2\varphi+\cos^2\varphi\big) 
= r^2\sin^2\theta.
\end{aligned}
$$

$$
\begin{aligned}
g_{\xi\xi}
&= \partial_\xi\mathbf{X}\cdot\partial_\xi\mathbf{X} \\
&= r^2\sin^2\theta\sin^2\varphi\big(\sin^2\xi+\cos^2\xi\big) 
= r^2\sin^2\theta\sin^2\varphi.
\end{aligned}
$$

### The Off-Diagonal Components

For $$i \neq j$$, the components vanish; for example:

$$
\begin{aligned}
g_{\theta\varphi}
&= \partial_\theta\mathbf{X}\cdot\partial_\varphi\mathbf{X} \\
&= (-r\sin\theta)\cdot 0 + (r\cos\theta\cos\varphi)(-r\sin\theta\sin\varphi) \\
&\qquad + (r\cos\theta\sin\varphi\cos\xi)(r\sin\theta\cos\varphi\cos\xi) \\
&\qquad + (r\cos\theta\sin\varphi\sin\xi)(r\sin\theta\cos\varphi\sin\xi) \\
&= r^2\cos\theta\sin\theta\big[-\cos\varphi\sin\varphi+\sin\varphi\cos\varphi(\cos^2\xi+\sin^2\xi)\big] \\
&= r^2\cos\theta\sin\theta\big[-\cos\varphi\sin\varphi+\sin\varphi\cos\varphi\big]=0.
\end{aligned}
$$

The same cancellation pattern (sine–cosine identities and $$\cos^2+\sin^2=1$$) makes $$g_{\theta\xi}=0$$ and $$g_{\varphi\xi}=0$$ as well. 
Thus the coordinate basis is orthogonal and all off-diagonal terms vanish. Another way of making sense of this result is by noting that the dot product of two orthogonal quantities will always yield zero by design, so all off-diagonal elements go to zero.

So the final form of the space-like components of the metric tensor turns out to be:

$$
g_{ij} =
\begin{bmatrix}
r^2 & 0 & 0 \\
0 & r^2\sin^2\theta & 0 \\
0 & 0 & r^2\sin^2\theta \sin^2\varphi
\end{bmatrix}.
$$

So the final form that incorporates the time-like component for a sphere with unit radius gives us:

$$
g_{ij} =
\begin{bmatrix}
-1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & \sin^2\theta & 0 \\
0 & 0 & 0 & \sin^2\theta \sin^2\varphi
\end{bmatrix}.
$$

Since the coordinates are arbitrary, we can relabel them like so:

$$\theta \to \xi, \quad \varphi \to \theta, \quad \xi \to \varphi$$


$$
g_{\mu\nu} =
\begin{bmatrix}
-1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & \sin^2\xi & 0 \\
0 & 0 & 0 & \sin^2\xi \sin^2\theta
\end{bmatrix}.
$$

The purpose was to  make the metric resemble to that of case 1 (flat universe) with $$r=\sin\xi$$.


## Case 3: The Hyperbolic Universe

The third case is of a hyperbolic or open universe, which is the geometrical opposite of a sphere since it is an open shape, and is therefore difficult to visualize. It's mathematics is exactly the same as that of the spherical universe which we just described, with the only different being that $$r=\sinh{\xi}$$ instead to $$r=\sin{\xi}$$, and so it's metric can be written as:

$$
g_{\mu\nu} =
\begin{bmatrix}
-1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & \sinh^2\xi & 0 \\
0 & 0 & 0 & \sinh^2\xi \,\sin^2\theta
\end{bmatrix}.
$$

<!-- The Hyperbolic Universe -->
<p align="center">
  <img src="/assets/images/Adobe Express - HyperbolicUniversePicture.gif" width="500" alt="The Continuity Equation"/>
  <br><em>Figure 2: The Hyperbolic Universe can be identified by an intersecting frown and smile.</em>
</p>

The underlying geometry for a hyperbolic universe is the mathematical dual of the spherical case, and the derivation is left to the reader.

## Unification of the 3 cases

The results can be compressed into a single metric with different cases:

$$
g_{\mu\nu} =
\begin{bmatrix}
-1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & r^2 & 0 \\
0 & 0 & 0 & r^2\sin^2\theta
\end{bmatrix}.
$$

where:

+  $$r=\xi$$ for flat universe
+  $$r=\sin\xi$$ for closed universe (spherical)
+  $$r=\sinh\xi$$ for open universe (hyperbolic)

### Introducing the Scale Factor

Now we introduce a term that stretches the fabric of space itself. We introduce such a scale factor a(t) which attaches itself to the basis vectors and allows us to study the dynamics of a universe whose volume changes with time. As it was hinted earlier that the metric element is a dot product if two basis vectors, the space-like elements now transform:

$$x_i\to a(t)x_i$$
$$x_j\to a(t)x_j$$

since $$g_{ij} = x_i.x_j$$,
we get

$$
g_{ij}\to(a(t))^2x_i.x_j\to(a(t))^2g_{ij}
$$

So, we can apply this onto the space-like elements. The time-like element remains unchanged because it is the very thing that we are accounting for here. In other words, the speed of time does not change because of the scale factor, and so it is not included in the time component of the metric, which now takes up the form:

$$
g_{\mu\nu} =
\begin{bmatrix}
-1 & 0 & 0 & 0 \\
0 & a^2 & 0 & 0 \\
0 & 0 & a^2r^2 & 0 \\
0 & 0 & 0 & a^2r^2\sin^2\theta
\end{bmatrix}.
$$

Now, we need and all-encompassing form of the metric that includes all 3 geometries.

<!-- Animation of vacuum fluctuations -->
<p align="center">
  <img src="/assets/images/Adobe Express - FlatUniverse.gif" width="500" alt="The Continuity Equation"/>
  <br><em>Simulation 1: The effect of the scale factor on the proper distance between two points in flat space. Remarkably, this simulation applies to all three curvature cases, because any expanding universe, when viewed closely enough, can be approximated as flat. This illustrates how the scale factor locally shapes the geometry of any universe.</em>
</p>

### Coordinate Transformation and the Final FLRW Metric

Let's consider a change in coordinates. To do that, we need to get into the fundamental nature of the basis vectors. If we write the basis vector as an operator. We can write the basis vector pointing in the i direction as:

$$e_i=\frac{\partial}{\partial{x_i}}$$

So for a vector with zero component in the i direction, its derivative with respect to i will also yield zero. This operator treatment is a powerful tool when we analyze the metric tensor as a product of the basis vectors:

$$g_{ij}=e_ie_j=\frac{\partial}{\partial{x_i}}.\frac{\partial}{\partial{x_j}}$$

Let's also remind ourselves that our metric has the form:

$$
g_{\mu\nu} =
\begin{bmatrix}
g_{tt} & 0 & 0 & 0 \\
0 & g_{\xi\xi} & 0 & 0 \\
0 & 0 & g_{\theta\theta} & 0 \\
0 & 0 & 0 & g_{\varphi\varphi}
\end{bmatrix}.
$$

where $$g_{\xi\xi}$$ can be expressed in the form of r as written earlier. Now, let's actually express the metric purely as r. How can we do that? easy. 

The aim is to perform a transformation such that:

$$
g_{\xi\xi} \to g_{rr}
$$

That is straightforward when you use the chain-rule:

$$
\frac{\partial}{\partial{\xi}}=\frac{\partial}{\partial{r}}\frac{\partial r}{\partial{\xi}}
$$

Therefore, 

$$
g_{\xi\xi}=e_\xi.e_\xi=\frac{\partial}{\partial{\xi}}\frac{\partial}{\partial{\xi}}
$$

$$
g_{\xi\xi}=(\frac{\partial}{\partial{r}}\frac{\partial r}{\partial{\xi}})(\frac{\partial}{\partial{r}}\frac{\partial r}{\partial{\xi}})
$$

$$
g_{\xi\xi}=(\frac{\partial r}{\partial{\xi}})^2\frac{\partial }{\partial{r}}\frac{\partial }{\partial{r}}=(\frac{\partial r}{\partial{\xi}})^2g_{rr}
$$



+ For flat space, recall that $$r=\xi$$, therefore $$(\frac{\partial r}{\partial{\xi}})^2=1$$. So in this case, $$g_{rr}=g_{\xi\xi}$$.
+ For spherical space, recall that $$r=\sin\xi$$, therefore $$(\frac{\partial r}{\partial{\xi}})^2=\cos^2\xi=1-\sin^2\xi=1-r^2$$. So, $$g_{rr}=\frac{g_{\xi\xi}}{1-r^2}$$.
+ For hyperbolic space, recall that $$r=\sinh\xi$$, therefore $$(\frac{\partial r}{\partial{\xi}})^2=\cosh^2\xi=1+\sinh^2\xi=1+r^2$$. So, $$g_{rr}=\frac{g_{\xi\xi}}{1+r^2}$$.


Now, because of the elegant final form $$g_{rr}$$ takes, we can compactly change $$g_{\xi\xi}$$, so that it takes the form:

$$
g_{rr}=\frac{g_{\xi\xi}}{1-kr^2}
$$

So, the FLRW metric can be written as:

$$
g_{\mu\nu} =
\begin{bmatrix}
-1 & 0 & 0 & 0 \\
0 & \frac{a^2}{1-kr^2} & 0 & 0 \\
0 & 0 & r^2 & 0 \\
0 & 0 & 0 & r^2\sin^2\theta
\end{bmatrix}.
$$

The most common form in literature is:

$$
ds^2 = -dt^2 + a(t)^2 \left[ \frac{dr^2}{1 - k r^2} + r^2 (d\theta^2 + \sin^2\theta\, d\phi^2) \right]
$$



where $$k=-1,0,1$$ corresponds to hyperbolic (open), flat and spherical (closed) geometries, respectively. It is important to note that everything else stays the same, because we transform $$\xi \to r$$,so r staying as is, is a matter of convention. The only difference is the change in the elements $$g_{\xi\xi} \to g_{rr}$$, which we have already incorporated. So, now you have a metric tensor that is highly relevant to cosmology, so much so that a cosmology course looks incomplete without at least mentioning this metric. Now that we have put in the hard yards, we can calculate everything from geodesics, to real distance, and curvature using straightforward but lengthy mathematics. 


Luckily for us, we live in the age of computers, and we can easily code this without needing pen or paper. I have prepared a mathematica notebook code which calculates inputs the FLRW metric and calculates it's curvature using the Christoffel symbol, Riemann tensor, Ricci Tensor and Ricci scalar. They deserve their own code-oriented post which is left for a future blog.  

The analytical calculation for a $$3 \times 3$$ metric's case:
https://www.physics.mcgill.ca/~rhb/ph514/10sol6.pdf

What began as a geometric argument about how to measure distances in a symmetric universe has now yielded the FLRW metric, which is the mathematical foundation of the Big Bang model. Every modern cosmological calculation, from the expansion of the universe to the CMB anisotropies, begins here.
Feel free to access the links and as always, keep on physicsing.

## References

S. Weinberg, Gravitation and Cosmology: Principles and Applications of the General Theory of Relativity, Wiley (1972). — A foundational text that rigorously develops the FLRW metric and its cosmological implications.

C.W. Misner, K.S. Thorne, and J.A. Wheeler, Gravitation, W.H. Freeman (1973). — The definitive reference for the geometric and physical interpretation of spacetime metrics in general relativity.

S. Carroll, Spacetime and Geometry: An Introduction to General Relativity, Addison-Wesley (2004). — Excellent modern treatment of cosmological metrics, curvature tensors, and the derivation of the FLRW metric.

R.M. Wald, General Relativity, University of Chicago Press (1984). — A mathematically rigorous text that includes detailed discussions on curvature, symmetry, and spacetime dynamics.

J.B. Hartle, Gravity: An Introduction to Einstein’s General Relativity, Addison-Wesley (2003). — Provides an accessible and conceptual development of cosmological solutions including the FLRW metric.

E. Hubble, A Relation Between Distance and Radial Velocity Among Extra-Galactic Nebulae, Proceedings of the National Academy of Sciences 15 (1929). — The original paper establishing cosmic expansion, motivating the time-dependent scale factor a(t).

M. Hobson, G. Efstathiou, and A. Lasenby, General Relativity: An Introduction for Physicists, Cambridge University Press (2006). — A clear and modern reference for the derivation and physical interpretation of the Friedmann equations.

Note: All figures, illustrations, and Mathematica simulations are original content created by the author unless stated otherwise in the caption.

## For the Curious Learner

https://www.youtube.com/watch?v=iERBF2_TnXo
  




