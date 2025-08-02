---
title: "Limitations of the Schrödinger Equation and the Birth of Particle Physics"
date: 2025-08-02
categories: [Cosmology, Relativistic Quantum Mechanics, Particle Physics, Relativity]
mathjax: true
layout: single
author_profile: true
read_time: true
comments: true
share: true
related: true
---

## Introduction

Welcome to this blog series where the objective is to spread science and make difficult concepts digestible. The content of this blog is for an audience familiar with basic Quantum Mechanics and concepts of matrices. I will show you that with such basic tools, one can track all the way back to the founding equation of particle physics which governs our universe. However, be advised, this blog series is not for the faint-hearted. You must take on the math

The well-known Schrödinger equation is given by:

$i\hbar \frac{\partial}{\partial t} \psi(\mathbf{r}, t) = \left[ -\frac{\hbar^2}{2m} \nabla^2 + V(\mathbf{r}, t) \right] \psi(\mathbf{r}, t)$ &nbsp; -----------(1)

This equation is a cornerstone of Quantum Mechanics. It provides accurate predictions for many atomic and molecular systems. In essence, it is an energy conservation equation which states the total energy of a particle (left-hand side of 1) is the sum of its kinetic energy (first term on the right-hand side) and potential energy (second term), in the form of quantum mechanical operators.

It is a first-order partial differential equation, which means that once the wavefunction $\psi(\mathbf{r}, t)$ is known, we can determine the evolution of the particle using:

$\Psi(\mathbf{r}, t) = \psi(\mathbf{r}, 0) e^{-\frac{iHt}{\hbar}}$ &nbsp; -----------(2)

The probability density associated with the wavefunction is given by:

$\rho(\mathbf{r}, t) = |\psi(\mathbf{r}, t)|^2$ &nbsp; -----------(3)

## The Continuity Equation for the Schrödinger Equation

Lets do a simple analysis of this equation using the continuinty equation. If you are familiar with electromagnetic theory, this equation governs how the movement of charge density influences the divergence of current density. In EMT, this equation is responsible for the conservation of charge. 

 $\frac{d}{dt}\int\rho(\mathbf{r},t)d^3x=-\int j(\mathbf{r},t)dS $

 Using the Gauss Divergence theorem:
 
 $\frac{d}{dt}\int\rho(\mathbf{r},t)d^3x=-\int \nabla.j(\mathbf{r},t)d^3x$

 Integrating over volume yields the continuity equation.
 
 $\frac{d\rho}{dt}+\nabla.j=0$

 Remarkably, the same treatment can be applied to the Schrodinger equation and conserve another crucial probability. We begin with the time-dependent Schrödinger equation:

$i\hbar \frac{\partial \psi}{\partial t} = \left(-\frac{\hbar^2}{2m} \nabla^2 + V \right)\psi$ &nbsp; -----------(4)

and taking the complex conjugate of both sides, we get:

$-i\hbar \frac{\partial \psi^\star}{\partial t} = \left(-\frac{\hbar^2}{2m} \nabla^2 + V \right)\psi^\star$ &nbsp; -----------(5)

Now multiply Eq. (4) by $\psi^\star$ and Eq. (5) by $\psi$:

$\psi^\star i\hbar \frac{\partial \psi}{\partial t} = \psi^\star \left( -\frac{\hbar^2}{2m} \nabla^2 \psi + V\psi \right)$ &nbsp; -----------(6)

$\psi (-i\hbar) \frac{\partial \psi^\star}{\partial t} = \psi \left( -\frac{\hbar^2}{2m} \nabla^2 \psi^\star + V\psi^\star \right)$ &nbsp; -----------(7)

Subtracting the two equations:

$i\hbar \left( \psi^\star \frac{\partial \psi}{\partial t} + \psi \frac{\partial \psi^\star}{\partial t} \right) = -\frac{\hbar^2}{2m} \left( \psi^\star \nabla^2 \psi - \psi \nabla^2 \psi^\star \right)$ &nbsp; -----------(8)

Note that the terms containing the potential V cancelled out. We now take $i\hbar$ on the other side, and subtracting both terms:

$\frac{\partial}{\partial t} (\psi^\star \psi) + \nabla \cdot \left[ \frac{-i\hbar}{2m} \left( \psi^\star \nabla \psi - \psi \nabla \psi^\star \right) \right] = 0$ &nbsp; ----------(8)

Recognizing the first term on the left-hand side as the time derivative of the probability density:

$\frac{\partial}{\partial t} (\psi^\star \psi) = \frac{\partial \rho}{\partial t}$ &nbsp; -----------(9)

The second left-hand side term becomes the divergence of a vector using an identity:

$\nabla \cdot \left( \frac{\hbar}{2mi} (\psi^\star \nabla \psi - \psi \nabla \psi^\star) \right)$ &nbsp; -----------(10)

Plucking (9) and (10) into (8), we obtain the continuity equation:

$\frac{\partial \rho}{\partial t} + \nabla \cdot \mathbf{j} = 0$ &nbsp; -----------(11)

Where:

$\rho = \psi^\star \psi$ &nbsp; -----------(12)

$\mathbf{j} = \frac{\hbar}{2mi} (\psi^\star \nabla \psi - \psi \nabla \psi^\star)$ &nbsp; -----------(13)

In this case, we find that the equation that was used to conserve charge in a seemingly unrelated context of EMT also applies to Quantum Mechanics to conserve probability. An important takeaway here is the fact that probability density is always positive. This is the beauty of physics, where all different scenarios are fundamentally governed by conservation mechanisms. Such mechanisms will be extensively discussed in future blogs.

For the Schrodinger equation, the positive probability density is a physically viable result since we expect probability to not be negative. But as the title suggests, this equation has its shortcomings. While it describes the dynamics accurately at low velocities, it is inherently non-relativistic. This means that it does not do a great job when applied to particles moving close to the speed of light. This stems from the fact that it arises from a classical expression. Furthermore, there is no mention of anti-particles, and spin needs to be added "by hand". Keeping these limitations in mind, lets try a relativistic treatment of this equation.

## The Klein-Gordon Equation

We begin with the relativistic energy-momentum relation:

$E^2 = p^2c^2 + m^2c^4$   -----------(14)

Now we promote energy and momentum to operators in quantum mechanics:

$E \rightarrow i\hbar \frac{\partial}{\partial t}, \quad \mathbf{p} \rightarrow -i\hbar \nabla$   -----------(15)

Applying the operators in (15) and a wavefunction $\psi$ onto (14), we get:

$(i\hbar \frac{\partial}{\partial t})^2 \psi = \left[ (-i\hbar \nabla)^2 c^2 + m^2 c^4 \right] \psi$   

This simplifies to:

$- \hbar^2 \frac{\partial^2 \psi}{\partial t^2} = \left[ -\hbar^2 c^2 \nabla^2 + m^2 c^4 \right] \psi$   

Rearranging terms gives:

$\frac{\partial^2 \psi}{\partial t^2} - c^2 \nabla^2 \psi + \left( \frac{m^2 c^4}{\hbar^2} \right) \psi = 0$ --------(16) 

This is the Klein-Gordon equation in its expanded form.

We can now write it in a more compact and relativistically manifest form:

$\left( \frac{1}{c^2} \frac{\partial^2}{\partial t^2} - \nabla^2 + \frac{m^2 c^2}{\hbar^2} \right) \psi = 0$  

This equation, developed by Oskar Klein and Walter Gordon, is Lorentz invariant and thus compatible with special relativity. However, in doing so, we have introduced other glaring issues. First of all, it is second-order in time, meaning that the wavefunction $\psi(\mathbf{r}, t)$ alone is not sufficient to determine the system's evolution. This violates a fundamental postulate of quantum mechanics, which states that the dynamics of a whole system can be determined if the wavefunction is known. But here, we require complete information about the wavefunction and its first order derivative to compute dynamics. Also, this equation does not mention spin or predict antiparticles, painting an incomplete picture. Among its most troublesome flaws is the failure to reproduce the energy levels of hydrogen and the fine-structure constant. It might, at this point, appear that I have personal issues with this equation though I assure you that is not the case. And nfortunately its problems do not stop here either, as deriving the continuity equation from the Klein-Gordon equation reveals another critical discrepancy.

## Continuity Equation for Klein-Gordon
The procedure that was applied on the Schrodinger equation will be repeated here but all important steps will be displayed so its easier to follow. 
The Klein-Gordon equation is:

$\left( \frac{1}{c^2} \frac{\partial^2}{\partial t^2} - \nabla^2 + \frac{m^2 c^2}{\hbar^2} \right) \psi = 0$

Its complex conjugate is:

$\left( \frac{1}{c^2} \frac{\partial^2}{\partial t^2} - \nabla^2 + \frac{m^2 c^2}{\hbar^2} \right) \psi^\star = 0$

Now multiply Eq. (1) by $\psi^\star$ and Eq. (2) by $\psi$, and subtract the two:

$\psi^\star \frac{\partial^2 \psi}{\partial t^2} - \psi \frac{\partial^2 \psi^\star}{\partial t^2} - c^2 \left( \psi^\star \nabla^2 \psi - \psi \nabla^2 \psi^\star \right) = 0$  

Using the product rule identities, this becomes:

$\frac{\partial}{\partial t} \left( \psi^\star \frac{\partial \psi}{\partial t} - \psi \frac{\partial \psi^\star}{\partial t} \right) + c^2 \nabla \cdot \left( \psi \nabla \psi^\star - \psi^\star \nabla \psi \right) = 0$   

To make the dimensions consistent with the continuity equation, we define the probability density and current as:

$\rho = \frac{i\hbar}{2mc^2} \left( \psi^\star \frac{\partial \psi}{\partial t} - \psi \frac{\partial \psi^\star}{\partial t} \right)$   

$\mathbf{j} = \frac{i\hbar}{2m} \left( \psi \nabla \psi^\star - \psi^\star \nabla \psi \right)$   

We now obtain the continuity equation in the usual form:

$\frac{\partial \rho}{\partial t} + \nabla \cdot \mathbf{j} = 0$  

This looks familiar — but there's a problem. The expression for $\rho$ can be negative if the second term in Eq. (5) dominates the first. That is:

$\rho < 0$ if $|\psi \frac{\partial \psi^\star}{\partial t}| > |\psi^\star \frac{\partial \psi}{\partial t}|$  

This is the case when a plane-wave solution is applied. This violates the probabilistic interpretation of quantum mechanics, because probability density must always be non-negative. So, in trying to make our equation relativistically correct, we have introduced a fatal flaw: the Klein-Gordon equation allows negative probabilities. And not to mention all the other red-flags that we associated with this equation but a negative probability density is considered blasphemy in quantum mechanics. 

What now?
---

## Dirac's Ingenious Insight 
Paul Dirac, a brilliant British physicist, tackled the problems of the Klein-Gordon equation by proposing a linear form of the energy equation:

$$E = (\alpha_x p_x + \alpha_y p_y + \alpha_z p_z)c + \beta mc^2$$

Now, squaring both sides:

$$E^2 = \left((\alpha_x p_x + \alpha_y p_y + \alpha_z p_z)c + \beta mc^2\right)^2$$

Expanding the square:

$$
\begin{aligned}
E^2 &= \alpha_x^2 p_x^2 c^2 + \alpha_y^2 p_y^2 c^2 + \alpha_z^2 p_z^2 c^2 + \beta^2 m^2 c^4 \\
&\quad + (\alpha_x \alpha_y + \alpha_y \alpha_x) p_x p_y c^2 + (\alpha_x \alpha_z + \alpha_z \alpha_x) p_x p_z c^2 \\
&\quad + (\alpha_y \alpha_z + \alpha_z \alpha_y) p_y p_z c^2 + (\alpha_x \beta + \beta \alpha_x) p_x m c^3 \\
&\quad + (\alpha_y \beta + \beta \alpha_y) p_y m c^3 + (\alpha_z \beta + \beta \alpha_z) p_z m c^3
\end{aligned}
$$


In order for this expression to reduce to the relativistic energy relation $E^2 = p^2 c^2 + m^2 c^4$, a number of constraints must be satisfied as the last 6 terms must vanish.
Dirac imposed the following constraints:

$$ \alpha_x^2 = \alpha_y^2 = \alpha_z^2 = 1 $$, $$ \beta^2 = 1 $$

$$ \alpha_i \alpha_j + \alpha_j \alpha_i = 0 $$ 

$$ \alpha_i \beta + \beta \alpha_i = 0 $$ 

These can be summarized compactly:

$$ \alpha_i \alpha_j + \alpha_j \alpha_i = 0 \quad \text{(17)}$$ 

$$ \alpha_i \beta + \beta \alpha_i = 0 \quad \text{(18)}$$ 

$$
\alpha_i^2 = 1 \quad \text{(19)}
$$

$$
\beta^2 = 1 \quad \text{(20)}
$$

There began the race to find a quantity that would satisfy (17)-(20)

### Why Scalars Won’t Work

Assume $\alpha$ is a scalar. Then (17) implies:

$$
\alpha_i \alpha_j = -\alpha_j \alpha_i
$$

This can only be true if either $\alpha_i = 0$ or $\alpha_j = 0$, which contradicts (19). So $\alpha$ cannot be a scalar.

### The Pauli Matrix Attempt

This was where Dirac's genius had begun to shine. Normally, one would conclude this to be a dead route since no number satisfies all constraints at once. The Pauli matrices were then tried. Although Dirac claimed to have derived these himself, it is not consensus as these matrices are usually associated with Wolfgang Pauli, another prominent physicist of that time.
A famous property of these matrices is that they satisfy:

$$ \sigma_i \sigma_j + \sigma_j \sigma_i = 0 $$ 
for $$ i \ne j $$
and 
$$ \sigma_i^2 = \mathbb{I} $$

So (17) and (19) are satisfied.
We begin with the Pauli matrices:

$$
\sigma_x = \begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix}, \quad
\sigma_y = \begin{bmatrix}
0 & -i \\
i & 0
\end{bmatrix}, \quad
\sigma_z = \begin{bmatrix}
1 & 0 \\
0 & -1
\end{bmatrix}
$$

Assume a general $2 \times 2$ matrix for $\beta$:

$$
\beta = \begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
$$

Applying the anti-commutation relation with $\sigma_x$:

$$
\sigma_x \beta + \beta \sigma_x =
\begin{bmatrix}
c + b & d + a \\
a + d & b + c
\end{bmatrix} = 0
$$

This implies:

$$
c = -b, \quad d = -a
$$

So $\beta$ becomes:

$$
\beta = \begin{bmatrix}
a & b \\
-b & -a
\end{bmatrix}
$$

Now test this against $\sigma_y$:

$$
\sigma_y \beta + \beta \sigma_y =
\begin{bmatrix}
2ib & 0 \\
0 & 2ib
\end{bmatrix} = 0 \Rightarrow b = 0
$$

Thus:

$$
\beta = \begin{bmatrix}
a & 0 \\
0 & -a
\end{bmatrix}
$$

Now test this $\beta$ against $\sigma_z$:

$$
\sigma_z \beta + \beta \sigma_z =
\begin{bmatrix}
2a & 0 \\
0 & 2a
\end{bmatrix} = 0 \Rightarrow a = 0
$$

So finally:

$$
\beta = \begin{bmatrix}
0 & 0 \\
0 & 0
\end{bmatrix}
$$

This is the **null matrix**, which violates the constraint $\beta^2 = 1$. Hence, **no $2 \times 2$ matrix can satisfy all of Dirac's anticommutation relations**. A higher-dimensional structure is necessary.

## 4×4 Matrix Solution to the Dirac Equation

So there is, once again, a violation of the constraints. It would be natural for someone to give up by now but not this guys. Matter of fact, he doubled down. Literally. He went one step further and imagined the matrices $\alpha$ to be $4 \times 4$ matrices, posed as block forms made of $2 \times 2$ matrices. 

The form is as follows:

$$
\alpha_x = \begin{bmatrix}
0 & 0 & 0 & 1 \\
0 & 0 & 1 & 0 \\
0 & 1 & 0 & 0 \\
1 & 0 & 0 & 0
\end{bmatrix}
$$

$$
\alpha_y = \begin{bmatrix}
0 & 0 & 0 & -i \\
0 & 0 & i & 0 \\
0 & -i & 0 & 0 \\
i & 0 & 0 & 0
\end{bmatrix}
$$

$$
\alpha_z = \begin{bmatrix}
0 & 0 & 1 & 0 \\
0 & 0 & 0 & -1 \\
1 & 0 & 0 & 0 \\
0 & -1 & 0 & 0
\end{bmatrix}
$$

The beauty of this formalism lies in the fact that all the previous constraints are still satisfied. The only difference is that instead of $2 \times 2$ matrices of scalars, we now use $4 \times 4$ matrices made from $2 \times 2$ matrix blocks.
Let’s test the anticommutation relation between $\alpha_x$ and $\alpha_y$:


$$
\alpha_x \alpha_y + \alpha_y \alpha_x =
\begin{bmatrix}
\sigma_x \sigma_y + \sigma_y \sigma_x & 0 \\
0 & \sigma_x \sigma_y + \sigma_y \sigma_x
\end{bmatrix}=
\begin{bmatrix}
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0
\end{bmatrix}
$$

Now for $\alpha_x^2$:

$$\alpha_x^2 =
\begin{bmatrix}
\sigma_x^2 & 0 \\
0 & \sigma_x^2
\end{bmatrix}=
\begin{bmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1
\end{bmatrix}
$$

The same applies to $\alpha_y^2$ and $\alpha_z^2$, confirming:
- $\alpha_i \alpha_j + \alpha_j \alpha_i = 0$ for $i \ne j$
- $\alpha_i^2 = \mathbb{I}$



Let $\beta$ be:

$$
\beta =
\begin{bmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & -1 & 0 \\
0 & 0 & 0 & -1
\end{bmatrix}
$$

This satisfies:

$$
\beta^2 =
\begin{bmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1
\end{bmatrix}
= \mathbb{I}_{4 \times 4}
$$

Now check the anticommutation between $\alpha_x$ and $\beta$:

$$
\alpha_x \beta + \beta \alpha_x =
\begin{bmatrix}
0 & \sigma_x \\
\sigma_x & 0
\end{bmatrix}
\begin{bmatrix}
\mathbb{I} & 0 \\
0 & -\mathbb{I}
\end{bmatrix}
+
\begin{bmatrix}
\mathbb{I} & 0 \\
0 & -\mathbb{I}
\end{bmatrix}
\begin{bmatrix}
0 & \sigma_x \\
\sigma_x & 0
\end{bmatrix}=
\begin{bmatrix}
0 & -\sigma_x \\
\sigma_x & 0
\end{bmatrix}
+
\begin{bmatrix}
0 & \sigma_x \\
-\sigma_x & 0
\end{bmatrix}=
\begin{bmatrix}
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0
\end{bmatrix}
$$

Hence, all of Dirac's constraints are satisfied. This confirms that $4 \times 4$ matrices are the minimal representation that preserves both Lorentz invariance and compatibility with quantum mechanics.




Let $\beta$ be:

$$
\beta =
\begin{bmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & -1 & 0 \\
0 & 0 & 0 & -1
\end{bmatrix}
$$

This choice satisfies the condition:

$$
\beta^2 =
\begin{bmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1
\end{bmatrix}
$$

Now check the anticommutation relation between $\alpha_x$ and $\beta$:

$$
\alpha_x \beta + \beta \alpha_x =
\begin{bmatrix}
0 & \sigma_x \\
\sigma_x & 0
\end{bmatrix}
\begin{bmatrix}
1 & 0 \\
0 & -1
\end{bmatrix}
+
\begin{bmatrix}
1 & 0 \\
0 & -1
\end{bmatrix}
\begin{bmatrix}
0 & \sigma_x \\
\sigma_x & 0
\end{bmatrix}=
\begin{bmatrix}
0 & -\sigma_x \\
\sigma_x & 0
\end{bmatrix}
+
\begin{bmatrix}
0 & \sigma_x \\
-\sigma_x & 0
\end{bmatrix}=
\begin{bmatrix}
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0
\end{bmatrix}
$$

Thus, this construction satisfies all of Dirac’s constraints, confirming that $4 \times 4$ matrices are the minimal representation necessary to maintain compatibility with both quantum mechanics and special relativity. This derivation was long, but it involved the most simple matrix algebra that I hope you were able follow.

## Operator Form of the Dirac Equation

Now that we have attained equations that satisfy all constraints simultaneously, let's go back to the earlier form of the energy equation.

Energy was written as a linear combination of momentum. Now apply the momentum and energy operators to a wavefunction $\psi$ so

$$
E \psi = (\alpha_x p_x + \alpha_y p_y + \alpha_z p_z)c \psi + \beta m c^2 \psi
$$

becomes:

$$
i\hbar \frac{\partial \psi}{\partial t} = -i\hbar c \left( \alpha_x \frac{\partial \psi}{\partial x} + \alpha_y \frac{\partial \psi}{\partial y} + \alpha_z \frac{\partial \psi}{\partial z} \right) + \beta m c^2 \psi
$$

---

## Covariant Form of the Dirac Equation

We have obtained the time-dependent Dirac equation, but this form is not readily found in textbooks. To simplify, we assume **natural units** where $\hbar = c = 1$.

Defining the gamma matrices as:

$$
\gamma^0 = \beta, \quad \gamma^i = \beta \alpha_i \quad (i = x, y, z)
$$

Also defining the spacetime 4-gradient (which is a fancy way of saying that we are account for all dimensions, the 3 of space and 1 of time):

$$
\partial_\mu = \left( \frac{1}{c} \frac{\partial}{\partial t}, -\nabla \right), \quad
\text{and } \gamma^\mu = (\gamma^0, \gamma^1, \gamma^2, \gamma^3)
$$

This allows us to write the Dirac equation more compactly:

$$
\left( i\hbar \sum_{\mu = 0}^3 \gamma^\mu \partial_\mu - m c \right) \psi = 0
$$

Using the **Einstein summation convention**, we drop the summation symbol:

$$
\boxed{(i\hbar \gamma^\mu \partial_\mu - m c)\psi = 0}
$$

which gives us the Dirac equation in its most minimal and elegant form. This equation solved everything as it was relativistically correct and therefore computes the energy levels of the Hyfrogen atom better than the Schrodinger equation. It introduces no negative probability density anomalies and remarkably also predicts spin states and anti-particles. Since the derivative is a 4-vector so must be the wavefunction. Its four components allows for the elegant inclusion of both the spin states of, both, the particle and its anti-particle counterpart. .I can go on with details since this is just the beginning of particle physics, but lets leave the Dirac wavefunction for another blog. This remains, to date, the most complete equation in all of quantum mechanics. Remarkably, the equation remains obscure to many due to the mathematical complexity involved. This elegant formalism allows interpretation of negative energy solutions as antiparticles, which were later explained by **Richard Feynman** as normal particles traveling **back in time**. BUT, the shortcomings never end...


## The Strong Force Problem

The Dirac equation still fails to account for the **strong interaction**, the binding force at the core of the atomic nucleus. This challenge lies at the heart of **nuclear physics**. The difficulty is embedded in the **fine-structure constant**:

$$
\alpha = \frac{\alpha_{\text{EM}}}{\alpha_{\text{SF}}} = \frac{e^2}{4\pi \epsilon_0 \hbar c} \approx \frac{1}{137}
$$

At low energies, the strong force coupling becomes dangerously close to 1. This presents a major issue for **perturbative methods**, which expand physical quantities as power series in the coupling constant.

The general perturbative series looks like:

$$
A(\alpha) = \sum_{i=0}^n \alpha^i A^{(i)} = A^{(0)} + \alpha A^{(1)} + \alpha^2 A^{(2)} + \cdots + \alpha^n A^{(n)}
$$
When $\alpha \geq 1$, the series diverges, rendering all of our known analytical treatments as useless. So the next time you are part of nuclear physics lecture, know that every single potential and equation that invloves the strong nuclear force is an approximation that fits experiments and has not be analytically derived. 
And who knows, maybe if you can figure out a way to solve problems the same way Dirac did, you might be able to figure this out. At that point, you would have a realistic shot of being nominated as a Noble Prize laureate. 

Thank you for making it this far, and as always, keep on physicsing. 


