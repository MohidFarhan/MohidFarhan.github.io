---

title: "Blog 13—The Duel Between Particle Physics and Quantum Field Theory (Part 2)"
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

In the last post, we saw that fields can acquire mass by interacting with another field having a non-zero vacuum expectation value. Today, we are going to expand our understanding to unravel a significant development in our understanding of physics.

In July 2012, the world of physics witnessed its latest milestone, when scientists at CERN announced the discovery of a new particle, termed as the Higgs boson. Overnight, headlines dubbed it “$$\textbf{the God Particle}$$,” and while physicists winced at the nickname, the excitement was somewhat justified. This tiny, fleeting particle represented the final missing piece of the Standard Model, the framework that describes all known fundamental particles and their interactions.

The Higgs boson is the visible imprint of an invisible mechanism, and a field, that quietly permeates the entire universe. Without this field, particles like electrons and quarks would have no mass, atoms would never form, and stars and galaxies would never ignite. In other words, the Higgs boson helps explain why anything in the universe weighs anything at all.

Despite its fame, the Higgs remains one of the most mysterious players in modern physics. Its discovery opened as many questions as it answered: Why does the Higgs field have the value it does? Is it connected to dark matter or dark energy? Could there be more Higgs-like particles hidden beyond the Standard Model?

In today's post, we will explore what the Higgs boson is, why its discovery was such a monumental achievement, and how it continues to shape our understanding of the universe.

## Acquiring a non-zero VEV

We explored a quadratic potential in the previous blog, but that yielded a zero VEV. We now need a potential which allows $$\phi$$ to acquire a non-zero VEV. Enter the Higgs potential:

$$
V(\phi) = -\frac{1}{2}\mu^2\phi^2 + \frac{1}{4}\lambda\phi^4
$$
where $$\mu^2$$ and $$\lambda$$ are both positive. Let's do some mathematics to justify our choice.

To find the $$\textbf{Vacuum Expectation Value (VEV)}$$, we must determine the value of $$\phi$$ that minimizes the potential energy.


First, we calculate the first derivative of the potential with respect to the field $$\phi$$ and set it to zero:

$$
\frac{dV}{d\phi} = \frac{d}{d\phi} \left( -\frac{1}{2}\mu^2\phi^2 + \frac{1}{4}\lambda\phi^4 \right)
$$

$$
\frac{dV}{d\phi} = -\mu^2\phi + \lambda\phi^3 = 0
$$


We can solve this equation by factoring out $$\phi$$:

$$
\phi \left( -\mu^2 + \lambda\phi^2 \right) = 0
$$

This yields two distinct solutions for the field:

The symmetric state: $$\phi = 0$$, and the broken-symmetry state: $$\phi^2 = \frac{\mu^2}{\lambda}.$$


To confirm we have found a minimum rather than a maximum, we examine the second derivative:

$$
\frac{d^2V}{d\phi^2} = -\mu^2 + 3\lambda\phi^2
$$

$$\textbf{At the origin ($\phi = 0$): }$$ The second derivative is $$-\mu^2$$. Since this is negative, the origin is an unstable local maximum.

$$\textbf{At the non-zero points: }$$ We substitute $$\phi^2 = \frac{\mu^2}{\lambda}$$ into the second derivative:


$$
\frac{d^2V}{d\phi^2} = -\mu^2 + 3\lambda \left( \frac{\mu^2}{\lambda} \right) = 2\mu^2
$$

Since $$2\mu^2 > 0$$, these points represent stable global minima.
    

The field naturally "settles" into one of these minima. We define this stable value as the Vacuum Expectation Value, $$v$$:

$$
v = \pm\sqrt{\frac{\mu^2}{\lambda}}
$$

![Figure 1](/assets/images/B13P1.jpg)
**Figure 1**: The Higgs field in its uniform vacuum state, showing the constant Vacuum Expectation Value (VEV) $$v \approx 1.41$$ that permeates all of space.

Because $$v \neq 0$$, the symmetry of the system is spontaneously broken, providing a mechanism for particles to acquire mass.

The fact that the origin is at an unstable stationary point, with stable stationary points on either side--at a distance of v from the origin--sets the stage for $$\textbf{Spontaneous Symmetry Breaking}$$.

## Imprints of Spontaneous Symmetry Breaking

Let us revisit the equation of motion of the field $$\phi$$,


$$
\frac{\partial^2 \phi}{\partial t^2} - c^2 \frac{\partial^2 \phi}{\partial x^2} + \frac{\partial V(\phi)}{\partial \phi} + g^2 \psi^2 \phi= 0.
$$ 

And with the Higgs potential, it becomes:

Let us revisit the equation of motion of the field $$\phi$$,


$$
\frac{\partial^2 \phi}{\partial t^2} - c^2 \frac{\partial^2 \phi}{\partial x^2} +\phi \left( -\mu^2 + \lambda\phi^2 \right) + g^2 \psi^2 \phi = 0.
$$

where $$\phi=v$$ is the resting value, the field wants to settle at, when left to itself. Now, let's cause a perturbation $$h$$ in the field such that:

$$
\phi(x,t)=v+h(x,t)
$$
  

where $$v$$ is the constant VEV and $$h(x,t)$$ is the physical Higgs field.

![Figure 2](/assets/images/B13P2.jpg)
**Figure 2**: A perturbation $$h(x,t)$$  propagating through the Higgs field, representing the excited state that we detect as the Higgs boson particle.

Substituting $$\phi = v + h$$ into the Equation of Motion:

$$
\frac{\partial^2 h}{\partial t^2} - c^2 \frac{\partial^2 h}{\partial x^2} + (v+h)\left[ -\mu^2 + \lambda(v+h)^2 \right] + g^2 \psi^2 (v+h) = 0
$$


We expand the term $$P(h) = (v+h)(-\mu^2 + \lambda(v+h)^2)$$ around $$h=0$$:

$$
P(h) \approx P(0) + P'(0)h + \frac{1}{2}P''(0)h^2 + \dots
$$

Performing the algebraic expansion:
$$
(v+h)(-\mu^2 + \lambda v^2 + 2\lambda v h + \lambda h^2)
$$
Since $$\lambda v^2 - \mu^2 = 0$$ at the minimum:

$$
(v+h)(2\lambda v h + \lambda h^2) = 2\lambda v^2 h + 3\lambda v h^2 + \lambda h^3
$$

Keeping only the linear term for the wave equation, as an approximation if h is small:

$$
\approx 2\lambda v^2 h
$$


Substituting the linear terms back into the Equation of motion:

$$
\frac{\partial^2 h}{\partial t^2} - c^2 \frac{\partial^2 h}{\partial x^2} + (2\lambda v^2) h + g^2 \psi^2 v \approx 0
$$


Since $$\mu^2=\lambda v^2$$,

$$
\frac{\partial^2 h}{\partial t^2} - c^2 \frac{\partial^2 h}{\partial x^2} + 2\mu^2 h + g^2 \psi^2 v \approx 0
$$

We can neglect the interaction terms since we are retaining only the linear terms under the assumption of small h. I will provide a disclaimer that this is an approximation, and the picture it will describe is an oversimplified one. 

![Figure 3](/assets/images/B13P3.jpg)
**Figure 3**: The "ball rolling down the hill" analogy for spontaneous symmetry breaking, showing the field settling into a stable minimum and oscillating around it—these oscillations correspond to the Higgs boson.
![Figure 4](/assets/images/B13P4.jpg)
**Figure 4**: Mass generation via coupling to the Higgs field, illustrating how different particles (photon, electron, quark) acquire mass proportional to their interaction strength with the omnipresent Higgs field.

Once the dust settles, we are left with:

$$
\frac{\partial^2 h}{\partial t^2} - c^2 \frac{\partial^2 h}{\partial x^2} + 2\mu^2 h= 0
$$

What we have just written down is the equation of motion of the Higgs field, which is the field responsible for giving mass to other fields. If this field interacts strongly with you, you attain a mass, and if it doesn't, you will forever be massless. And this was just theory until 2012, when the LHC detected the quantum excitation of this field, and it was termed the Higgs boson. This was named after Peter Higgs, the genius physicist who devised this mechanism from first principles. Let's zero in on this field and quantize it, to find the Higgs boson.
![Figure 5](/assets/images/B13P7.jpg)
**Figure 5**: The discovery of the Higgs boson at CERN in 2012, showing the proton-proton collision process, the energy scale peak at 125 GeV, the 5σ statistical significance required for discovery, and the 50-year timeline from theoretical proposal to experimental confirmation.


Notice that this equation is of the same form we discussed in our previous blog,

$$
\frac{\partial^2\phi}{\partial t^2}-c^2\frac{\partial^2\phi}{\partial x^2}+\omega_0^2\phi=0
$$

so the mass of the quanta for such a field would be:

$$
m=\frac{\hbar\omega_0}{c^2}
$$
Therefore, applying the same formalism to $$h$$, gives us:
$$m_h=\frac{\hbar \sqrt{2}\mu}{c^2}$$

This can also be rewritten as:

$$
m_h=\frac{\hbar \sqrt{\frac{\partial^2V(\phi)}{\partial\phi^2}}}{c^2}
$$

    
when you realize that:

$$
\left.\frac{\partial^2V}{\partial \phi^2}\right|_{\phi = \pm \sqrt{\frac{\mu^2}{\lambda}}}=2\mu^2
$$

So the mass of this particle, the Higgs boson, is dependent on how steep the potential is on its resting value.
![Figure 6](/assets/images/B13P5.jpg)
**Figure 6**: Wave propagation comparison showing the dispersion relation for massless photons ($$\omega=ck$$) versus massive Higgs bosons ($$\omega^2=c^2k^2+(m_h c^2)^2$$), and the connection between potential curvature at the minimum and particle mass.

![Figure 7](/assets/images/B13P6.jpg)
**Figure 7**: Left: The universe cooling from high temperature (symmetric phase with $$\phi=0$$ ) through the critical temperature to the low temperature broken-symmetry phase where the field acquires a non-zero VEV.
Right: Quantum fluctuations around the vacuum minimum, where small oscillations correspond to the physical Higgs boson excitation.
