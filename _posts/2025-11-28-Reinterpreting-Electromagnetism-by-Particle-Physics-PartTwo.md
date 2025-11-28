---

title: "Blog 9—Walking through the Birth of Electromagnetism from Gauge Theory: Part 2"
date: 2025-11-28
categories: [Particle Physics, Electromagnetism, Gauge Theory, Atomic and Molecular Physics, Fundamental Forces]
use_math: true
layout: single
author_profile: true
read_time: true
comments: true
excerpt: "We now delve into the mathematics of local U(1) symmetry and uncover how a Dirac field must be modified for its physics to remain invariant under this transformation."


---

## Introduction

This blog post is a follow-up of the previous post. Today, we will look at the Lagrangian of Quantum Electro-Dynamics and apply the local gauge transformation on it. These look like very fancy words, and they are, so prepare for the most challenging post yet. But with the challenge comes a great reward which is the fact that by the end of the series, you will be able to see how electromagnetism blossoms from a simple symmetry, and it is sure to blow your mind. Without further ado, let's begin.

## What is a Lagrangian?

The real question should be: "What isn’t the Lagrangian?". 

In particle physics, the Lagrangian is everything. It’s a single equation that tells us everything we need to know about a system, its evolution, its interactions, and how symmetries shape the forces of nature.  

The idea comes from the Principle of Least Action. Nature, as it turns out, is kind of lazy, and always takes the path that requires the least "effort" (technically, the path that minimizes the action S):

$$
S = \int L \, dt
$$

Here, L is the Lagrangian density, or one can say, the crown jewel of the system.

For a single particle, the Lagrangian is simply:

$$
L = T - V
$$

where T is the kinetic energy and V is the potential energy. For example, a free particle (no potential) moving with velocity v has:

$$
L = \frac{1}{2}mv^2
$$

Applying the Euler–Lagrange equation:

$$
\frac{d}{dt}\left(\frac{\partial L}{\partial \dot{x}}\right) - \frac{\partial L}{\partial x} = 0
$$

we get:

$$
m\ddot{x} = 0
$$

which is simply Newton’s First Law for constant velocity motion.  

So yes, the Lagrangian secretly encodes all of classical mechanics, and when generalized to fields, it will give us all of quantum field theory. Every particle, every force, every interaction — all born from this one quantity $\mathcal{L}$. There are more fun exercises we can do with the Lagrangian mechanics, that we simply can't with Newtonian mechanics e.g. proving that the shortest distance between 2 points in a 2D plane is a straight line.

To learn more about its applications for beginners, refer to chapter 1 of "Introduction to Classical Mechanics" by Goldstein.

## The Dirac Lagrangian

For our purposes, the Lagrangian we need has to encode the Dirac field. This seems like a complicated task, but in natural units the Dirac the Lagrangian has an uncanny resemblance with the Dirac equation.

$$
\mathcal{L}_D = \bar{\psi}\left(i\gamma^\mu \partial_\mu - m\right)\psi,
$$

In fact, this resemblance is not a coincidence. The Dirac Lagrangian is constructed so that when you apply the Euler–Lagrange equations to it, you recover the Dirac equation itself. In other words, the Lagrangian is the compact, elegant parent equation from which the entire dynamics of the Dirac field can be derived. The readers can prove this for themselves, but what's new is the $$\bar{\psi}$$ known as the adjoint. If,

 $$
 \psi =
\begin{pmatrix}
\psi_1 \\
\psi_2\\
\psi_3 \\
\psi_4 
\end{pmatrix}
$$
    
then,

$$
\bar{\psi} =
\begin{pmatrix}
\psi_1^* & \psi_2^* & -\psi_3^* & -\psi_4^*
\end{pmatrix}
$$

Since we are familiar with the Dirac equation and its implications from blog 1 and 8, we can make sense of this form of the Lagrangian. 

Before diving into the math, another important fundamental concept relevant here is that of the Noether's theorem which states that for every obeyed symmetry, there exists a conserved quantity. Though this seems pretty abstract for now, it will be having massive implications later on.

## Global Gauge Invariance

Now that we have the Dirac Lagrangian, let’s see what happens when we poke it a little. Physics loves symmetry, and one of the most beautiful symmetries we can demand from our Lagrangian is gauge invariance. 

What does that mean? It means that the physics of our system should not change if we rotate the complex phase of our wavefunction:

$$
\psi^{\prime} \rightarrow e^{i\alpha}\psi,
$$

where $$\alpha$$ is just some constant phase. This transformation doesn’t affect anything observable, since multiplying by a complex phase doesn’t change the probability density $$\psi^\dagger \psi$$ since the exponent's complex conjugate cancels out with the complex factor:

$$
\psi=Ae^{i\alpha}, \quad \psi^*=Ae^{-i\alpha}
$$

$$
\psi\psi^*=A^2e^{i\alpha}e^{-i\alpha}=A^2
$$

Therefore, when we apply this transformation, 

$$
\mathcal{L}_D = \bar{\psi}(i\gamma^\mu \partial_\mu - m)\psi, \quad \psi \rightarrow\psi e^{i\alpha}
$$

We get:

$$
\mathcal{L}_D^{\prime} = \bar\psi e^{-i\alpha}(i\gamma^\mu \partial_\mu - m)\psi e^{i\alpha}
$$

$$
\mathcal{L}_D^{\prime} = \bar\psi (i\gamma^\mu \partial_\mu - m)\psi e^{-i\alpha} e^{i\alpha}
$$

$$
\mathcal{L}_D^{\prime} = \bar\psi (i\gamma^\mu \partial_\mu - m)\psi  
$$

$$
\mathcal{L}_D^{\prime} =  \mathcal{L}_D
$$

Since the transformed Lagrangian is exactly the same as the original, the physics of our system is oblivious to the transformation. This is called global gauge invariance, and it’s a direct reflection of charge conservation which a deep result encoded in Noether’s theorem. Keep in mind that $$\psi$$ is no ordinary wavefunction, but a spinor whose phase factor did not depend on its position.

## Local Gauge Invariance

Global gauge invariance was cool, but let’s push our luck. What if the phase $$\alpha$$ wasn’t constant? What if it could change with position and time?

$$
\psi \rightarrow e^{i\alpha(x)}\psi
$$

Now the transformation depends on spacetime itself. Now, let's test invariance now and see the fireworks.

$$
\mathcal{L}_D = \bar{\psi}(i\gamma^\mu \partial_\mu - m)\psi, \quad \psi \rightarrow\psi e^{i\alpha(x)}
$$

The adjoint transforms as

$$
\bar\psi\longrightarrow \bar\psi'
= e^{-\,i\alpha(x)}\bar\psi.
$$

We must evaluate the derivative term carefully:

$$
\partial_\mu\psi'=\partial_\mu\big(e^{i\alpha(x)}\psi\big)
= e^{i\alpha(x)}\partial_\mu\psi + i(\partial_\mu\alpha(x))\,e^{i\alpha(x)}\psi.
$$


Hence

$$
i\gamma^\mu\partial_\mu\psi' = i\gamma^\mu e^{i\alpha}\partial_\mu\psi
- \gamma^\mu e^{i\alpha}(\partial_\mu\alpha)\psi,
$$

$$
\mathcal{L}_D = \bar{\psi}(i\gamma^\mu \partial_\mu - m)\psi
$$

$$
\mathcal{L}_D = \bar{\psi}(i\gamma^\mu \partial_\mu)\psi - \bar{\psi}m\psi
$$

Picking all the puzzle pieces and placing them together, the transformed Dirac Lagrangian becomes:

$$
\mathcal{L}_D^{\prime} = \bar\psi e^{-i\alpha(x)}\gamma^\mu e^{i\alpha(x)}\partial_\mu\psi
- \bar\psi e^{-i\alpha(x)}\gamma^\mu e^{i\alpha(x)}(\partial_\mu\alpha(x))\psi - \bar{\psi}e^{-i\alpha(x)}m\psi e^{i\alpha(x)}
$$

$$
\mathcal{L}_D^{\prime} = \bar\psi i\gamma^\mu \partial_\mu\psi
- \bar\psi\gamma^\mu (\partial_\mu\alpha(x))\psi - \bar{\psi}m\psi
$$

$$
\mathcal{L}_D^{\prime} = \bar\psi i\gamma^\mu \partial_\mu\psi - \bar{\psi}m\psi
- \bar\psi\gamma^\mu (\partial_\mu\alpha(x))\psi 
$$

$$
\mathcal{L}_D^{\prime} = \bar\psi (i\gamma^\mu \partial_\mu - m)\psi
- \bar\psi\gamma^\mu (\partial_\mu\alpha(x))\psi 
$$

Therefore, the relationship between the Dirac Lagrangian and it's transformed counterpart is:

$$
\mathcal{L}_D^{\prime} = \mathcal{L}_D
- \bar\psi\gamma^\mu (\partial_\mu\alpha(x))\psi 
$$

Following the same chain of thought as earlier, we clearly see that the transformed Lagrangian has an additional term as compared to the original Lagrangian. This means that the physics has changed and the Dirac Lagrangian itself does not have local gauge invariance. 

However, if we are adamant that local invariance is a given and try to necessitate it, how can we incorporate it? After all, mathematics never lies. 


## An Ad-Hoc Solution
In a desperate bid to restore local gauge invariance let's add the exact same term back into the original Dirac Lagrangian to counter the deficit causing the variance.

So, I will go ahead and write:

$$
\mathcal{L}_d = \bar{\psi}(i\gamma^\mu \partial_\mu - m)\psi + \bar\psi\gamma^\mu (\partial_\mu\alpha(x))\psi
$$

Here d notates "Dream" not "Dirac", since by adding a term to your Lagrangian, you're no longer representing the same Dirac system, but an ideal Dreamy system which solves all of our problems. We have no idea what this "Dream" system represents but let's test invariance once more using the quantities we have already derived. 

$$
\mathcal{L}_d = \mathcal{L}_D + \bar\psi\gamma^\mu (\partial_\mu\alpha(x))\psi
$$

Applying the dreaded transformation:

$$
\mathcal{L}_d^{\prime}= \mathcal{L}_D^{\prime} - \bar\psi\gamma^\mu (\partial_\mu\alpha(x))\psi+ \bar\psi e^{-i\alpha(x)}\gamma^\mu (\partial_\mu\alpha(x))\psi e^{i\alpha(x)}
$$


$$
\mathcal{L}_d^{\prime}= \mathcal{L}_D^{\prime} - \bar\psi\gamma^\mu (\partial_\mu\alpha(x))\psi+ \bar\psi\gamma^\mu (\partial_\mu\alpha(x))\psi (e^{-i\alpha(x)}.e^{i\alpha(x)})
$$

$$
\mathcal{L}_d^{\prime}= \mathcal{L}_D^{\prime} - \bar\psi\gamma^\mu (\partial_\mu\alpha(x))\psi+ \bar\psi\gamma^\mu (\partial_\mu\alpha(x))\psi 
$$

$$
\mathcal{L}_d^{\prime}= \mathcal{L}_D^{\prime}
$$

So at least, the dream Lagrangian does solve our problem but any good physicist should call foul on this. After all, we know how important and fundamental the Lagrangian is and I just went forward and added a term there like it was no big deal. Yes, it solves the problem but this is not how physics is done. A term can not be introduced just for the sake of solving a problem but should serve a purpose. And  the fact that it shows up in a Lagrangian, of all places, means that it should be something fundamental. 

So let's try to interpret the fundamental change we were forced to bring.



## Conclusion

So, I’ll leave you with the guilt of the sin we’ve just committed, by adding something that suits our need but tears physics apart. In the next blog, we’ll try to justify our sin before the physics jury, and make sense of the beautiful mess we’ve created. See you in the next post, and until then, keep on physicsing.
