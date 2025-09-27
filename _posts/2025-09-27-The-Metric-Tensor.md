---

title: "The Metric Tensor: A Self-Adapting Ruler"
date: 2025-09-27
categories: [General Relativity, Cosmology, Spacetime, Astrophysics, Tensor Calculus]
use_math: true
layout: single
author_profile: true
read_time: true
comments: true
excerpt: "The metric tensor is the universe’s measuring tape, and dictates how distances, angles, and time itself changes for different spacetimes. And you can understand all this using basic math, as will be shown."


---


## Introduction

Tensors are an overwhelming topic for most students, which is a problem since they are important if you want to get into the fun part of physics. Cosmology, general relativity, particle physics, and many more interesting fields rely on tensors. In today's blog, we'll get into a special type of tensor, gaining intuition about them along the way. Hopefully, by the end of it, you will be able to grasp what they are and how they can be used. We will go much deeper into tensors in future blogs, so stay tuned!

To understand tensors, let's firstforget what we know and start from scratch. We can then go on a journey to rediscover them. The most fundamental tensor is the metric tensor. Once we understand that, we can generalize and deepen our understanding. The prerequisites are pretty simple: all you need to know are $$7^{\text{th}}$$ grade geometry concepts like the Pythagorean theorem and the area of a triangle. Yes, it's that simple. Buckle up and let's begin.


## A Vector in a Square Grid

Let's begin with a simple 2D map where you have to go from one point to another, as shown in figure 1.

![Figure 1](/assets/images/B5P1.png)  

*Figure 1*: A vector in a Square Grid.

You ideally want to draw a line between the points and call it a vector, since a line shows the shortest path and a vector makes it easy to visualize magnitude and direction. So, in this case, you can see that the vector is 3 units along the x-axis and 4 units along the y-axis, and so by Pythagorean theorem, the shortest path between the two points is 5 units since: 

$$
5^2=3^2+4^2
$$

But, we still do not know how far away they actually are to each other since we have not defined the unit. Once we define a unit to be a kilometer, we have our metric. In the simplest of words, a metric translates geometric coordinates into real distances (for the Euclidean space in this case). So, how many numbers need to included into the metric, for it to define and translate any scenario of points in a 2D case?  

## A Vector in a Rectangular Grid

![Figure 2](/assets/images/B5P2.png)  

*Figure 2*: A vector in a Rectangular Grid.

For a square grid as shown in figure 1, we only need one number to define the metric as one unit is the equivalent to one kilometer throughout the square grid. However, we might not get as lucky for a rectangular grid, which is shown in figure 2 where the same vector is drawn on a rectangular grid. One might ask, what's the point of using a grid like this? 
Some may have even seen a grid like this for the first time since it's pretty useless, but bear with me...you'll understand the why soon.

Now, one unit along the x-axis represents one kilometer but one along the y-axis represents two kilometers. Now, we cannot directly apply the Pythagorean theorem since the units are not the same, therefore: 

$$
|v|^2 \neq 3^2 + 2^2
$$

We need to first convert the y-axis scale to be consistent with the x-axis scale in terms of units, and then recompute the distance. 

$$
|v|^2 = (1 \times 3)^2 + (2 \times 2)^2
$$

$$
|v|^2 = 3^2 + 4^2 = 5^2
$$

We reproduce the same answer for magnitude as before, which makes sense since a change in the geometry of coordinates should not change the vector's magnitude. In other words, a vector's magnitude is invariant under a transformation of the geometry of coordinates. 

Now, to determine the metric, we need two numbers, one for the x-axis and the other for the y-axis. We can write:

$$
|v|^2= g_{xx}x^2+g_{yy}y^2
$$

Here $$g_{xx}$$ and $$g_{yy}$$ are metric scalars for x and y axis respectively and have the "rectangleness" of the grid encoded in them. A critical point here is that x and y are displacements, not coordinates. Though, this convention might be a bit confusing right now, it has been intentionally kept this way as it will come in handy for a concept later on. 


## The Oblique Grid

![Figure 3](/assets/images/B5P3.png) 

*Figure 3*: A vector in an Oblique Grid.

So, with the help of the two-numbered metric, we can effectively map the rectangular grid onto the square grid. But, now, let's take things up another notch, and assume the geometry of the grid to be as shown in figure 3. Well, a lot has changed now. Since we no longer have a right-angle between x and y axis, we not longer have a right angled triangle, on which we can apply the Pythagorean theorem. So, what now? Moreover, how many metric scalars do you, now, need to know?

![Figure 4](/assets/images/B5P4.png) 

*Figure 4*: Completing the right-angled triangle.

Well, we can deal with the problem and make it compatible with a right angled triangle by completing the obtuse triangle to form a right angled triangle, as shown in figure 4. The main vector v is now being shown as the vector $$\overrightarrow{AC}$$, to better understand the components. The blue triangle shows a grid element cut diagonally, with the magnitude of $$\overrightarrow{AD}$$ being x and that of $$\overrightarrow{BC}$$ being y on the oblique grid system. The x-component of the main vector $$\overrightarrow{AC}$$, notated by X is given by:

$$
X=|AD|+|DB|=x+|CD|Cos\theta
$$
    

$$
X=|AD|+|DB|=x+yCos\theta
$$

and the y-component of the main vector $$\overrightarrow{AC}$$, notated by Y is given by:

$$
Y=|CD|Sin\theta = ySin\theta
$$

so, the overall magnitude is given by:

$$
|v|^2=|AB|^2=X^2+Y^2
$$


$$
|v|^2=(x+yCos\theta)^2+(ySin\theta)^2
$$

$$
|v|^2=x^2+y^2(Cos\theta)^2+2xyCos\theta+y^2(Sin\theta)^2
$$ 

$$
|v|^2=x^2+2xyCos\theta+y^2(Sin\theta^2+Cos\theta^2)
$$

$$
|v|^2=x^2+2xyCos\theta+y^2
$$

Rewriting elegantly, we get: 

$$
|v|^2=x^2+xyCos\theta+yxCos\theta+y^2
$$

This elegant form allows us to incorporate the metric elements nicely via: 

$$
|v|^2=g_{xx}x.x+g_{xy}x.y+g_{yx}y.x+g_{yy}y.y
$$

So, that's four scalars that we now need to know. The elements $$g_{xy}$$ and $$g_{yx}$$ absorb the Cos$$\theta$$ term and therefore now encode the "obtuseness" of the geometry involved. But wait, look at the way I have notated them. We can write this as a matrix! 

$$
g=
\begin{pmatrix}
g_{xx} & g_{xy} \\
g_{yx} & g_{yy}
\end{pmatrix}
$$

and THAT, my friends, is what we call a Rank-2 tensor. So now, we can calculate the magnitude by using elements taken from this tensor. Since this particular tensor encodes all the elements required for a coordinate transformation, we call it a metric tensor.

Notice that if you take the case $$\theta=90$$, $$g_{xy}$$ and $$g_{yx}$$ vanish, and so you retain the case of rectangle grid (if $$g_{xx} \neq g_{yy}$$) and square grid (if $$g_{xx} = g_{yy}$$). This makes perfect sense when you realize that the square and rectangle grids are right-angled grids, so that is a useful intuitive picture. 

This metric tensor can be further generalized to three dimensions: 



$$
g=\begin{pmatrix}
g_{xx} & g_{xy} & g_{xz} \\
g_{yx} & g_{yy} & g_{yz} \\
g_{zx} & g_{zy} & g_{zz}
\end{pmatrix}
$$


Now, let's devise a compact form where we can generalize to any number of dimensions, so extending the equation: 

$$
|v|^2=g_{xx}x.x+g_{xy}x.y+g_{yx}y.x+g_{yy}y.y
$$

to N dimensions, we can write: 

$$
 |v|^2 = \sum_{\mu,\nu}^N g_{\mu \nu}x^{\mu} x^{\nu}
$$

## The Final Form

Let's unpack this. First of all $$\mu$$ and $$\nu$$ are indices which we will sum over. The metric tensor is notated by $$g_{\mu \nu}$$. It's indices on the bottom because it is a covariant tensor, since the elements of the tensor covaries with the length of the grids. Since, as you increase the grid length of the Euclidean space, the element's value of the metric tensor increases. The opposite is true for x (or the displacement), and so its indices are at the top and so it's a contravariant quantity. The x, y and z coordinates are notated by $$x^1$$, $$x^2$$ and $$x^3$$ respectively, and can be extended to N dimensions. 

So, is this the most general form? Is this formula sufficient for converting any geometry into distance? 

![Figure 5](/assets/images/B5P5.png) 

*Figure 5*: A Chaotic Grid.

To answer that question, look at figure 5. What do you do now? The answer is that can take infinitely small displacements, and assume that over the length of the infinitesimal displacement, the grid-lines are straight. So a more generalized formula for displacement for any coordinate system arises: 

$$
 dv^2 = \sum_{\mu,\nu}^N g_{\mu \nu}dx^{\mu} dx^{\nu}
$$

Using the Einstein summation convention, we can get rid of the summation sign and obtain the most elegant form of this formula: 

$$
 dv^2 = g_{\mu \nu}dx^{\mu} dx^{\nu}
$$

So the metric tensor is a tensor whose individual element fit perfectly to the coordinates of any geometry, like a puzzle piece in a jigsaw, and elegantly output the distance. To call it a powerful tool would be an understatement. And in general, tensors are powerful tools. We will use more tensors in future blogs.

Now that the mystery surrounding the tensor and matrix tensor is cleared, let's dive into the cosmological aspect of this tensor. 

## A Formalism to Detect Curvature

We are now equipped to discuss curvature in space. Firstly, why should we bother? Can we not look at an object and know it's curvature. Not really, the human brain is pretty bad at deducing curvature. Let's look at the Earth as an example. How do we know that the surface of the Earth is curved? It's because we can not map it onto a 2D plane with a uniform metric. So most world maps lie to you. 

![Figure 6](/assets/images/B5P6.png) 

*Figure 6*: The World Map (adapted from Vecteezy). 

Here, it looks like Greenland is larger than Australia, but the truth is that it's area is only a small fraction of Australia's overall area. The reason why Greenland appears larger is because the non-uniform metric is more generous to Greenland than it is to Australia and exaggerates small distances, resulting in the unfair stretching of Greenland that we see on the World map. 
And this is  the methodology of determining curvature. If you can map a 3D surface onto a 2D plane, without warping the metric or the "grid-lines", the surface is flat. In that case, you would be intuitively correct to think that all 3D surfaces are curved, like which 3D surface does not distort the metric when mapped onto 2D. But don't jump to conclusions yet, or trust your intuition, and look no farther than the case of a cylinder. 
A cylinder can be laid out as a perfect rectangular, opened up 2D surface. Our intuition deceives us in most cases when it comes to dimensions, and completely fails when you try to think of more that 3 dimensions, but I'll tell you what is not deceived by the facade of curved space: MATHEMATICS. 

This is why this geometrical formalism is not a formality but a necessary tool for us to not get lost or lose our way. This is precisely the reason as to why general relativity is so popular and why Einstein is considered, arguably, the smartest person to ever live. He was able to determine a formalism where all other methods had failed. And it was not even his biggest achievement...heck, he was just getting started.

Einstein's ingenious insight was to combine space and time under one fabric, creatively named spacetime. To incorporate the time component, often referred to as the temporal component, we need to include one time dimension alongside 3 spatial dimensions. One can visualize spacetime by plotting an event onto a graph with space on the x-axis and time on the y-axis. 
    
The above simulation shows flat spacetime, since the path of light (blue) was not curved. Under the influence of gravity, this fabric is bent, so light and the object would experience a direction change due to gravity. This is why it's said that gravity is not fundamentally a force, but a ripple or warp of spacetime. This geometrical interpretation of gravity is at the heart of general relativity. 

The simulation only had one dimension of space, but in reality, there are three dimensions of space. Luckily for us, the earlier formula for distance can be applied to spacetime since it can be generalized to any amount of dimensions.

## Application to Cosmology

Earlier, we were trying to map a 3D object onto 2D, now it's 4D sapcetime that we are dealing with. The formalism remains the same but the complexity now goes up a notch. 

The mathematical procedure involves computing Kristoffel symbols, Riemaan Tensors, Ricci Tensors and Ricci Scalar (R), with a non-zero Ricci scalar resulting in flat spacetime and the opposite is true if $$R \neq 0$$.

To learn more about the procedure, visit my github repository where I have everything coded out in Mathematica. And maybe, we will dive into the details in a future blog if need be. 

But for now, let's pause and look back at the journey we embarked on. Using grade 7 mathematics, we were able to devise a formalism that equips us to not only determine the distance for any geometrical coordinates nature can thrown at us, nut to also use that formalism to dive deep into cosmology and understand our universe from it's core.

Good job on making it this far, and as always, keep on physicsing.

