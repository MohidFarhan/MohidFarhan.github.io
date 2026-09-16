---

title: "Blog 2—Inside the Atom: Where ‘Empty Space’ Teems with Activity"
date: 2025-08-16
categories: [Quantum Field Theory, Relativistic Quantum Mechanics, Particle Physics, Atomic and Molecular Physics]
use_math: true
layout: single
author_profile: true
read_time: true
comments: true
excerpt: "A subtle shift in hydrogen’s energy levels cracked open the door to quantum field theory which revealed the dynamic, buzzing vacuum inside every atom."


---

## Introduction

Today we will unravel the idea that in physics, there is no such thing as empty space. What we like to call "empty" is teeming with activity and fluctuations at the quantum scales. This is not just theory, but has measurable consequences, all of which we will get into as we go forward, so enjoy the adventure. You will need a grasp of basic quantum mechanics, electromagnetic theory and a bit of atomic and molecular physics to go with that. 

Our understanding of the atom was a hot topic for physicists in the early 1900s, with J.J. Thompson's famous "fruitcake" model, where the atom was assumed to be a smooth and filled sphere of positive charge, with clumps of negative charges embedded in it. 

<!-- Animation of vacuum fluctuations -->
<p align="center">
  <img src="/assets/images/Adobe Express - VacuumThomson.gif" width="500" alt="J.J Thomson's model of the atom"/>
  <br><em>Simulation 1: The Fruitcake Model of the atom. This model was later refined.</em>
</p>


In 1911, Ernest Rutherford devised the most accurate atomic model known to man, backed by an experiment, where a minority of alpha particles were observed to scatter off at large angles when targeted at a thin foil of gold. This showed that an atom was mostly empty space with a lot of its mass being concentrated at the center, leading to such dramatic scattering. This center with positive charge is known as a nucleus, with negative electrons orbiting around it.

<!-- Animation of vacuum fluctuations -->
<p align="center">
  <img src="/assets/images/Adobe Express - HydrogenAtom.gif" width="500" alt="J.J Thomson's model of the atom"/>
  <br><em>Simulation 2: A not-to-scale, oversimplified visualization of the most fundamental atom in the universe: Hydrogen. Here, the radius of the orbit is kept constant at the Bohr radius, but in reality, the Bohr radius is the most likely radius of an atom at any given point. In the literal sense, the atomic radius is not always constant but we will assume so, in this post, for simplification.</em>
</p>

 

## The Empty Space in an Atom

Now that we objectively know that most of the atom is empty space, lets make estimations to quantify this emptiness. The Rutherford model predicts the radius of the atom to be of the order $$r_a \approx 10^{-10}m$$ and of the nucleus to be $$r_n \approx 10^{-15}m$$. Comparing the ratios of their volumes gives:

$$
\frac{\frac{4 \pi (r_a)^3}{3}}{\frac{4 \pi (r_n)^3}{3}}=\frac{r_a^3}{r_n^3} \approx (\frac{10^{-10}}{10^{-15}})^3 \approx 10^{15}
$$

This tells us that the atom is almost completely empty. To  give you an idea of the magnitude of this ratio, its like if the atom was the size of a football field, the nucleus would be a cherry placed in its center. Now, let's dive into the deep end. If I claimed that there is no such thing as empty space, that what is actually going on in that space?

To understand this, we will view the atom from the lens of Quantum Field Theory (QFT).

## The Behaviour of the Electrons

   In the classical treatment of the atom, the electrons should spiral into the nucleus while radiating energy and ultimately the atom should collapse in picoseconds assuming that it is purely a particle. However, in the quantum mechanical treatment, it is assumed to be a wave, in the sense that all of its information is inscribed in its wavefunction $$\psi$$, which can be computed by solving the Schrodinger equation:
   
$$
\left[-\frac{\hbar^2}{2m} \nabla^2 - \frac{e^2}{4\pi \varepsilon_0 r} \right] \psi = E \psi
$$

This $$\psi$$ acts like a probability that is distributed throughout empty space, which do not locate the electron exactly, but rather give the probability of where we are likely to find it. As it turns out, the resulting $$\psi$$ leads to discrete energy levels which keep the atom stable, and the electron's energy constant, with different energies corresponding to different shells. While all this points to the fact that empty space is not truly empty due to a probability being smeared all across it, the real game-changer is the addition of special relativity and relativistic quantum mechanics. 

## Particles in a Contracting Box

One can intuitively picture the atom as a small sphere, which contrains the particles confined within it. To understand the dominance of quantum effects, let's analyze the example of a particle in a contracting box.  The Heisenberg Uncertainty Principle says that the smaller the uncertainty in position, the larger the uncertainty in momentum and vice versa. 

$$
\Delta p \Delta x \geq \frac{\hbar}{2}
$$

So if an electron is constrained to a small enough space, relativistic effects become dominant. In such a case, the characteristic energy can be approximated as: 

$$
E \approx \Delta pc \approx mc^2
$$

$$
\frac{\hbar c}{2\Delta x}=mc^2
$$

$$
\Delta x=\frac{\hbar}{2m_ec} \approx 10^{-13}m
$$

So this means that if I were to constrain anything within $$10^{-13}m$$, which is the case in an atom, the correct characteristic energy can match a critical value of 1.02 MeV, which is the energy required to produce the positron-electron pair, setting the stage for jitters within the atom.

<!-- Animation of vacuum fluctuations -->
<p align="center">
  <img src="/assets/images/Adobe Express - AtomicVacuumFluctuations.gif" width="500" alt="Vacuum fluctuations inside the atom"/>
  <br><em>Simulation 3: Vacuum fluctuations appearing and disappearing within the “empty” region of the atom. These fluctuations are not just a matter of theory since they have real, measureable fingerprints that can be picked up as we will see.</em>
</p>

It becomes apparent that $$10^{-13}m$$ is bigger than the radius of the nucleus but smaller than that of the atom, hence, making the "empty" space inside the atom an ideal environment for effects to occur, as shown in the figure. The nucleus is not drawn to scale; the scale that was mentioned earlier (Cherry to a football field). It is now easy to visualize that the idea of a constant number of particles breaks down, and therefore the pure Quantum Mechanical picture becomes blurry. To incorporate and account for the creation and annhilation of particles, we need a deeper theory which treat the number of particles as variables, unlike quantum mechanics. This is where Quantum Field Theory (QFT) shines. The name of this theory is actually very self explanatory. In the QFT, quantized fields are fundamental, not particles. Particles are just localized excitations within that field. The perpective shift from pure particles (classical mechanics), to waves (quantum mechanics) to, now, fields (QFT) proves fruitful in explaining the whole picture as I will show you shortly.


## The Picture Without QFT

Before diving head-first into QFT, Let's pick a benchmark first, and treat it without QFT. We pick the simplest case here: the ground-state Hydrogen atom, with an electron orbiting a proton. We can estimate the ground-state energy of the hydrogen atom using the Heisenberg uncertainty principle. 

The total energy of the electron is approximately the sum of its kinetic and potential energies:

$$
E \approx K + U
$$

I say approximately here since this is the non-relativistic treatment and has it's shortcomings as we discussed in the previous blog. Here the kinetic energy $$K$$ is given by

$$
K = \frac{(\Delta p)^2}{2 m_e}
$$

and the potential energy $$U$$ is the Coulomb potential:

$$
U = - \frac{e^2}{4 \pi \varepsilon_0 \Delta x}.
$$

Here, $$\Delta x$$ is the characteristic size of the electron's orbit (or its position uncertainty), and $$\Delta p$$ is the momentum uncertainty.  

From the Heisenberg uncertainty principle:

$$
\Delta x \, \Delta p \gtrsim \frac{\hbar}{2} \quad \implies \quad \Delta p = \frac{\hbar}{\Delta x}.
$$

Substituting $$\Delta p$$ into the kinetic energy gives:

$$
K = \frac{\hbar^2}{2 m_e (\Delta x)^2}.
$$

Thus, the total energy as a function of $$\Delta x$$ is:

$$
E(\Delta x) = \frac{\hbar^2}{2 m_e (\Delta x)^2} - \frac{e^2}{4 \pi \varepsilon_0 \Delta x}.
$$

To find the equilibrium (minimum) energy, differentiate with respect to $$\Delta x$$ and set it to zero. For the untrained reader, this might seem like an operation that came out of nowhere, and let's try to make it make sense. All particles (or waves or fields depending upon which side you are on) in the universe have the same mission: to achieve stability. Every single particle like to lose energy and settle comfortably to the lowest energy possible and not an ounce more than that. In this case, that particle so happens to be the electron, and it is no different. It wants to orbit the nucleus such that its energy is minimized. The best way to that is to plot the energy as a function of $$\Delta x$$ and look for the value of $$\Delta x$$ where the energy is at its minimum. This would be the distnce from the nucleus that the electron would be most comfortable in being and, therefore, you are most likely to find the electron at this distance.

![Figure 1](/assets/images/HAGS.png)

**Figure 1**: The energy as a function of distance for the hydrogen atom.


$$
\frac{dE}{d (\Delta x)} = - \frac{\hbar^2}{m_e (\Delta x)^3} + \frac{e^2}{4 \pi \varepsilon_0 (\Delta x)^2} = 0.
$$

Solving for $$\Delta x$$:

$$
\frac{\hbar^2}{m_e (\Delta x)^3} = \frac{e^2}{4 \pi \varepsilon_0 (\Delta x)^2} 
\quad \implies \quad 
\Delta x = \frac{4 \pi \varepsilon_0 \hbar^2}{m_e e^2}.
$$

This reproduces the famous Bohr Radius, so thats a great sign that our working is not only correct, but also makes perfect sense. Finally, substituting this value of $$\Delta x$$ back into the total energy expression:

$$
E_1 = - \frac{m_e e^4}{2 (4 \pi \varepsilon_0)^2 \hbar^2} \approx -13.6~\mathrm{eV}.
$$

This reproduces the exact ground-state energy of the hydrogen atom. 



For the confined particle, if we take the assumption that $$\psi$$ vanishes at the edges, the allowed wavelengths are given by: 

$$
\lambda_n=\frac{2L}{n}
$$


<!-- Animation of the Allowed Wavefunctions -->
<p align="center">
  <img src="/assets/images/Adobe Express - PIAB.gif" width="500" alt="Vacuum fluctuations inside the atom"/>
  <br><em>Simulation 4: A dynamic visualization of the allowed wavefunctions that disappear at boundaries resulting in modes. Do you notice a trend in frequency?</em>
</p>


The edges (where probability disappears) are called nodes, which have distinct spatial and temporal frequencies. n is an integer value and L is the length of the constraining box. The wavenumber k (spatial frequency) is given by $$k=\frac{2 \pi}{\lambda}$$, which results in: 

$$
k=\frac{\pi n}{L}
$$

Expanding into 3 dimensions, we get the spatial frequency vector: 

$$
k=\frac{\pi}{L}(n_x,n_y,n_z)
$$

The temporal frequency, on the other hand, is given by: 

$$
\omega_k=2 \pi f=\frac{2 \pi c}{\lambda}=kc
$$

## The QFT Treatment

Quantum Field Theory pictures a field as infinite coupled modes, each acting as harmonic oscillators. 

<!-- Animation of the QFT Interpretation -->
<p align="center">
  <img src="/assets/images/Adobe Express - QFTPlaneCoupled (1).gif" width="500" alt="Vacuum fluctuations inside the atom"/>
  <br><em>Simulation 5: A visualization of a quantized fields comprised of coupled modes acting as harmonic oscillators.</em>
</p>


One can think of simulation 3 above as a 3D extension of simulation 2. The minimum energy of a quantum harmonic oscillator is, unlike classical oscillators, non zero due to the Heisenberg Uncertainty Principle. Why am I blaming HUP for this? Well, picture this...

A classical oscillator (like a pendulum) can sit at zero kinteic energy. As a matter of fact, that is exactly what happens if you don't keep on applying a force to it since it loses energy to the environment. BUT, why can't a quantum harmonic oscillator do the same? Thats because if its stationary, we know its position with certainty, and its momentum with certainty (zero). And since, HUP must be obeyed by the particles at the quantum scale, this can not happen. So when, $$\Delta x$$ becomes small, the uncertainties in momentum are a source of maintaining a minimum energy, and vice vera. Hopefully, that makes sense intuitively. Now, let's have it make sense mathematically. 

Consider a one-dimensional quantum harmonic oscillator with mass $$m$$ and angular frequency $$\omega$$. Its Hamiltonian is:

$$
\hat{H} = \frac{\hat{p}^2}{2m} + \frac{1}{2} m \omega^2 \hat{x}^2,
$$

where $$\hat{p} = -i\hbar \frac{d}{dx}$$ is the momentum operator, and the potential term (second term on the right hand side) arises from $$E=\frac{1}{2} k x^2$$ where spring constant k takes the form $$k=m \omega^2$$

To find the ground-state energy, we look for the state that minimizes the total energy. Using the Heisenberg uncertainty principle:

$$
\Delta x \, \Delta p \ge \frac{\hbar}{2},
$$

we estimate the kinetic and potential contributions in terms of $$\Delta x$$:

$$
E \approx \frac{(\Delta p)^2}{2m} + \frac{1}{2} m \omega^2 (\Delta x)^2
= \frac{\hbar^2}{8 m (\Delta x)^2} + \frac{1}{2} m \omega^2 (\Delta x)^2.
$$

![Figure 2](/assets/images/QHOGS.png)

**Figure 2**: The energy as a function of distance for the quantum harmonic oscillator.



This gives the total energy as a function of $$\Delta x$$. To find the minimum, differentiate with respect to $$\Delta x$$ and set the derivative to zero:

$$
\frac{dE}{d(\Delta x)} = -\frac{\hbar^2}{4 m (\Delta x)^3} + m \omega^2 (\Delta x) = 0.
$$

Solving for $$\Delta x$$:

$$
(\Delta x)^4 = \frac{\hbar^2}{4 m^2 \omega^2} \implies \Delta x = \sqrt{\frac{\hbar}{2 m \omega}}.
$$

Substituting back into the energy expression:

$$
E_{\min} = \frac{\hbar^2}{8 m (\Delta x)^2} + \frac{1}{2} m \omega^2 (\Delta x)^2
= \frac{\hbar^2}{8 m} \cdot \frac{2 m \omega}{\hbar} + \frac{1}{2} m \omega^2 \cdot \frac{\hbar}{2 m \omega} = \frac{1}{2} \hbar \omega.
$$

Thus, the ground-state energy of the quantum harmonic oscillator is

$$
E_0 = \frac{1}{2} \hbar \omega.
$$

This non-zero energy is called the zero-point energy, reflecting the fact that even in its lowest-energy state, the oscillator still exhibits quantum fluctuations. This seemingly innocent characteristic has a profound consequences since it gives rise to vacuum fluctuations. Now, the picture start to become clear from a theoretical point of view.

So we can see that by incorporating QFT, these modes that make up the vacuum give rise to vacuum energy, due to quantum fluctuations. This bold prediction is made possible by the QFT treatment. Analyzing the effect due to one mode, we combine the previous 2 equations to get: 

$$
E_{min}=\frac{\hbar\omega_k}{2}=\frac{\hbar ck}{2}
$$

 According to Maxwell equations of Electromagnetism, the energy density of a mode k is given by:
 
$$
u=\frac{\epsilon_0|\epsilon_k|^2}{2}
$$

$$\epsilon_k$$ is the root mean square amplitude of the electric field associated with k. Note that the magnetic field is not mentioned since its weaker than the electron field by a factor of c. The energy is simply the product of energy density and volume. Assuming our confining box has length a, we get:

$$
E_{vac}=ua^3=\frac{\epsilon_0|\epsilon_k|^2a^3}{2}
$$

We can, now, equate $$E_{vac}$$ with $$E_{min}$$ in a semi classical approximation to get:

$$
\frac{\epsilon_0|\epsilon_k|^2a^3}{2}=\frac{\hbar ck}{2}
$$

Though this is a semi-classical approximation, ultimately it leads to the same result. The resulting root mean square of the electric field amplitude of a mode is:

$$
|\epsilon_k|^2=\frac{\hbar ck}{\epsilon_0 a^3}
$$

So the vacuum electric field amplitude associated with mode k is given by:

$$
\epsilon_k=\sqrt{\frac{\hbar ck}{\epsilon_0 a^3}}
$$

We now observe, from the QFT perspective,  that every mode trembles with its own electric field. Note that in QFT, there are infinite amount of modes and each one contributes its own effects, in a vacuum, oblivious to the presence or absence of particles. Now the idea of empty space not being empty starts to make sense, but we are not finished. Each mode within the Hydrogen atom, influences the electron, not by much alone, but the effects add up. This also changes the probability distribution of the electron, and is something we can pick up despite its subtlety.

## The Lamb Shift

This subtle change in the electron's probability distribution leads to a shift in its energy levels, in what is referred to as "The Lamb Shift". If you bear with me a little longer, we can get into how we can quantify it for our Hydrogen atom. Let's first study the shift caused by one mode, with spatial wave-vector k and frequency $$\omega_k$$, on an electron. The force experienced by the electron due to an electric field is given by:

$$
F=m_ea=e\epsilon
$$

So the acceleration caused by a mode k is given by:

$$
a_k=\frac{e\epsilon_k}{m_e}
$$

The time period of the oscillation of mode k is given by:

$$
T_k=\frac{2\pi}{\omega_k}
$$

The time where the field pushes the electron in one direction is half of this time period (picture a pendulum):

$$
\tau=\frac{\pi}{\omega_k}=\frac{\pi}{ck}
$$

The displacement ($$s_k$$) caused due to a mode is given by:

$$
s_k=\frac{a_k\tau^2}{2}
$$

$$
s_k=\frac{e\epsilon_k\pi^2}{2m_ec^2k^2}=\frac{e\pi^2}{2m_ec^2k^2}\sqrt{\frac{\hbar ck}{\epsilon_0 a^3}}=\frac{e\pi^2}{2m_e c^2 k^{3/2}} \left( \frac{\hbar c}{\varepsilon_0 a^3} \right)^{1/2}
$$

Now we can calculate the summed up effects on displacement, due to all the modes. Since these modes are not correlated with each other, we can sum the mean square displacement. The summation takes the following form over k-space:

$$
s^2=\sum_k (s_k^2)
$$

Taking the continuum limit over k-space gives us:

$$
s^2=\sum_k (s_k^2)=\frac{a^3}{(2\pi)^3}\int_k(s_k)^2d^3k
$$

The factor $$\frac{a^3}{(2\pi)^3}$$ arises due to the density of states in k-space, which factors in for the step-size of k and allows the sum to take the form of an integral. Since we are dealing with a spherical atom, it is useful to use spherical coordinates where:

$$
d^3k=4\pi k^2dk
$$

We can now substitute in $$d^3k$$ and $$s_k$$ to give us an integral in terms of k.

$$
s^2=\frac{a^3}{(2\pi)^3}\int_k \left( \frac{e\pi^2}{2m_e c^2 k^{3/2}} \left( \frac{\hbar c}{\varepsilon_0 a^3} \right)^{1/2} \right)^2 4\pi k^2dk 
$$

Simplifying gives:

$$
s^2=\frac{\pi^2\hbar e^2}{8m^2\epsilon_0c^3}\int_k\frac{1}{k}dk
$$

If we are not careful, and integrate from zero to infinity, we could get unphysical answers. Therefore, we are going to integrate over the cut-off limits, since not all modes can interact with the electron. We introduce the IR-UV (Infrared-UltraViolet) cutoffs, since modes smaller than the IR modes are have wavelengths too high to perturb the electron and modes greater than the UV modes, have wavelengths that are too small compared to the atoms, which means that the idea of small perturbations on the electron does no longer apply. We define the cutoffs as:

$$
k_{UV}=\frac{1}{\lambda_c}, \quad k_{IR}=\frac{1}{a_0}
$$

where $$\lambda_c=\frac{\hbar}{mc}$$ is the Compton wave length which we derived earlier and $$a_0$$ is the Bohr radius. 

Which gives us the integral:

$$
s^2=\frac{\pi^2\hbar e^2}{8m^2\epsilon_0c^3}\int_{k_{UV}}^{k_{IR}}\frac{1}{k}dk
$$

Performing the integration yields:

$$
s^2=\frac{\pi^2\hbar e^2}{8m^2\epsilon_0c^3}In\left(\frac{1}{\alpha}\right)
$$

where, remarkably, $$\alpha$$ is the fine structure constant and is of the form:

$$
\alpha=\frac{e^2}{4\pi \epsilon_0\hbar c}\approx\frac{1}{137}
$$

which is the strength of the electromagnetic interaction. This constant is baked into nature and thecfact that it pops up here also, is a very encouraging sign that we are on the right track. This is the beauty of physics, where the mathematics magically leads you to the most fundamental constants in nature. The average displacement registered by the electron can be computationally derived through simulations, the details of which we will not get into in this blog, and it turns out to be:

$$
\bar{s}=\frac{s^2}{3a_0}
$$

To determine the energy shift on the Hydrogen atom, we begin by considering the potential: 

$$
V(r)=\frac{-e^2}{4\pi \epsilon_0r}
$$

Factoring in the perturbation of the electron yields, by the Taylor Expansion:

$$
V(r+s)=V(r)+s\frac{dV}{dr}+...
$$

$$
V(r+s)=V(r)+s\frac{e^2}{4\pi \epsilon_0r^2}+...
$$

The second term on the left hand side is the energy due to the perturbation, and is precisely what we are looking for. So letting $$r=a_0$$ (the most probable value of r for the ground-state Hydrogen atom) gives us:

$$
\Delta E=s\frac{e^2}{4\pi \epsilon_0a_0^2}
$$

$$
\Delta E=\frac{s^2}{3a_0}\frac{e^2}{4\pi \epsilon_0a_0^2}=\frac{e^2s^2}{12\pi \epsilon_0a_0^3}
$$

Using the $$s^2$$ relation derived earlier gives:

$$
\Delta E=\frac{e^2}{12\pi \epsilon_0a_0^3}\frac{\pi^2\hbar e^2}{8m^2\epsilon_0c^3}In\left(\frac{1}{\alpha}\right)\approx5 \times10^{-5} eV
$$

Note that every single quantity in this expression is a known constant, and so plucking in all the constants gives you a reasonable order-of-magnitude value the change in energy due to empty space not being actually empty. Although this energy is a million times smaller than the ground-state energy of Hydrogen which was stated earlier, it is a measurable change which acts as undeniable and irrefutable proof that the vacuum is far from empty: it always jitters and its fingerprints are real and measurable. So we just proved by both theory and experiment, that even empty space when quantized to a small enough scale, gives rise to fluctuations. If you constrain something to a small enough volume, the Heisenberg Uncertainty Principle allows it to acquire enough energy to produce particle-anti particle pairs. 


I hope you learned something new from today's blog, and I will be back soon with another interesting topic which is now, almost a century long mystery.

## References

W.E. Lamb Jr. & R.C. Retherford, Fine Structure of the Hydrogen Atom by a Microwave Method, Phys. Rev. 72, 241 (1947). — The original experimental discovery of the Lamb shift.

H.A. Bethe, The Electromagnetic Shift of Energy Levels, Phys. Rev. 72, 339 (1947). — The first theoretical explanation of the Lamb shift using quantum electrodynamics (QED).

R.P. Feynman, QED: The Strange Theory of Light and Matter, Princeton University Press (1985). — A lucid non-technical discussion of how quantum fluctuations and virtual photons cause effects like the Lamb shift.

J.J. Sakurai & J. Napolitano, Modern Quantum Mechanics, 2nd Edition, Addison-Wesley (2011). — Explains atomic energy levels and radiative corrections in the quantum framework.

M.E. Peskin & D.V. Schroeder, An Introduction to Quantum Field Theory, Westview Press (1995). — Covers vacuum polarization, self-energy corrections, and their connection to observable effects like the Lamb shift.

C. Cohen-Tannoudji, B. Diu & F. Laloë, Quantum Mechanics, Vol. 2, Wiley-VCH (1977). — Standard text with detailed discussion on fine structure and radiative corrections in atoms

## For the Casual Readers

https://www.youtube.com/watch?v=21XuHLJkEeg&t=1862s
