---
title: "Inside the Atom: Where ‘Empty Space’ Teems with Activity"
date: 2025-08-16
categories: [Quantum Field Theory, Relativistic Quantum Mechanics, Particle Physics, Atomic and Molecular Physics]
use_math: true
layout: single
author_profile: true
read_time: true
comments: true
share: true
related: true
excerpt: "A subtle shift in hydrogen’s energy levels cracked open the door to quantum field theory which revealed the dynamic, buzzing vacuum inside every atom."
---

## Introduction
Today we set out to unravel one of the most counterintuitive facts in all of physics: that *empty space is not empty at all*. What we casually refer to as “nothing” is, in reality, a restless arena of quantum activity and fluctuations. These are not just speculative ideas born in abstract theory but have very real and measurable consequences. One of those consequences is the subject of this post, and as we work our way into it you will see that even a simple hydrogen atom becomes a window into the deepest layers of reality. You will need knowledge on introductory Modern Physics and Quantum Mechanics.

   Our understanding of the atom was a hot topic for physicists in the early 1900s, with J.J Thompsons famous "fruitcake" model, where the atom was assumed to be a smooth and filled sphere of positive charge, with clumps of negative charges embedded in it. In 1911, Earnest Rutherford devised the most accurate atomic model known to man, backed by an experiment, where a minority of alpha particles were observed to scatter off at large angles when targeted at a thin foil of gold. This showed that an atom was mostly empty space with a lot of its mass being concentrated at the center, leading to such dramatic scattering. This center with positive charge is known as a nucleus, with much lighter negative electrons orbiting around it. 

## The Empty Space Inside the Atom

  Now that we objectively know that most of the atom is empty space, lets make estimations to quantify this emptiness. The Rutherford model predicts the radius of the atom to be of the order $$r_a \approx 10^{-10}m$$ and of the nucleus to be $$r_n \approx 10^{-15}m$$. Comparing the ratio of their volumes:
  
$$
\frac{\frac{4 \pi (r_a)^3}{3}}{\frac{4 \pi (r_n)^3}{3}}=\frac{r_a^3}{r_n^3} \approx (\frac{10^{-10}}{10^{-15}})^3 m\approx 10^{15}m
$$

This tell us that the atom is almost completely empty. To  give you an idea of the magnitude of this ratio, its like if the atom was the size of a football field, the nucleus would be a cherry placed in its center. Now, lets dive into the deep end. If I claimed that there is no such thing as empty space, that what is actually going on in that space?

To understand this, we will view the atom from the lens of Quantum Field Thoery (QFT).

## The Behaviour of the Electrons

   In the classical treatment of the atom, the electrons should spiral into the nucleus while radiating energy and ultimately the atom should collapse in picoseconds assuming that it is purely a particle. However, in the quantum mechanical treatment, it is assumed to be a wave, in the sense that all of its information is inscribed in its wavefunction $\psi$, which can be computed by solving the Schrodinger equation:
   
$$
\left[-\frac{\hbar^2}{2m} \nabla^2 - \frac{e^2}{4\pi \varepsilon_0 r} \right] \psi = E \psi
$$

This $$\psi$$ acts like a probability that is distributed throughout empty space, which do not locate the electron exactly, but rather give the probability of where we are likely to find it. As it turns out, the resulting $\psi$ leads to discrete energy levels which keep the atom stable, and the electrons energy constant, with different energies corresponding to different shells. While all this points to the fact that empty space is not truly empty due to a probability being smeared all across it, the real game-changer is the addition of special relativity and relativistic quantum mechanics. 

## Particles in a Contracting Box

One can intuitively picture the atom as a small sphere, which contrains the particles confined within it. To understand the dominance of quantum effects, let's analyze the example of a particle in a contracting box.  The Heisenberg Uncertainty Principle says that the smaller the uncertainty in position, the larger the uncertainty in momentum and vice versa. 

$$
\Delta p \Delta x \geq \frac{\hbar}{2}
$$

So if an electron is constrained to a small enough space, relativistic effects become dominant. In such a case, the energy is given by: 

$$
E=\Delta pc=mc^2
$$

$$
\frac{\hbar c}{2\Delta x}=mc^2
$$

$$
\Delta x=\frac{\hbar}{2m_ec} \approx 10^{-12}m
$$

It becomes apparent that this length is bigger than the radius of the nucleus but smaller then that of the atom, hence making the "empty" space inside the atom an ideal environment for effects to occur. So, we have seen that in the case of an atom, the electron can be confined to a region where the quantum mechanical picture becomes fuzzy. Beyond this, ordinary quantum mechanics breaks down, and we require another way to understand the atom. This is where Quantum Field Theory (QFT) can play a part, but do not be overwhelmed by the fancy name...it is a lot more simple than it sounds. In the QFT interpretation, fields are fundamental, not particles. Particles are simply localized excitation in fields that permeate through space. Using QFT allows us to study the atom from a field perspective, which aids in making sense of the situation. In order to detect the consequences of the restless empty space on atomic energies, we need to determine a consequence of these quantum effects. To detect QFT's effects, we first need to establish what happens without them. 

## The Picture Without QFT

Let's pick the simplest case here: the ground state Hydrogen atom, with an electron orbiting a proton. The well known ground state energy of the Hydrogen atom is given by solving the Schrodinger equation mentioned earlier , and turns out to be:

$$
E = -\frac{1}{2} \cdot \frac{m_e e^4}{(4\pi \varepsilon_0)^2 \hbar^2}=-13.6 eV
$$

The full derivation of this is the topic for another blog, but for now, trust me on this. Note that this is the picture without QFT, since the Schrodinger equation is non-relatvistic, as explained in the first blog of this series. For the confined particle, if we take the assumption that $$\psi$$ vanishes at the edges, the allowed wavelengths are given by: 

$$
\lambda_n=\frac{2L}{n}
$$

The edges (where probability disappears) are called modes, which have distinct spatial and temporal frequencies. n is an integer value and L is the length of the constraining box. The wavenumber k (spatial frequency) is given by $$k=\frac{2 \pi}{\lambda}$$, which results in: 

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


