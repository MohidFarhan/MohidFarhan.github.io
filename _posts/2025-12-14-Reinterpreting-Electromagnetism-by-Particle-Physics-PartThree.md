---

title: "Blog 10—Walking through the Birth of Electromagnetism from Gauge Theory: Part 3"
date: 2025-12-14
categories: [Particle Physics, Electromagnetism, Gauge Theory, Atomic and Molecular Physics, Fundamental Forces]
use_math: true
layout: single
author_profile: true
read_time: true
comments: true
excerpt: "We now delve into the mathematics of local U(1) symmetry and uncover how a Dirac field must be modified for its physics to remain invariant under this transformation."


---

## Introduction
Last time, we broke physics boldly, unapologetically, and with style. We added a term to the sacred Dirac Lagrangian, a move so blasphemous that even Feynman would have raised an eyebrow. But today, redemption begins.

In this follow-up post, we’ll see that our so-called “sin” wasn’t a mistake at all but a discovery in disguise. By demanding local gauge invariance, we’ll be forced to introduce a brand new field, one that nature herself uses to communicate electromagnetic forces.

Get ready as this is where symmetry creates interaction.


### What have we done?
We introduced a term to the Dirac Lagrangian and attained what we called the "Dream Lagrangian".

$$
\mathcal{L}_d = \mathcal{L}_D + \bar\psi\gamma^\mu (\partial_\mu\alpha(x))\psi
$$

where $$\mathcal{L}_d$$ and $$\mathcal{L}_D$$ notate the dream and Dirac Lagrangian respectively.


Let's see what we can change, rearrange or simply just reinterpret. First of all, we can pull out the derivative of $$\alpha(x)$$.

$$
\mathcal{L}_d = \mathcal{L}_D + \partial_\mu\alpha(x)\bar\psi\gamma^\mu \psi
$$

Now $$\alpha(x)$$ is , physically, a non uniform gauge field that changes with time. So it would not be unreasonable to reinterpret this as a gauge field in itself, and the $$\bar\psi\gamma^\mu \psi$$ looks like some quantity that, since there is invariance, must be conserved under the Noether's theorem. 


And looking at the term as a whole:

$$
\partial_\mu\alpha(x)\bar\psi\gamma^\mu \psi,
$$

It looks suspiciously like an interaction term of something coupling the Dirac field $$\psi$$ with another entity that changes across spacetime.  

So instead of feeling guilty, let's lean into the heresy. Let’s assume there really $$\textbf{is}$$ such a field, call it $$A_\mu$$, and absorb our mysterious derivative into it:

$$
\partial_\mu\alpha(x) \quad \longrightarrow \quad gA_\mu.
$$

The constant g is simply a coupling factor that tells us how strongly $$\psi$$ interacts with this new field.  

With this change, the Lagrangian becomes:

$$
\mathcal{L} = \bar{\psi}(i\gamma^\mu\partial_\mu - m)\psi + g\bar{\psi}\gamma^\mu A_\mu\psi
$$



## Not an Ad-Hoc Solution?

Let’s first look closely at what it multiplies:

$$
\bar{\psi}\gamma^\mu \psi
$$

This combination is special as the mathematics is now starting to whisper. It’s not just any term, it represents the flow of charge in spacetime, known as the $$\textbf{Dirac current}$$:

$$
j^\mu = \bar{\psi}\gamma^\mu \psi
$$

This current is the suspected naturally conserved property through Noether’s theorem, a direct consequence of global gauge invariance:

$$
\partial_\mu j^\mu = 0
$$

The probability current analogy makes special sense when you look at the conserved quantities of the Schrodinger and Klein-Gordon equation in the very first blog. 
    
So our “extra” term can now be rewritten as:

$$
\partial_\mu\alpha(x)\bar{\psi}\gamma^\mu \psi = gA_{\mu}j^\mu
$$

At this point, the mathematics is screaming something insanely profound. It’s telling us that the Dirac field is trying to $$\textbf{talk}$$ to gauge field $$A_{\mu}$$ through its current $$j^{\mu}$$, with a coupling constant g.

Now to give the interaction some legs, we have to introduce a few things.

To truly respect local gauge invariance, the derivative $$\partial_\mu$$ must now evolve.  
It can no longer act alone because $$\psi$$ carries charge and the phase $$\alpha(x)$$ depends on spacetime.  

So we introduce a new operator, the $$\textbf{covariant derivative}$$:

$$
D_\mu = \partial_\mu + igA_\mu
$$

This new derivative “absorbs” the unwanted phase term, restoring perfect local gauge invariance.  
When we rewrite our Lagrangian with $$D_\mu$$, we obtain:

$$
\mathcal{L} = \bar{\psi}\left(i\gamma^\mu D_\mu - m\right)\psi
$$


which expands to:

$$
\mathcal{L} = \bar{\psi}(i\gamma^\mu \partial_\mu - m)\psi + g\bar{\psi}\gamma^\mu A_\mu\psi
$$

Now, the interaction term is far from something we added out of desparation, and looks more like a stroke of genius.  

But we’re not done yet. The rule for the Dirac field was:

$$
\psi \rightarrow e^{i\alpha(x)}\psi
$$

But there is another transformation that is the consequence of the transformations that we have seen so far. For the Lagrangian to stay invariant, the new derivative:

$$
D_\mu = \partial_\mu + igA_\mu
$$

must transform in the same way as the aforementioned rule:

$$
D_\mu\psi \rightarrow e^{i\alpha(x)}D_\mu\psi
$$

Let’s see what this demand does to $$A_\mu$$.

## Deriving the Transformation Law

Starting with:

$$
D_\mu \psi = (\partial_\mu + igA_\mu)\psi
$$

We applied the transformation in the previous blog and retained:

$$
\psi \rightarrow e^{i\alpha(x)}\psi, \qquad
\partial_\mu\psi \rightarrow e^{i\alpha(x)}(\partial_\mu\psi + i(\partial_\mu\alpha)\psi)
$$

Applying the same set of rules onto the covariant derivative:

$$
D_\mu\psi \rightarrow e^{i\alpha(x)}\left[\partial_\mu + i(\partial_\mu\alpha) + igA_\mu\right]\psi
$$

For this to equal $$e^{i\alpha(x)}(\partial_{\mu} + igA'_{\mu})\psi$$, we must have:

$$
A'_\mu = A_\mu - \frac{1}{g}\partial_\mu\alpha(x)
$$ 

So that:

$$
D_\mu\psi \rightarrow e^{i\alpha(x)}\left[\partial_\mu + i(\partial_\mu\alpha(x)) + ig( A_\mu - \frac{1}{g}\partial_\mu\alpha(x))\right]\psi
$$

$$
D_\mu\psi \rightarrow e^{i\alpha(x)}\left[\partial_\mu + i(\partial_\mu\alpha(x)) + ig A_\mu - ig\frac{1}{g}\partial_\mu\alpha(x)\right]\psi
$$   

$$
D_\mu\psi \rightarrow e^{i\alpha(x)}\left[\partial_\mu + i(\partial_\mu\alpha(x)) + ig A_\mu - i\partial_\mu\alpha(x)\right]\psi
$$   

$$
D_\mu\psi \rightarrow e^{i\alpha(x)}\left[\partial_\mu +  ig A_\mu \right]\psi
$$   

So none of the transformations were pulled out of nowhere, but were intentional attempts to restore the form of the equation to our liking. This is perfectly allowed in physics. The latest of these transformations is:

$$
A'_\mu = A_\mu - \frac{1}{g}\partial_\mu\alpha(x)
$$ 

And this reveals something very interesting.


## The Subtlety with Gauge Field

Now, the implications of this transformation far outweigh all the others, since $$D_{\mu}$$ is simply a mathematical object, whereas $$A_{\mu}$$ is a literal 4-potential we have just invented. An implication of inventing this field should be its ability to exist on it's own, or the possibility to couple to itself. After all, we can not just bring a field into existence just for the sake of solving our problem. We need to study field in its totality and it should somehow energetically manifest itself. So first of all, let's try to have it couple to itself and once again, whether that is allowed or not depends on whether the same gauge transformation allows for invariance. So let's invent a term that looks like:

$$gA^{\mu}A_{\mu}$$

Applying the transformation:

$$
A'_\mu = A_\mu - \frac{1}{g}\partial_\mu\alpha(x)
$$ 

We can see that:

$$
g\big(A^\mu - \frac{1}{g}\partial^\mu\alpha(x)\big)\big( A_\mu - \frac{1}{g}\partial_\mu\alpha(x)\big) \neq gA^{\mu}A_{\mu}
$$ 

So the field can not couple to itself, under the transformation. So how can we get $$A_{\mu}$$ to manifest energetically, and on it's own? We need a transformation that, when applied, respects local gauge invariance. Luckily for us, there is a way. There seems to be no transformation that involves $$\partial_{\mu}$$ and retains invariance under the $$A_{\mu}$$ transform, but there is a hack.


## The Miracle Transformation
The proposed term that works is:

$$
\partial_{\mu}A_{\nu}-\partial_{\nu}A_{\mu}
$$

Since, under the transformation, we:

$$
=\partial_{\mu}(A_\nu - \frac{1}{g}\partial_\nu\alpha(x))-\partial_{\nu}(A_\mu - \frac{1}{g}\partial_\mu\alpha(x))
$$

$$
=\partial_{\mu}A_\nu - \partial_{\nu}A_\mu-\frac{1}{g}\partial_\mu\partial_\nu\alpha(x) + \frac{1}{g}\partial_\nu\partial_\mu\alpha(x)
$$

$$
=\partial_{\mu}A_{\nu}-\partial_{\nu}A_{\mu}
$$

We just exploited the fact that all the partial derivatives applied on $$A_{\mu}$$ cause a variance of similar magnitude and so if we subtract any two terms, the variance cancels out. Smart, isn't it? So you have a trick which makes the Lagrangian of our system oblivious to a local phase change, and this term gives us all the ways in which $$A_{\mu}$$ can mess around, and it be allowed by nature since the physics remains unchanged. So let's dig deeper into the implications of this.


## The Allowed Degrees of Freedom

In physics, we call these "ways of allowed messing around" as degrees of freedom. And as we have seen in the general relativity posts earlier, there are 4 universal degrees of freedom, 3 in space and one in time. They map one-to-one onto the 4 gamma matrices with the index being 0 for time and 1,2,3 for space. So let's exploit those. 

The space-time combinations are:

$$
\partial_{0}A_{1}-\partial_{1}A_{0}, \quad \partial_{0}A_{2}-\partial_{2}A_{0},\quad 
\partial_{0}A_{3}-\partial_{3}A_{0}
$$

The space-space combinations are:

$$
\partial_{1}A_{2}-\partial_{2}A_{1}, \quad \partial_{1}A_{3}-\partial_{3}A_{1},\quad 
\partial_{2}A_{3}-\partial_{3}A_{2}
$$

So there are 6 routes that lead to invariance while allowing $$A_{\mu}$$ to manifest energetically.


### The Manifestation: A return to non-natural units

Let's first define the 4-potential as:

$$
A^{\mu}=[V,A]
$$

$$
A_{\mu}=[V,-A]
$$

And we return back to non-natural units because that is important for a while. So the 3 space-time combinations yield results as follows:

$$
\partial_{0}A_{1}-\partial_{1}A_{0}=-\frac{1}{c}\frac{\partial A_{x}}{\partial t}-\frac{\partial V}{\partial x}
$$

$$
\partial_{0}A_{2}-\partial_{2}A_{0}=-\frac{1}{c}\frac{\partial A_{y}}{\partial t}-\frac{\partial V}{\partial y}
$$

$$
\partial_{0}A_{3}-\partial_{3}A_{0}= -\frac{1}{c}\frac{\partial A_{z}}{\partial t}-\frac{\partial V}{\partial z}
$$




Let's also look at the space-space combinations:

$$
\partial_{1}A_{2}-\partial_{2}A_{1}=\frac{\partial A_{y}}{\partial x}-\frac{\partial A_x}{\partial y}
$$

$$
\partial_{1}A_{3}-\partial_{3}A_{1}=\frac{\partial A_{z}}{\partial x}-\frac{\partial A_x}{\partial z}
$$

$$
\partial_{2}A_{3}-\partial_{3}A_{2}=\frac{\partial A_{z}}{\partial y}-\frac{\partial A_y}{\partial z}
$$

The trained eyes might be start to lit-up now. Anyone who has studied an electromagnetic theory course will now smell the blood in the water because the formulas that we have attained from space-time combination match the components of the electric field and those of the space-space components, match the expressions for the magnetic field.  

We are no longer justifying sins, but we are now looking at the electric and magnetic fields naturally manifesting from the allowed degrees of freedom determined by the local gauge transformation. When I saw this for the first time, my mind was BLOWN. 
 

We have just found out that the electromagnetic formulas are not first principles, and given their richness, this is nothing short of absolutely insane. The electric and magnetic fields are simply manifestations of the strict compliance of local gauge symmetry, so symmetry is fundamental, everything else is just consequences. Now, after studying the concept of the Faraday tensor, we can derive all of electromagnetism from scratch. Also note that earlier, we saw that the gauge field does not couple to itself, which predicts that photons do not interact with each other, which is consistent with observation.


## The Faraday Tensor

We will enjoy the fruits of all this work shortly, as we will construct electromagnetism from scratch. But for that, we need to derive the Faraday tensor. Tensors have bullied most of us from the beginning, but are not completely new to us, since we dived into the metric tensor in blog 5. The best way to understand this is to make a table, where we will now use the compact form:

$$
F_{\mu\nu}=\partial_{\mu}A_{\nu}-\partial_{\nu}A_{\mu}
$$

$$
F^{\mu\nu} =
\begin{pmatrix}
F_{00} & F_{01} & F_{02} & F_{03} \\
F_{10} & F_{11} & F_{12} & F_{13} \\
F_{20} & F_{21} & F_{22} & F_{23} \\
F_{30} & F_{31} & F_{32} & F_{33}
\end{pmatrix}
$$

Notice that all diagonal terms are zero since:

$$
F_{ii}=\partial_i\partial_i-\partial_i\partial_i=0
$$





Another property of note is that: 

$$
F_{\mu\nu}=-F_{\nu\mu}
$$

which means that the diagonal (all composed of zero) also acts as a sort of mirror, and on the other side of the diagonal are terms of equal quantity but with an inverted sign. The funny bit is that we have already derived the 6 unique entries earlier, we just have to identify them, like so:

$$
F_{01}=\partial_{0}A_{1}-\partial_{1}A_{0}=\frac{1}{c}\frac{\partial A_{x}}{\partial t}-\frac{\partial V}{\partial x}=E_x
$$

$$
F_{02}=\partial_{0}A_{2}-\partial_{2}A_{0}=\frac{1}{c}\frac{\partial A_{y}}{\partial t}-\frac{\partial V}{\partial y}=E_y
$$

$$
F_{03}=\partial_{0}A_{3}-\partial_{3}A_{0}=\frac{1}{c}\frac{\partial A_{z}}{\partial t}-\frac{\partial V}{\partial z}=E_z
$$

$$
F_{12}=\partial_{1}A_{2}-\partial_{2}A_{1}=\frac{\partial A_{y}}{\partial x}-\frac{\partial A_x}{\partial y}=B_Z
$$

$$
F_{13}=\partial_{1}A_{3}-\partial_{3}A_{1}=\frac{\partial A_{z}}{\partial x}-\frac{\partial A_x}{\partial z}=-B_y
$$

$$
F_{23}=\partial_{2}A_{3}-\partial_{3}A_{2}=\frac{\partial A_{z}}{\partial y}-\frac{\partial A_y}{\partial z}=B_x
$$

### The Final Form of the Faraday Tensor

Since we know the 6 unique entries now, we can just put all diagonal values as zero and use the diagonal reflection rule to create the entire tensor
$$
F_{\mu\nu} =
\begin{pmatrix}
0 & E_x & E_y & E_z \\
-E_x & 0 & B_z & -B_y \\
-E_y & -B_z & 0 & B_x \\
-E_z & B_y & -B_x & 0
\end{pmatrix}
$$ 

This tensor is simply a mathematical representation of the 6 degrees of freedom that we saw earlier. We have identified this as the source of $$A_{\mu}$$ manifesting energetically, it deserves its place in the Lagrangian.

Writing the contravariant counterpart of this tensor:

$$
F^{\mu\nu} =
\begin{pmatrix}
0 & -E_x & -E_y & -E_z \\
E_x & 0 & -B_z & B_y \\
E_y & B_z & 0 & -B_x \\
E_z & -B_y & B_x & 0
\end{pmatrix}
$$


## The QED Lagrangian

The magnitude squared of the Faraday tensor is given by the term:

$$
F_{\mu\nu}F^{\mu\nu}
$$

which shows up as a term in the QED Lagrangian which shows the kinetic contribution of the photon field. Since, we did not assign a magnitude to our units, we can apply any factor to this term since units are arbitrary. The most common form of this term is written as:

$$
-\frac{1}{16\pi}F_{\mu\nu}F^{\mu\nu}
$$

The minus sign here is there to distinguish time from space. So, the Lagrangian for Quantum Electro-Dynamics, is the "dream" Lagrangian and this term, so we get:

$$
\mathcal{L}_{QED}=\bar{\psi}(i\gamma^\mu \partial_\mu - m)\psi + \bar\psi\gamma^\mu A_{\mu}\psi-\frac{1}{16\pi}F_{\mu\nu}F^{\mu\nu}
$$

There might still be some ambiguity regarding the Faraday tensor term, and they will be addressed in the next blog series, where we will see why this form is convenient when we try to reproduce electromagnetism from gauge theory. And until then, keep on physicsing.


