---

title: "Blog 11—Walking through the Birth of Electromagnetism from Gauge Theory: Part 4"
date: 2025-12-31
categories: [Particle Physics, Electromagnetism, Gauge Theory, Atomic and Molecular Physics, Fundamental Forces]
use_math: true
layout: single
author_profile: true
read_time: true
comments: true
excerpt: "We now delve into the mathematics of local U(1) symmetry and uncover how a Dirac field must be modified for its physics to remain invariant under this transformation."


---

## Introduction

In the last blog, symmetry spoke, and out of pure mathematics, the electric and magnetic fields emerged. What began as a desperate attempt to fix our “broken” Dirac equation turned into one of the most profound revelations in modern physics: that interaction itself is a consequence of demanding local gauge invariance.

In this post, we will take that revelation seriously. We’ll strip away every equation you’ve ever memorized about electromagnetism, be it Coulomb’s law, Faraday’s law or Maxwell’s equations, and rebuild them from the ground up using only symmetry, tensors, and logic.

By the end, you won’t just see electromagnetism as a force but as an inevitable outcome of nature’s obsession with local gauge symmetry.

## The Euler-Lagrange Equation

We briefly discussed the Euler-Lagrangian equation two blogs ago, and now we will leverage it. For more information on how it emerges from $$\textbf{Principle of Least Action}$$, look up the first chapter in Goldstein's book "Introduction to Classical Mechanics". In a nutshell, nature selects the path of least effort to make its components achieve stability, and the Euler-Lagrange equations are a manifestation of that rule.

$$
\frac{\partial \mathcal{L}}{\partial A_{\nu}}=\partial_{\mu}\big(\frac{\partial\mathcal{L}}{\partial(\partial_{\mu}{A_{\nu}})}\big)
$$

To make the magic happen, all we need is the Euler-Lagrange equation and the Lagrangian and luckily for us, we have both of them. 

$$
\mathcal{L}_{QED}=\bar{\psi}(i\hbar \gamma^i \partial_i - mc^2)\psi - g\bar\psi\gamma^i A_{i}\psi-\frac{1}{16\pi}F_{ij}F^{ij}
$$

So let's first evaluate the left hand side of the Euler-Lagrange equation. The first and third terms are independent with respect to change in $$A_{\mu}$$, so that leaves behind:

$$
\frac{\partial \mathcal{L}}{\partial A_{\nu}}= - g\bar\psi\gamma^i\psi\frac{\partial A_i}{\partial A_{\nu}}
$$

Now there's a subtlety. The derivative terms $$\frac{\partial A_i}{\partial A_{\nu}}$$ can only be 1 or 0, since if $$A_{\nu}$$ and $$A_{i}$$ are the same fields, then a derivative by itself yields one, otherwise it yields a zero since two fields are independent of each other. So this is a Kronecker delta term:

$$
 \frac{\partial A_i}{\partial A_{\nu}}=\delta_{i\nu}
$$ 

 So the LHS of the Euler-Lagrange equation can be generalized to:

$$
\frac{\partial \mathcal{L}}{\partial A_{\nu}}= - g\bar\psi\gamma^i\delta_{i\nu}\psi= - g\bar\psi\gamma^{\nu}\psi=-\frac{j^{\nu}}{c}
$$

This equation leverages tensorial calculus which is pretty advanced stuff but all you need to know is that with this step, we have removed all the redundant, zero-yielding terms. The final step just leverages the dimension-corrected probability 4-current, which is the first time in the series we have deviated from natural units, with the reason being that c cannot be left out if we wish to re-derive all of EMT from first principles.

Now let's derive the RHS of the Euler-Lagrange equation. Now, the first and second terms of $$\mathcal{L}$$ cancel out, but the term involving the Faraday tensor does not, because its fundamental structure aligns with the nature of the equation involved
$$
\partial_{\mu}\big(\frac{\partial\mathcal{L}}{\partial(\partial_{\mu}{A_{\nu}})}\big)=-\frac{1}{16\pi}\partial_{\mu}\big(\frac{\partial F_{ij}F^{ij}}{\partial(\partial_{\mu}{A_{\nu}})}\big)
$$

Now we can equate the RHS with the LHS of the Euler-Lagrange equation to give:

$$
-\frac{1}{16\pi}\partial_{\mu}\big(\frac{\partial F_{ij}F^{ij}}{\partial(\partial_{\mu}{A_{\nu}})}\big)=-\frac{j^{\nu}}{c}
$$

Multiplying through with $$-16\pi$$ and using the product rule:

$$
\partial_{\mu}\big(\frac{\partial F^{ij}}{\partial(\partial_{\mu}{A_{\nu}})}F_{ij}+\frac{\partial F_{ij}}{\partial(\partial_{\mu}{A_{\nu}})}F^{ij}\big)=16\pi\frac{j^{\nu}}{c}
$$

The two terms on the LHS are equal so:

$$
2\partial_{\mu}\big(\frac{\partial F_{ij}}{\partial(\partial_{\mu}{A_{\nu}})}F^{ij}\big)=16\pi\frac{j^{\nu}}{c}
$$

which can be simplified to:

$$
\partial_{\mu}\big(\frac{\partial (\partial_{i}A_j-\partial_jA_i)}{\partial(\partial_{\mu}{A_{\nu}})}\big)F^{ij}=8\pi\frac{j^{\nu}}{c}
$$

$$
\partial_{\mu}\big(\frac{\partial (\partial_{i}A_j)}{\partial(\partial_{\mu}{A_{\nu}})}\big)F^{ij}-\partial_{\mu}\big(\frac{\partial (\partial_{j}A_i)}{\partial(\partial_{\mu}{A_{\nu}})}\big)F^{ij}=8\pi\frac{j^{\nu}}{c}
$$

so using the same Kronecker delta interpretation and using the same tensorial calculus rule gives us:

$$
\partial_{\mu}(\delta_{i\mu}\delta_{j\nu}\big)F^{ij}-\partial_{\mu}(\delta_{j\nu}\delta_{i\mu}\big)F^{ij}=8\pi\frac{j^{\nu}}{c}
$$

$$
\partial_{\mu}(\delta_{i\mu}\big)F^{i\nu}-\partial_{\mu}(\delta_{j\nu}\big)F^{\nu j}=8\pi\frac{j^{\nu}}{c}
$$

$$
\partial_{\mu}F^{\mu\nu}-\partial_{\mu}F^{\nu \mu}=8\pi\frac{j^{\nu}}{c}
$$

Note that, just like earlier, all I did was generalize the term which naturally removes all the null results. In simpler terms, the only remaining terms are when the derivatives of different gauge fields do not yield zero.

Let's remind ourselves that $$F^{\mu\nu}=-F^{\nu\mu}$$ and so we get:
    
$$
\partial_{\mu}F^{\mu\nu}+\partial_{\mu}F^{\mu \nu}=8\pi\frac{j^{\nu}}{c}
$$

$$
\partial_{\mu}F^{\mu \nu}=4\pi\frac{j^{\nu}}{c}
$$

This looks like an elegant equation. Let's dive deeper and analyze the $$\nu=0$$ case. Expanding using the Einstein summation convention, we get:

$$
\partial_{\mu}F^{\mu 0}=\partial_{0}F^{0 0}+\partial_{1}F^{1 0}+\partial_{2}F^{2 0}+\partial_{3}F^{3 0}=4\pi\frac{j^{0}}{c}
$$

Recall that:

$$
F^{\mu\nu} =
\begin{pmatrix}
0 & -E_x & -E_y & -E_z \\
E_x & 0 & -B_z & B_y \\
E_y & B_z & 0 & -B_x \\
E_z & -B_y & B_x & 0
\end{pmatrix}, \quad\partial_{\mu}=[\frac{1}{c}\frac{\partial}{\partial t}, \frac{\partial}{\partial x},\frac{\partial}{\partial y},\frac{\partial}{\partial z}]
$$

So after some replacing and plucking, we find:

$$
\frac{\partial E_x}{\partial x}+\frac{\partial E_y}{\partial y}+\frac{\partial E_z}{\partial z}=\frac{4\pi}{c}\rho c=4\pi \rho
$$

which, when written compactly, gives:

$$
\nabla.\vec{E}=4\pi\rho
$$

and would you look at that. Gauss' law lies ahead of you as a natural emergence of an underlying mechanism and not as a first principle. It is all starting to come together...

## The Spatial Components: $$\nu = 1, 2, 3$$

Now let's analyze the spatial components i.e. $$\nu = 1, 2, 3$$. Recall our general expression:

$$
\partial_{\mu} F^{\mu\nu} = 4\pi \frac{j^{\nu}}{c}
$$

Let’s begin with $$\nu = 1$$ (the x-component):

$$
\partial_{\mu} F^{\mu 1} = \partial_0 F^{0 1} + \partial_2 F^{2 1} + \partial_3 F^{3 1} = 4\pi \frac{j^1}{c}
$$

Substituting the elements of the Faraday tensor, we get:

$$
\frac{1}{c}\frac{\partial E_x}{\partial t} - \frac{\partial B_z}{\partial y} + \frac{\partial B_y}{\partial z} = \frac{4\pi}{c} j_x
$$

Multiplying through by c:

$$
\frac{\partial E_x}{\partial t} = c\bigg(\frac{\partial B_z}{\partial y} - \frac{\partial B_y}{\partial z}\bigg) - 4\pi j_x
$$

Similarly, for $$\nu = 2$$ (the y-component):

$$
\partial_{\mu} F^{\mu 2} = \partial_0 F^{0 2} + \partial_1 F^{1 2} + \partial_3 F^{3 2} = 4\pi \frac{j^2}{c}
$$

Substitute the tensor components:

$$
\frac{1}{c}\frac{\partial E_y}{\partial t} - \frac{\partial B_x}{\partial z} + \frac{\partial B_z}{\partial x} = \frac{4\pi}{c} j_y
$$

Multiplying through by c gives:

$$
\frac{\partial E_y}{\partial t} = c\bigg(\frac{\partial B_x}{\partial z} - \frac{\partial B_z}{\partial x}\bigg) - 4\pi j_y
$$

And finally, for $$\nu = 3$$ (the z-component):

$$
\partial_{\mu} F^{\mu 3} = \partial_0 F^{0 3} + \partial_1 F^{1 3} + \partial_2 F^{2 3} = 4\pi \frac{j^3}{c}
$$

Substituting $$F^{\mu\nu}$$ values:

$$
\frac{1}{c}\frac{\partial E_z}{\partial t} - \frac{\partial B_y}{\partial x} + \frac{\partial B_x}{\partial y} = \frac{4\pi}{c} j_z
$$

Multiply by c:

$$
\frac{\partial E_z}{\partial t} = c\bigg(\frac{\partial B_y}{\partial x} - \frac{\partial B_x}{\partial y}\bigg) - 4\pi j_z
$$

### Compact Vector Form

Combining all three spatial components, we can write:

$$
\frac{\partial \vec{E}}{\partial t} = c(\nabla \times \vec{B}) - 4\pi \vec{j}
$$

or rearranged:

$$
\nabla \times \vec{B} - \frac{1}{c}\frac{\partial \vec{E}}{\partial t} = \frac{4\pi}{c} \vec{j}
$$

And there you have it. Ampère’s law with Maxwell’s correction emerged cleanly from the Euler–Lagrange equation.

We’ve now derived two of Maxwell’s equations, Gauss’s law and the corrected Ampère’s law purely from the gauge  invariant Lagrangian. Are you starting to believe?

## From Lagrangian to Force

If you still do not believe, and need more proof, there's more of just that.
We derived how the field $$A_\mu$$ must exist and how it carries dynamics. Now for the payoff, let's see how a charged particle actually feels this field?

Take the minimal-coupling Lagrangian for a non-relativistic particle of mass m and charge q:

$$
L(\mathbf{x},\dot{\mathbf{x}},t)=\tfrac{1}{2}m\dot{\mathbf{x}}^2 + q\dot{\mathbf{x}}\!\cdot\!\mathbf{A}(\mathbf{x},t) - q\Phi(\mathbf{x},t),
$$

where $$\Phi$$ is the scalar potential and A is the vector potential.
Let's apply the Euler–Lagrange equation for an arbitrary coordinate $$x_k$$:

$$
\frac{d}{dt}\!\left(\frac{\partial L}{\partial \dot{x}_k}\right)-\frac{\partial L}{\partial x_k}=0.
$$

Computing the LHS, we see the third term does not contain $$\dot{x}$$, so we are left with:

$$
\frac{\partial L}{\partial \dot{x}_k}=m\dot{x}_k + qA_k(\mathbf{x},t).
$$

Taking the derivative with respect to time gives us the LHS:

$$
\frac{d}{dt}\!\left(\frac{\partial L}{\partial \dot{x}_k}\right)
= m\ddot{x}_k + q\Big(\frac{dA_k}{dt}\Big)
= m\ddot{x}_k + q\Big(\partial_t A_k + (\dot{\mathbf{x}}\!\cdot\!\nabla)A_k\Big).
$$

Now for the RHS of the Euler-Lagrange equation, only the first term is not dependent on x, $$\Phi$$ and A are dependent and so:

$$
\frac{\partial L}{\partial x_k}
= q\,\dot{x}_i\frac{\partial A_i}{\partial x_k} - q\frac{\partial \Phi}{\partial x_k}.
$$

(Indices summed; $$partial_{x_k}A_i=\partial_k A_i$$.)


Entering all the terms into the Euler-Lagrange equation:

$$
m\ddot{x}_k + q\big(\partial_t A_k + (\dot{\mathbf{x}}\!\cdot\!\nabla)A_k\big)
- \Big(q\,\dot{x}_i\partial_k A_i - q\partial_k\Phi\Big) = 0.
$$

Rearranging for the acceleration:

$$
m\ddot{x}_k
= q\Big(-\partial_k\Phi - \partial_t A_k \Big)
+ q\Big(\dot{x}_i\partial_k A_i - (\dot{\mathbf{x}}\!\cdot\!\nabla)A_k\Big).
$$

Now use the vector identity (component form)

$$
(\dot{\mathbf{x}}\times\mathbf{B})_k
= \dot{x}_i(\partial_k A_i - \partial_i A_k).
$$

Hence

$$
\dot{x}_i\partial_k A_i - (\dot{\mathbf{x}}\!\cdot\!\nabla)A_k
= (\dot{\mathbf{x}}\times\mathbf{B})_k.
$$

Replace the bracketed terms with the fields. Recall the electric field in potentials:

$$
\mathbf{E} = -\nabla\Phi - \partial_t \mathbf{A}, \qquad \mathbf{B}=\nabla\times\mathbf{A}.
$$

Thus the component equation becomes:

$$
m\ddot{x}_k = q\big(E_k + (\dot{\mathbf{x}}\times\mathbf{B})_k\big).
$$

In compact vector form:
$$
m\mathbf{a} = q\big(\mathbf{E} + \dot{\mathbf{x}}\times\mathbf{B}\big).
$$

That, my friends, is the Lorentz force law and it, too, drops out naturally from the minimal-coupling Lagrangian. By now this is easily the final nail in the coffin. We have sealed the deal here. 

## The Conservation of Charge

We can stop here but I want to highlight one more powerful thing which you will not find very readily in EMT since it is usually treated as a given and that is the conservation of charge. But here, we treat nothing as given! And besides, it will prove our theory to be consistent, though we already know it is, but it is satisfying to see that math automatically shows it, in its own majestic language.
 
Recall that:

$$
\partial_{\mu} F^{\mu\nu} = 4\pi \frac{j^{\nu}}{c}
$$

Rearranging for probability 4-current gives us:

$$
\frac{c}{4\pi}\partial_{\mu} F^{\mu\nu} = j^{\nu}
$$

Charge itself would be conserved if the derivative of probability current is zero, since that would imply that the current cannot leak out of a region of space, and that the net charge of the universe is a conserved quantity and must be created and destroyed by equal amounts. To get a better idea of this, read through the continuity equation sections in blog 1. So anyway, to prove it mathematically, we require that:  

$$
\partial_\nu j^\nu=0
$$

and therefore,

$$
\partial_\nu\big(\frac{c}{4\pi}\partial_{\mu} F^{\mu\nu}\big)=0
$$

$$
\frac{c}{4\pi}\partial_\nu\big(\partial_{\mu} F^{\mu\nu}\big)=0
$$

$$
\partial_\nu\partial_{\mu} F^{\mu\nu}=0
$$
These are actually 16 terms when you expand using the Einstein summation convention.


Expanding the indices explicitly:

$$
 \partial_\nu \partial_\mu F^{\mu\nu}
= 
\partial_0 \partial_\mu F^{\mu 0} +
\partial_1 \partial_\mu F^{\mu 1} +
\partial_2 \partial_\mu F^{\mu 2} +
\partial_3 \partial_\mu F^{\mu 3}
$$

or, written out completely:

$$
\begin{aligned}
\partial_\nu(\partial_{\mu} F^{\mu\nu})
&= \partial_0(\partial_1 F^{10} + \partial_2 F^{20} + \partial_3 F^{30}) \\
&\quad + \partial_1(\partial_0 F^{01} + \partial_2 F^{21} + \partial_3 F^{31}) \\
&\quad + \partial_2(\partial_0 F^{02} + \partial_1 F^{12} + \partial_3 F^{32}) \\
&\quad + \partial_3(\partial_0 F^{03} + \partial_1 F^{13} + \partial_2 F^{23})
\end{aligned}
$$

Since $$F^{\mu\nu} = -F^{\nu\mu} $$, each non-diagonal term like

$$
\partial_\nu \partial_\mu F^{\mu\nu}
$$

appears with its negative counterpart

$$
\partial_\mu \partial_\nu F^{\nu\mu}
$$

Because partial derivatives commute:

$$
\partial_\mu \partial_\nu = \partial_\nu \partial_\mu
$$

the antisymmetry ensures cancellation of the 12 terms non-diagonal terms, as all 6 unique terms are countered by their antisymmetric counterparts:


    
$$
\partial_\nu \partial_\mu F^{\mu\nu} = - \partial_\mu \partial_\nu F^{\nu\mu}
\Rightarrow 
\partial_\nu(\partial_{\mu} F^{\mu\nu}) = 0, \quad \mu \neq \nu
$$

As for the diagonal terms, $$\mu=\nu$$, they are zero anyway. So there go the four remaining terms and what's left after it all? A big fat ZERO.

$$
 \partial_\nu J^\nu = 0.
$$

This is the final blow, the coup de grâce. Because not only have we destroyed EMT by conquering it and placing it under the flag of particle physics and reminding of its founding principles, but we have gone one step further by proving that the charge is conserved. This is something EMT could never manage on its own since it does not go to the depths we went to. And hey, we came out of those depths alive and wiser, and so we can and will keep on physicsing. 
