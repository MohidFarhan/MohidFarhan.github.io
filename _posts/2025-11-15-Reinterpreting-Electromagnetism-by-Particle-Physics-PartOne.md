---

title: "Blog 8—Walking through the Birth of Electromagnetism from Gauge Theory: Part 1"
date: 2025-11-15
categories: [Particle Physics, Electromagnetism, Gauge Theory, Atomic and Molecular Physics, Fundamental Forces]
use_math: true
layout: single
author_profile: true
read_time: true
comments: true
excerpt: "Every law ever formulated in Electromagnetism arises naturally from Gauge theory, with Gauge theory rooted in Particle Physics. Let's dive into how Electromagnetism is a consequence of a seemingly unrelated symmetry."


---

## Introduction

In this blog, we will continue from where we left off, in the very first blog post: The Dirac equation, where the reader can visit blog 1 to learn more about it. Today, we are not going to go through the derivation but, instead, review some of its interesting emergent implications. This is intended to be the first part of a mini series on particle physics. 

We have already seen that the Dirac equation kills multiple birds with one stone, as not only is it relativistically correct, but also incorporates inherent properties like spin and antiparticles. This cements its status in particle physics as a founding equation. We did not get into too much details when interpreting its results so let's dive in.

## Revisiting the Dirac Equation

The Dirac equation can be elegantly written as: 

$$
\left( i \hbar \gamma^\mu \partial_\mu - mc \right) \psi = 0 ,
$$

where $$\gamma^\mu$$ are the gamma matrices,
$$\partial_\mu = \frac{\partial}{\partial x^\mu}$$ is the four-gradient, m is the mass of the particle, and $$\psi$$ is the Dirac spinor field. The gamma matrices are written as:

$$
\gamma^0 =
\begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & -1 & 0 \\
0 & 0 & 0 & -1
\end{pmatrix},
$$

$$
\gamma^1 =
\begin{pmatrix}
0 & 0 & 0 & 1 \\
0 & 0 & 1 & 0 \\
0 & -1 & 0 & 0 \\
-1 & 0 & 0 & 0
\end{pmatrix}, \quad
\gamma^2 =
\begin{pmatrix}
0 & 0 & 0 & -i \\
0 & 0 & i & 0 \\
0 & i & 0 & 0 \\
-i & 0 & 0 & 0
\end{pmatrix}, \quad
\gamma^3 =
\begin{pmatrix}
0 & 0 & 1 & 0 \\
0 & 0 & 0 & -1 \\
-1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0
\end{pmatrix}.
$$

### Zero-momentum solution
The four-gradient is written as:
 $$\partial_\mu = \frac{\partial}{\partial x^\mu}=[\frac{1}{c} \frac{\partial}{\partial t},  \frac{\partial}{\partial x}, \frac{\partial}{\partial y}, \frac{\partial}{\partial z}]$$.
 So, it accounts for all of the 4 dimensions of spacetime, which we have already tackled. Since the Dirac equation has $$4\times4$$ matrices with a 4-gradient, then the wavefunction $\psi$ also needs to be a matrix with 4 rows, in order to be dimensionally consistent.
 
$$
\psi =
\begin{pmatrix}
\psi_1 \\
\psi_2\\
\psi_3 \\
\psi_4 
\end{pmatrix}
$$

This particular form of the wavefunction is called a Dirac spinor, which we will get into.

After performing the multiplication, and utilizing the notation, the Dirac equation takes the form:

$$
i \hbar \gamma^0 \frac{1}{c} \frac{\partial}{\partial t}\psi + i \hbar \gamma^1 \frac{\partial}{\partial x}\psi + i \hbar \gamma^2 \frac{\partial}{\partial y}\psi + i \hbar \gamma^3 \frac{\partial}{\partial z}\psi - mc  \psi = 0.
$$

which can be rearranged to:

$$
 \gamma^0 \frac{1}{c} \frac{\partial}{\partial t}\psi + \gamma^1 \frac{\partial}{\partial x}\psi +\gamma^2 \frac{\partial}{\partial y}\psi + \gamma^3 \frac{\partial}{\partial z}\psi
 = - \frac{imc}{\hbar}  \psi.
$$

Now, let's assume a free particle with precisely zero momentum since it is, by far, the simplest solution. The first derivatives of $\psi$ with respect to the spatial coordinates go to zero since for $$p=0$$, we have:
$$\hat{p}\psi=-i\hbar\nabla\psi=0$$
therefore,

$$
\frac{\partial \psi}{\partial x}
= \frac{\partial \psi}{\partial y}
= \frac{\partial \psi}{\partial z}=0
$$

This cancels 3 terms and reduces the Dirac equation.

$$ 
\frac{\gamma^0}{c} \frac{\partial \psi}{\partial t}=- \frac{imc}{\hbar}  \psi
$$  

$$
\begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & -1 & 0 \\
0 & 0 & 0 & -1
\end{pmatrix} \begin{pmatrix}
\frac{\partial\psi_1}{\partial t}\\
\frac{\partial\psi_2}{\partial t}\\
\frac{\partial\psi_3}{\partial t}\\
\frac{\partial\psi_4}{\partial t}
\end{pmatrix}= - \frac{imc^2}{\hbar} \begin{pmatrix}
\psi_1 \\
\psi_2\\
\psi_3 \\
\psi_4 
\end{pmatrix}, 
$$

We absorb $\gamma^0$, the equation is split into 2 parts.

$$
\begin{pmatrix}
\frac{\partial\psi_1}{\partial t}\\
\frac{\partial\psi_2}{\partial t}\\
\end{pmatrix}=- \frac{imc^2}{\hbar} \begin{pmatrix}
\psi_1 \\
\psi_2\\
\end{pmatrix}, \quad \begin{pmatrix}
\frac{\partial\psi_1}{\partial t}\\
\frac{\partial\psi_2}{\partial t}\\
\end{pmatrix}= \frac{imc^2}{\hbar} \begin{pmatrix}
\psi_1 \\
\psi_2\\
\end{pmatrix}
$$

Solving the first-order partial differential equation for $\psi$ gives us:

$$
\begin{pmatrix}
\psi_1(t)\\
\psi_2(t)\\
\end{pmatrix} = \begin{pmatrix}
\psi_1(0)\\
\psi_2(0)\\
\end{pmatrix}
\exp\!\Big(-\frac{i m c^2}{\hbar}t\Big), \quad
\begin{pmatrix}
\psi_3(t)\\
\psi_4(t)
\end{pmatrix}=
\begin{pmatrix}
\psi_3(0)\\
\psi_4(0)
\end{pmatrix}
e^{\Big(+\frac{i m c^2}{\hbar}t\Big)}.
$$

Recombining into the full Dirac spinor, we the time-evolved form of the Dirac spinor:

$$
\psi(t)=
\begin{pmatrix}
\psi_1(0)e^{-i m c^2 t/\hbar}\\
\psi_2(0)e^{-i m c^2 t/\hbar}\\
\psi_3(0)e^{+i m c^2 t/\hbar}\\
\psi_4(0)e^{+i m c^2 t/\hbar}
\end{pmatrix}.
$$

## Splitting the Dirac Spinor

This recombined form looks nice mathematically, but fails to encapsulate a crucial subtlety. For us to not miss that subtlely, we need to keep the top 2 components (positive energy solutions) separated from the bottom 2 (negative energy solutions). Let's start with the positive energy solution, which can be written as:

$$
\psi=\begin{pmatrix}
\psi_1(0)e^{-i m c^2 t/\hbar}\\
\psi_2(0)e^{-i m c^2 t/\hbar}\\
0\\
0
\end{pmatrix}=\begin{pmatrix}
\psi_1(0)\\
\psi_2(0)\\
0\\
0
\end{pmatrix}e^{-i m c^2 t/\hbar}
$$


So, this 2-component wavefunction (also referred to as a Dirac bi-spinor) is the product of two states, $\psi_1(0)$ and $\psi_2(0)$ and an exponent. Dirac, very diligently, reimagined the states as spin-states, and the exponent as an indication of the "type" of matter. We will get into the latter later, but as for the spin-states, it makes perfect sense when you realize that normalization requires:
 
$$
|\psi_1(0)|^2+|\psi_2(0)|^2=1
$$

If you ever took a quantum mechanics course, you will instantly be able to connect the dots by using this equation: $\psi_1(0)$ shows the spin-up state and $\psi_2(0)$ shows the spin-down state. The normalization condition ensures that the overall probability sums up to give 1, which as mentioned in blog 1  is hyper-important. The superposition of spin-up and spin-down in this case is written as:

$$
 \begin{pmatrix}
\psi_1(0)\\
\psi_2(0)
\end{pmatrix}=\psi_1(0)\begin{pmatrix}
1\\
0
\end{pmatrix}+\psi_2(0)\begin{pmatrix}
0\\
1
\end{pmatrix}
$$

So the probability of the free particle being measured spin-up and spin-down is given by taking the absolute square of $\psi_1(0)$ and $\psi_2(0)$, respectively. 
So, the positive energy solution component of the Dirac spinor, written as:

$$
\begin{pmatrix}
\psi_1(t)\\
\psi_2(t)
\end{pmatrix}=
\begin{pmatrix}
\psi_1(0)\\
\psi_2(0)
\end{pmatrix}
e^{\frac{-i m c^2}{\hbar}t}
$$

can be expanded to make sense of the spin-states:
 
$$
\begin{pmatrix}
\psi_1(t)\\
\psi_2(t)
\end{pmatrix}=
\begin{pmatrix}
\psi_1(0)\begin{pmatrix}
1\\
0
\end{pmatrix}+\psi_2(0)\begin{pmatrix}
0\\
1
\end{pmatrix}
\end{pmatrix}
e^{\frac{-i m c^2}{\hbar}t}
$$

Exactly the same exercise can be repeated for the bottom two components, which would give us the counterpart of the previous equation as:

$$
\begin{pmatrix}
\psi_3(t)\\
\psi_4(t)
\end{pmatrix}=
\begin{pmatrix}
\psi_3(0)\begin{pmatrix}
1\\
0
\end{pmatrix}+\psi_4(0)\begin{pmatrix}
0\\
1
\end{pmatrix}
\end{pmatrix}
e^{\frac{i m c^2}{\hbar}t}
$$
 
     
The spin-up and spin-down states are now associated with $\psi_3(0)$ and $\psi_4(0)$, and the exponent now has a positive sign. The sign of the exponent gives an indication of the nature of energy solutions. When one tries to extract the corresponding energy of a wavefunction containing a negative exponent, we get positive energy solutions, and vice versa. 

So, the previous equation shows us a bi-spinor containing wavefunctions with negative energies. That sounds unphysical and if it were up to us normal people, we would have removed these terms after branding them so. But Dirac saw through the subtlety and predicted an actual family of particles that actually yield negative energies called antiparticles. After experimental confirmation, their existence was confirmed.

It also now makes sense to interpret antiparticles as particles going back in time. Think of it like this. If an electron was placed in between 2 oppositely charged plates, it would accelerate to the positively charge plate, and so if you take snapshots of the electron you would see it barrel into the positive plate, getting closer and closer to it. Now, if a hypothetical particle with the exact same properties as the electron, just with the opposite charge was placed right on the positive plate, it would follow the path of electron, but reversed. So it's like an electron going back in time.

In quantum field theory, the charge operator does exactly this: it converts a particle to its antiparticle by reversing its charge. 

<!-- The Famous Feynman Interpretation of antiparticles -->
<p align="center">
  <img src="/assets/images/Adobe Express - B8A1.gif" width="500" alt="The Cosmological Redshift"/>
  <br><em>Simulation 1: The famous Feynman interpretation of antimatter as matter traveling back in time.</em>
</p>

$$
\hat{C}\psi=\bar{\psi}
$$

We will discuss the QFT operators in great detail in a future work once my findings are published. But, what we have found is that the concept of negative energy solutions are actually physically sound due to this charge symmetry. Going back to our bi-spinors, the top one represents a free electron with zero momentum and the bottom one represent a free positron with zero momentum. Now that the subtlety has been caught and identified, we can combine them elegantly to retain the Dirac spinor equation, but we now see the full picture.

$$
\psi(t)=
\begin{pmatrix}
\psi_1(0)e^{-i m c^2 t/\hbar}\\
\psi_2(0)e^{-i m c^2 t/\hbar}\\
\psi_3(0)e^{+i m c^2 t/\hbar}\\
\psi_4(0)e^{+i m c^2 t/\hbar}
\end{pmatrix}.
$$

## Why is it called a Spinor?

The complex exponent always shows rotation. A complex exponent $$e^{i \theta}$$ being applied to vector $$\arrow{V}$$, rotates it by angle $$\theta$$. In the case of the Dirac spinor, the complex exponent is a function of time, meaning that as time goes on, the initial spin-state vector ($$\psi_n(0)$$) spins continuously along the complex plane, with frequency $$\frac{mc^2}{\hbar}$$, and so it's a "$$\textbf{spin}$$or". When the sign is inverted (charge operator is applied), the spin-state vector rotates in the opposite direction, or can be reinterpret as the former example moving back in time.

## Interpreting matter type using the complex plane

<!-- The Famous Feynman Interpretation of antiparticles -->
<p align="center">
  <img src="/assets/images/Adobe Express - B8A2.gif" width="500" alt="The Cosmological Redshift"/>
  <br><em>Simulation 2: The essence of a spinor, which is a rapidly spinning entity in the complex plane. As implied, anti-clockwise rotations (antimatter) can be interpret as clockwise rotations (matter) going back in time.</em>
</p>

## Interpreting spin configuration using flagpoles

<!-- The Famous Feynman Interpretation of antiparticles -->
<p align="center">
  <img src="/assets/images/Adobe Express - B8P3.gif" width="500" alt="The Cosmological Redshift"/>
  <br><em>Simulation 3: The flag poles show spin configurations. Here the two basis states are shown. These basis can mix in any proportion to give any spin configuration.</em>
</p>

## Interpreting all components of the Dirac Spinor

<!-- The Famous Feynman Interpretation of antiparticles -->
<p align="center">
  <img src="/assets/images/Adobe Express - DiracSpinorFlags.gif" width="500" alt="The Cosmological Redshift"/>
  <br><em>Simulation 4: Leveraging the flagpoles analogy to visualize all 4 components of a dirac spinor in a complex plane. Simulation 3 shows that the poles give insights about the spin configuration and here it is shown that the flag rotation distinguishes matter from antimatter. Therefore, this powerful analogy helps us to visualize all components of a Dirac Spinor.</em>
</p>

So, this was just a refresher on the implications of the Dirac equation. In part 2, we will dive into the Lagrangian of this Dirac field and play with it for a bit. Until then, keep on physicsing
