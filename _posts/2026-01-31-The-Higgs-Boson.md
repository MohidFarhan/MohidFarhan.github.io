---

title: "Blog 12—The Duel Between Particle Physics and Quantum Field Theory (Part 1)"
date: 2026-01-31
categories: [Particle Physics, Electromagnetism, Quantum Mechanics, Quantum Field Theory, Fundamental Forces]
use_math: true
layout: single
author_profile: true
read_time: true
comments: true
excerpt: "Physics is the art of settling down, and even fields want to find a stable 'couch' to rest on. But what happens when we nudge a field out of its comfort zone?"


---

## Introduction
Think of a wrestling match. In one corner, you have Particle Physics, the intuitive champion. It describes electrons and quarks as tiny, discrete things, like microscopic balls colliding and interacting in space. It’s how we often visualize the subatomic world.

In the other corner stands Quantum Field Theory (QFT), the reigning champion of modern theory. It says particles aren’t really “things” at all. Instead, they are ripples in invisible, universe-wide fields. "An electron is just a localized vibration in an electric field", it says.

Both frameworks predict the same experimental results. But underneath, they tell two very different stories about reality. One offers tangible pictures,while the other demands we let go of intuition and embrace a world where particles are secondary, and fields are fundamental.

This is not merely a philosophical clash, rather, it shapes how we understand nothingness, force, and matter itself. So, let’s step into the ring and explore this deep, quiet duel at the heart of physics and how it links to the title of this blog.


## The Underlying Field
As we have already discussed in blog 2, Quantum Field Theory postulates that particles are mere excitations of fields, and these field are actually fundamental. In other words, a particle is the smallest possible vibration of a quantum field. Just like how a photon is the smallest quanta of the electromagnetic field, the Higgs boson plays the same role to the Higgs field. These quanta can be described by their relativistic equations of motion. 

$$
\frac{\partial^2\phi}{\partial t^2}-c^2\frac{\partial^2\phi}{\partial x^2}+\omega_0^2\phi=0
$$

where $$\phi=\phi(x,t)$$ is a field that permeates spacetime, holding a value at every point. Let's assume a plane wave solution:

$$
\phi(x,t)=A\cos(kx-wt)
$$

and see what we get. So, we first compute the derivatives:


$$
\frac{\partial^2\phi}{\partial t^2}
&= -A\omega^2\cos(kx-\omega t),
$$

$$
\frac{\partial^2\phi}{\partial x^2}
&= -Ak^2\cos(kx-\omega t).
$$

Inserting these into the wave equation gives us:


$$
-A\omega^2\cos(kx-\omega t)
- c^2(-Ak^2\cos(kx-\omega t))
+ \omega_0^2 A\cos(kx-\omega t)=0.
$$


Factoring out the common term $$A\cos(kx-\omega t)$$ gives us:

$$
A\cos(kx-\omega t)\left(-\omega^2 + c^2k^2 + \omega_0^2\right)=0.
$$

For a nontrivial solution ($$A\neq 0$$), the bracket must vanish. 

Thus we obtain the dispersion relation:

$$
\omega^2 = c^2k^2 + \omega_0^2
$$

In relativistic field theory, the constant $$\omega$$ is identified with the mass term,

$$
\omega_0^2 = \frac{m^2c^4}{\hbar^2},
$$

giving the standard result:

$$
\omega^2 = c^2k^2 + \frac{m^2c^4}{\hbar^2},
$$

which is equivalent to the relativistic energy relation:

$$
E^2 = p^2c^2 + m^2c^4,
$$

with $$E=\hbar\omega$$ and $$p=\hbar k$$.

So, we can see that this $$\omega_0$$ term is intimately related with mass as we follow the math. And if you recall from blog 9, this is also the frequency of a Dirac spinor, when you solve the Dirac equation for the case $$\Delta p=0$$. These crossroads are becoming common in all of our deep dives, reassuring us that we are on the right track.

### The Possibility of Massless Quanta

Speaking of the connectivity of physics, we are about to reproduce a famous equation as a special case for when $\omega_0=0$. The relativistic equation of motion reduces to:

$$
\frac{\partial^2\phi}{\partial t^2}-c^2\frac{\partial^2\phi}{\partial x^2}=0
$$

which, quite conveniently, is the $$\textbf{wave equation}$$ for a wave traveling at the speed of light (That's light itself! Isn't it?). And $$\omega_0=0$$ naturally means that the quanta of the field are massless, which ties elegantly to the fact that light $$\textbf{is}$$ massless. Physics is truly beautiful. The dispersion relation for such a field is:

$$
\omega^2=c^2k^2
$$

meaning that as k approaches 0, the field can settle into a point of zero frequency (No vibrations or ripples).


### The Massive Quanta

The same can not be said when you follow the dispersion relation for massive quanta, where the minimum frequency approaches $$\omega=\omega_0$$ as $$k\rightarrow0$$

In this case, we can say:

$$
\omega^2=\frac{m^2c^4}{\hbar^2} 
$$

The mass in such a case becomes:

$$
m=\frac{\hbar\omega}{c^2}
$$

So, this gives us a way of determining the mass of a quanta. This relation can also be reproduced when you set:

$$
E=\hbar\omega=mc^2
$$

which is a simple yet elegant way of combining relativity with quantum mechanics. The dispersion relations for both cases are given in Figure 1.

!<!-- Animation of vacuum fluctuations -->
<p align="center">
  <img src="/assets/images/DispersionComparison.gif" width="500" alt="J.J Thomson's model of the atom"/>
  <br><em>Simulation 1: The Dispersion Relations for massive and massless quanta.</em>
</p>



## The Origin of Potential

Despite the beauty of the equations, we can not ignore the fact that in the expression of the relativistic equations of motion:

$$
\frac{\partial^2\phi}{\partial t^2}-c^2\frac{\partial^2\phi}{\partial x^2}+\omega_0^2\phi=0
$$,

the last term appears to be added by hand with no real justification. This is where the concept of potential of a field comes into play. This final term is commonly referred to as the restoring term because it introduces a mechanism by which a field can settle to a minimum and stable value. This last term can be rewritten as:

$$
\frac{\partial^2\phi}{\partial t^2}-c^2\frac{\partial^2\phi}{\partial x^2}+\frac{\partial V}{\partial \phi}=0
$$

This potential ultimately decides the nature of the restoring term and the mass term. 

So, if one assumes a quadratic potential:

$$
V(\phi)=\frac{\omega_0^2\phi^2}{2}
$$,

then the first derivative yields:

$$
\frac{\partial V}{\partial \phi}=\omega_0^2\phi
$$

which recovers the relativistic equation of motion. This potential is called the $$\textbf{Quadratic Potential}$$. This approach is similar, in spirit, to a particle oscillating on a spring. The potential of the particle is given by:

$$
V(x)=\frac{1}{2}kx^2
$$

And the force can be calculated by:

$$
F=\frac{\partial V}{\partial x}=kx
$$

So, the potential is another fundamental property of a field which dictates how particles behaves under its influence. 


The incorporation  of potential introduces another feature of the framework, which is referred to as stability. Any object left to itself, wants to settle into a position where its energy is minimized. Picture a ball in a hilly area: given enough of a push, it would settle into the lowest point of the area and stay there. Mathematically:

$$
\left.\frac{\partial V}{\partial \phi}\right|_{\phi = v} = 0   
$$

This resting value v is known as the \textbf{Vacuum Expectation Value} v and is the minimum of the field where every particle that left to itself, wants to settle on. Think of it like a couch on a Sunday. Now, let's see what happens when this field is nudged from its stable configuration.

<!-- Animation of vacuum fluctuations -->
<p align="center">
  <img src="/assets/images/RightTextPotentialVisualization.gif" width="500" alt="J.J Thomson's model of the atom"/>
  <br><em>Simulation 2: The significance of the minima.</em>
</p>


## Perturbing a Field from its Resting State

Let's apply a field-dependent perturbation ($h(x,t)$) to $$\phi(x,t)$$ such that:

$$
\phi(x,t)=v+h(x,t)
$$

to:

$$
\frac{\partial^2\phi}{\partial t^2}-c^2\frac{\partial^2\phi}{\partial x^2}+\frac{\partial V}{\partial \phi}=0
$$.

We note that v is constant, so

$$
\frac{\partial^2 \phi}{\partial t^2} = \frac{\partial^2 h}{\partial t^2},
\qquad
\frac{\partial^2 \phi}{\partial x^2} = \frac{\partial^2 h}{\partial x^2}.
$$.

So the equation becomes:

$$
\frac{\partial^2 h}{\partial t^2}
- c^2 \frac{\partial^2 h}{\partial x^2}
+ \left.\frac{\partial V}{\partial \phi}\right|_{\phi = v + h} = 0.
$$


Using Taylor expansion, we can expand the potential derivative about the vacuum v,

$$
\left.\frac{\partial V}{\partial \phi}\right|_{\phi = v + h} =
\left.\frac{\partial V}{\partial \phi}\right|_{\phi = v} +
\left.\frac{\partial^2 V}{\partial \phi^2}\right|_{\phi = v} h
+ \mathcal{O}(h^2),
$$

where $$\mathcal{O}(h^2)$$ are higher order terms.

By using the vacuum condition,

$$
\left.\frac{\partial V}{\partial \phi}\right|_{\phi = v} = 0,
$$

we obtain the linearized equation of motion:

$$
\frac{\partial^2 h}{\partial t^2}
- c^2 \frac{\partial^2 h}{\partial x^2}
+ \eta^2 h = 0,
$$

where

$$
\eta^2 \equiv \left.\frac{\partial^2 V}{\partial \phi^2}\right|_{\phi = v}.
$$

This matches the exact form as earlier:

$$
\frac{\partial^2\phi}{\partial t^2}-c^2\frac{\partial^2\phi}{\partial x^2}+\omega_0^2\phi=0
$$

where $$\eta^2$$ matches with $$\omega_0^2$$, so the mass of the quanta comprising the field can be restated as:

$$
m=\frac{\hbar\eta}{c^2}
$$

So the mass depends on the curvature of the potential at the resting value. In other words, the sharper the cliff, the more massive the particle. But as it turns out, most particles do not gain mass by virtue of the curvature of their corresponding potential.

\begin{frame}{The True Mass Generating Mechanism}

To understand that part of the picture, we must study a case where $ $$\phi$$ $ (a field with non-zero VEV) interacts with a field  $$\psi$$ , that has no VEV. The potential of a 2-field interacting system is given by:

$$
V(\phi,\psi)=V(\phi)+U(\psi)+\frac{1}{2}g^2\psi^2\phi^2
$$

where g is the coupling constant, and determines the strength of the interaction. Its exact value is irrelevant to us, we can just assume it to be non-zero and move on. 

The equations of motion for the fields are obtained by taking functional derivatives
of the potential with respect to each field.

For the field $ $$\phi$$ $, we compute

$$
\frac{\partial V(\phi,\psi)}{\partial \phi} 
= \frac{\partial V(\phi)}{\partial \phi} + \frac{1}{2} g^2 \psi^2 \frac{\partial}{\partial \phi}(\phi^2)
= \frac{\partial V(\phi)}{\partial \phi} +
g^2 \psi^2 \phi.
$$

The equation of motion for $ $$\phi$$ $ is therefore

$$
\frac{\partial^2 \phi}{\partial t^2}
- c^2 \frac{\partial^2 \phi}{\partial x^2}
+ \frac{\partial V(\phi)}{\partial \phi}
+ g^2 \psi^2 \phi
= 0.
$$

    
Similarly, for the field $$\psi$$ we find

$$
\frac{\partial V(\phi,\psi)}{\partial \psi} =
\frac{\partial U(\psi)}{\partial \psi} +
\frac{1}{2} g^2 \phi^2 \frac{\partial}{\partial \psi}(\psi^2) =
\frac{\partial U(\psi)}{\partial \psi} + g^2 \phi^2 \psi.
$$

The corresponding equation of motion for $$\psi$$ is

$$
\frac{\partial^2 \psi}{\partial t^2}
- c^2 \frac{\partial^2 \psi}{\partial x^2}
+ \frac{\partial U(\psi)}{\partial \psi}
+ g^2 \phi^2 \psi
= 0.
$$

Now, we impose the condition that the quanta of the $$\phi$$ field are massless, despite it having a non zero VEV. Therefore there will be no mass term in the $ $$\phi$$ $ and the resulting equation is:

$$
\frac{\partial^2 \phi}{\partial t^2}
- c^2 \frac{\partial^2 \phi}{\partial x^2}=0
$$

Furthermore, by assuming that $$\psi$$ is settled at its resting value, its equation reduces to:

$$
\frac{\partial^2 \psi}{\partial t^2}
- c^2 \frac{\partial^2 \psi}{\partial x^2}
+ g^2 v^2 \phi
= 0.
$$

It is apparent that $$\omega_o^2=g^2v^2$$, and therefore we can say that:

$$
m_\psi=\frac{\hbar gv}{c^2}
$$

This is interesting. The quanta of field ( $$\psi$$ ) acquired a mass because it coupled to another field. What's more interesting is that this field that it interacted with ($$\phi$$) is massless on its own, but has a non-zero VEV. So $$m_\psi$$ depends, primarily, on the VEV of  $$\phi$$  and not on its own potential. A zero VEV of $ $$\phi$$ $ implies that  $$\psi$$  is massless. 

We have seen how the curvature of a field’s potential determines the mass of its own quanta. But not all mass arises this way as fields with no VEV can acquire mass purely through interactions with other fields that do have a vacuum expectation value. 



 



