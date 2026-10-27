---
series: "LDS-SF Paper"
title: "Blog 20—The S<sub>8</sub> Tension: Why Suppressing Growth Is the Answer"
date: "2026-10-25"
categories: [Cosmology, Dark Matter, Structure Formation, S8 Tension]
layout: post
math: true
comments: true
excerpt: "The Planck satellite and the weak-lensing surveys KiDS and DES disagree about how lumpy the universe is today. This is the S8 tension. Before I can tell you how my first paper tries to fix it, we need to understand exactly what S8 measures, why the disagreement survives so many years of scrutiny, and why suppressing structure growth at small scales is likely the only fix that doesn't break the Cosmic Microwave Background (CMB)."
---

## Introduction

In the last three blogs, we built the machinery of cosmological perturbation theory. We derived the continuity equation for cold dark matter, then Euler's equation, then the equations governing dark energy perturbations. It was a long road, and by the end of it you might reasonably have asked: what is all of this *for*?

This series is the answer. You are reading the first entry of a new arc, one that walks through my very first publication, from the problem it was written to solve all the way down to the benchmark points that resolve it. The paper is titled *Layered dark structure with a structuring field: a $$Z_4$$-symmetric inert doublet-singlet realization and implications for the $$S_8$$ tension*, and was published in *Physica Scripta* in March of 2026. If you have followed this blog from the beginning, you already have the tools to read it. If you haven't, I will try to make this series as self-contained as possible.

But before we can talk about the solution, we need to understand the problem. And the problem is one of the most stubborn cracks in modern cosmology, wearing a deceptively simple name: The $$S_8$$ tension.

## The standard story and the crack in it

Modern cosmology rests on a model called $$\Lambda$$CDM. It has only six free parameters, and it fits an absurd amount of data, spanning from the cosmic microwave background, the expansion history, and the abundances of light elements to the large-scale distribution of galaxies, to remarkable precision. If you are new to this blog, I introduced this picture in Blog 3 and Blog 4: a universe dominated by dark matter and dark energy, seeded by quantum fluctuations, growing into structure under gravity.

The story is clean. In $$\Lambda$$CDM, we can *predict* how matter clumps together as a function of scale and time. Quantum fluctuations are stretched across the sky during inflation, they enter the horizon at different epochs, they grow under gravity, and they eventually collapse into the galaxies and clusters we observe. Every step of this process is calculable and this is exactly what we spent the last arc learning to do.

And here is the remarkable thing: the theory makes a *specific* prediction for how lumpy the universe should be today. It's simply a number with error bars, derived from the same six parameters that fit the CMB.

The prediction is called $$\sigma_8$$: the root-mean-square amplitude of matter density fluctuations, smoothed over spheres of radius $$8\,h^{-1}$$ Mpc. It tells you: if you drop a sphere of radius $$8\,h^{-1}$$ Mpc anywhere in the universe, on average how much does the matter density inside it deviate from the cosmic mean?

In $$\Lambda$$CDM, calibrated to Planck, the answer is about $$0.81$$. Give or take very little, depending on exactly which parameters you marginalize over. This appears to be a simple prediction, but this is where the trouble begins.

## The tension

Starting in the mid-2010s, a series of weak-lensing surveys began to measure the cosmic shear signal with increasing precision: first the Canada-France-Hawaii Telescope Lensing Survey, then the Kilo-Degree Survey (KiDS), then the Dark Energy Survey (DES). Unlike most of their predecessors, they are not CMB experiments. They look at how the light from millions of distant galaxies is distorted by the gravitational lensing of foreground matter, and from that distortion they reconstruct how much matter is clumped between us and those galaxies. It is a probe of the *present-day* clumpiness of the universe, but it is not a direct measurement of $$\sigma_8$$. It is more like a measurement of shear correlations, which are then fit to a $$\Lambda$$CDM template to extract $$\sigma_8$$. We will come back to this nuance in a moment.

The good news was that every one of these surveys agreed with each other. The bad news: every one of them came in *lower* than Planck, and by enough of a margin that it could not be dismissed as a statistical coincidence.

The current numbers look roughly like this:

$$
\sigma_8^{\text{Planck}} \approx 0.811 \pm 0.006, \quad
\sigma_8^{\text{weak lensing}} \approx 0.76 \pm 0.02.
\tag{1}
$$

<img src="/assets/img/s8_tension.png" alt="The S8 tension between Planck and weak lensing surveys" style="width: 60%; display: block; margin: 2rem auto;">
*Figure 1: The $$S_8$$ tension. The Planck 2018 value (dark blue square) sits visibly to the right of the three weak-lensing measurements (KiDS-1000, DES Y3, HSC Y3). The shaded band is the Planck $$1\sigma$$ interval, and the dashed line marks its central value. The gap between Planck and the lensing mean is roughly $$3\sigma$$ — small enough that it could be a statistical fluke, but large enough that, in a model where $$\sigma_8$$ is predicted rather than fit, it demands an explanation. The top axis converts $$S_8$$ to $$\sigma_8$$ at $$\Omega_m = 0.3$$.*

The Planck satellite represents the $$\Lambda$$CDM fit to the early universe: its six baseline parameters are inferred from the CMB, and $$\sigma_8$$ is a *prediction* of that fit. Weak lensing surveys like KiDS and DES measure late-time shear correlations, and they fit those correlations to the same $$\Lambda$$CDM template, extracting a value of $$\sigma_8$$ from the fit. So one can think of the tension as two $$\Lambda$$CDM fits to two different datasets or the same model running on two different cosmic epochs. Neither side measures $$\sigma_8$$ directly; both report the value that $$\Lambda$$CDM assigns to their respective datasets (and epochs). And the central values differ by roughly $$3\sigma$$.

This is not an enormous discrepancy. For many problems in physics, a $$3\sigma$$ disagreement would be considered a curiosity, not a crisis. But in a field where $$\Lambda$$CDM fits everything else at sub-percent precision, a $$3\sigma$$ discrepancy in a parameter that the theory *predicts* is a problem. It has been called the "$$S_8$$ tension", with $$S_8$$ being a closely related statistic, defined as

$$
S_8 \equiv \sigma_8 \sqrt{\Omega_m / 0.3},
\tag{2}
$$

because it is what weak-lensing surveys actually constrain: the rescaling by $$\sqrt{\Omega_m/0.3}$$ breaks a degeneracy between $$\sigma_8$$ and the matter density $$\Omega_m$$.

Why does the tension persist? For a while, people blamed systematics, especially on the weak-lensing side: shear calibration, photometric redshift errors, intrinsic alignment of galaxies, and so on. Each of these has been studied in exhaustive detail. The surveys themselves have grown from hundreds of square degrees to thousands. Independent teams using independent pipelines keep finding the same low value. The tension has not gone away. If anything, it has been confirmed and sharpened.

On the Planck side, the situation is similar. The CMB measurement of $$\sigma_8$$ is not a single number, since it is inferred, through a chain of modeling assumptions, from the full power spectrum of temperature and polarization anisotropies. But the inference is robust: to reduce $$\sigma_8$$ while preserving the Planck acoustic peaks, you would need to change something substantial about the model.

## How $$\Lambda$$CDM predicts a number

Before we go any further, we need to answer a deceptively simple question: where does the number $$0.811$$ actually come from? Measuring the clumpiness of something is a unique problem and it requires unique cosmological techniques. The Planck satellite does not measure $$\sigma_8$$ with a ruler. It measures temperature fluctuations in the CMB, and those fluctuations are processed through a theoretical pipeline that ultimately outputs a value for $$\sigma_8$$. If we want to understand what the tension means, we need to understand that pipeline.

The computation happens in three stages: the primordial spectrum, the transfer function, and the growth factor.

### Stage 1: The primordial seed

Let's remind ourselves, from Cosmological Perturbation Theory, that the structures that we see in the universe today are cosmological evolutions of tiny perturbations in the early universe. Inflation stretched these primordial quantum fluctuations across the sky and froze them in as classical density perturbations. The statistics of these perturbations are encoded in the primordial power spectrum, which is nearly scale-invariant:

$$
\mathcal{P}_{\zeta}(k) = A_s \left(\frac{k}{k_{\text{piv}}}\right)^{n_s - 1},
\tag{3}
$$
where $$A_s$$ and $$n_s$$ are two of the six fundamental $$\Lambda$$CDM parameters. $$A_s$$ is the amplitude of primordial curvature fluctuations and serves as the "strength" or *power* of the quantum fluctuations injected into the universe during inflation. The second parameter ($$n_s$$) is the spectral index and encodes how these fluctuations depend on the scale. A weak scale-dependence in this case would imply that density fluctuations would not change depending on the size of the magnifying glass you use to measure them. Here, $$k_{\text{piv}}$$ is a pivot scale and denotes the scale you are viewing the universe from. Scale is usually denoted with $$k$$ and is a bit of a counter-intuitive quantity: a small $$k$$ means that you are viewing large chunks of the universe (viewing at large scales resulting in a low resolution picture) and a large $$k$$ would mean that you are viewing the universe with a very fine, small-grained view (viewing at small scales resulting in a sharp and resolved picture). Notice that if $$n_s=1$$, the primordial power spectrum would reduce to its scale-invariant (a.k.a Harrison-Zeldovich) limit $$\mathcal{P}_{\zeta}(k)=A_s$$, which would physically imply that irrespective of which picture you use (small-grained or low resolution), the strength of the primordial fluctuations would not change. This would result in a CMB with no fluctuations and would simplify the calculations, but it is not what we actually observe as CMB has these very tiny but measurable fluctuations in temperature. 


Planck measures $$A_s \approx 2.1 \times 10^{-9}$$, meaning that the primordial fluctuations were small in magnitude and $$n_s \approx 0.965$$, meaning that the power spectrum exhibits a small, but non-negligible, amount of scale-dependence which is interesting: the strength of the perturbations change depending on your "picture resolution" of the universe. These two quantities are raw input: a nearly flat spectrum of perturbations, laid down when the universe was only a fraction of a second old.

### Stage 2: The transfer function

Between inflation and today, the universe expands, cools, and passes through several epochs: radiation domination (when the universe was an ultra-hot soup of relativistic particles such as photons, neutrinos, and quarks), matter-radiation equality (when the energy budget of radiation diluted enough that it matches the matter budget before being overtaken by matter), recombination (when the universe cooled down enough to allow free electrons to be captured by nuclei) and many more epochs which deserve their own blog post. During these epochs, perturbations on different scales evolve differently. A mode that enters the horizon during radiation domination behaves much differently from one that enters during matter domination. The transfer function $$T(k)$$ encodes all of this physics and can be interpreted as the processing of the primordial spectrum by the cosmic expansion history. We would not need this parameter if the universe was still and boring, which is exactly why we need it.

The matter power spectrum today is then:

$$
P(k) = \mathcal{P}_{\zeta}(k) \, T^2(k) \, D^2(z=0),
\tag{4}
$$

where the primordial power spectrum, that we analyzed in Eq. 3, sets the initial conditions for the power spectrum. $$D(z)$$ is the linear growth factor, which describes how rapidly gravitational instability causes matter fluctuations to grow as the universe expands.This quantity can have profound consequences on the growth of structure and we will certainly come back to it later. For now, know that it is normalized so that $$D(0) = 1$$. The transfer function $$T(k)$$ is where $$\Lambda$$CDM does most of its work: it depends on the total density of all matter (including dark matter) $$\Omega_m h^2$$, the density of all Baryonic matter $$\Omega_b h^2$$, and the radiation density $$\Omega_r h^2$$. $$T(k)$$ determines the *shape* of the power spectrum: where the turnover of cosmic epochs occur and how much small-scale power is suppressed relative to large scales. Note that the computation of many quantities we will discuss (like for example $$T(k)$$), involves tracking complex coupled differential equations for dark matter, baryons, photons, and neutrinos simultaneously, and in many cases exact analytical solutions do not exist. Therefore, cosmologists solve for these numerically using codes like CLASS and CAMB, which is the approach we took in our paper.

### Stage 3: Smoothing on 8 $$h^{-1}$$ Mpc

The power spectrum $$P(k)$$ is a function of scale. But many observables, including the one we are after, want a **single number** that summarizes "how clustered is the universe today?" To get one, we smooth the density field inside a sphere of a chosen radius and compute the variance of the smoothed field. The radius is $$R_8 = 8\,h^{-1}$$ Mpc; the reason for that specific choice comes in the next subsection. First, the mathematics.

In technical terms, the smoothed density contrast is the integration of the original field with a window function $$W_R(\mathbf{x})$$:

$$
\delta_R(\mathbf{x}) = \int d^3x' \, W_R(\mathbf{x} - \mathbf{x}') \, \delta(\mathbf{x}').
\tag{5}
$$

While the previous sentence would have sounded incredibly fancy, it's actually quite intuitive to understand. In simple terms,  we are taking a blurry, averaged snapshot of the universe by running a giant sphere (of radius 8 $$h^{-1}$$ Mpc) across space and averaging everything inside it in order to attain a single value that summarizes how clumpy the universe is.

One can think of the density contrast field ($$\delta(\mathbf{x})$$) as the raw, pixel-perfect universe. If you could map out every single atom and dark matter particle in the universe down to the millimeter, that raw, ultra-detailed, spikey map is the original field. In this map, a single galaxy looks like a massive, sharp spike of high density, and the space right next to it looks like a deep, empty void. The window function $$W_R(\mathbf{x})$$ is simply your magnifying glass that dictates how you cut your chunks which you will use to view the universe. This is defined, in technical terms, as a "spherical top-hat" window. Physically, this is just a perfect, hard-edged 3D sphere with a radius of 8 $$h^{-1}$$ Mpc (about 26 million light-years).

For a **spherical top-hat** window of radius $$R$$, the window function is simply:

$$
W_R(\mathbf{x}) = \begin{cases} \dfrac{3}{4\pi R^3} & |\mathbf{x}| \leq R, \\[6pt] 0 & |\mathbf{x}| > R. \end{cases}
\tag{6}
$$

It is called a "window" because you are only looking at the matter that falls inside that specific sphere at any given moment. Everything outside the sphere is ignored (multiplied by 0). That is, it counts all the mass inside the sphere and averages uniformly. Its Fourier transform (the quantity that actually enters the variance calculation) has the closed form:

$$
\tilde{W}(kR) = \frac{3(\sin kR - kR \cos kR)}{(kR)^3}.
\tag{7}
$$

<img src="/assets/img/pk_and_filter.png" alt="The matter power spectrum and the top-hat filter" style="width: 60%; display: block; margin: 2rem auto;">
*Figure 2: The matter power spectrum $$P(k)$$ (top panel) and the squared top-hat filter $$\tilde{W}^2(kR_8)$$ (bottom panel), sharing the same wavenumber axis. The spectrum rises as $$k$$ at large scales (the primordial shape), turns over near the horizon scale at matter–radiation equality, and falls as $$k^{-3}$$ at small scales (transfer-function suppression). The filter peaks at $$k=0$$, where $$\tilde{W}=1$$, and oscillates to zero at $$kR_8 \approx 4.49$$. The shaded band marks the range of modes that contribute most to the $$\sigma_8$$ integral in equation (20): small-scale modes carry most of the power, but only the ones in the band survive the smoothing, and large-scale modes survive but carry little power. The $$\sigma_8$$ integral is dominated by this overlap region.*

This function peaks at $$kR = 0$$ and oscillates with decreasing amplitude at large $$kR$$. Physically, it is a filter: modes whose wavelength is much larger than $$R$$ vary slowly across the sphere and survive the average, while modes whose wavelength is much smaller than $$R$$ average to zero inside it and are suppressed. In other words, smoothing with a sphere of radius $$R$$ keeps only the modes with $$k \lesssim 1/R$$.

Now define the **smoothed density variance**:

$$
\sigma_R^2 \equiv \langle \delta_R^2(\mathbf{x}) \rangle.
\tag{8}
$$

This is the ensemble average of the squared smoothed density contrast: "how much does the smoothed density vary from one sphere of radius $$R$$ to another?" By substituting (5) into (8), we can evaluate the ensemble average for smoothed variance.

The equation (5) becomes a simple multiplication in Fourier space. Writing both the density field and the window function as inverse Fourier transforms,

$$
\delta(\mathbf{x}) = \int \frac{d^3k}{(2\pi)^3} \, e^{i\mathbf{k} \cdot \mathbf{x}} \, \tilde{\delta}(\mathbf{k}),
\qquad
W_R(\mathbf{x}) = \int \frac{d^3k}{(2\pi)^3} \, e^{i\mathbf{k} \cdot \mathbf{x}} \, \tilde{W}(kR),
\tag{9}
$$

the convolution theorem tells us immediately that the smoothed field in Fourier space is:

$$
\tilde{\delta}_R(\mathbf{k}) = \tilde{W}(kR) \, \tilde{\delta}(\mathbf{k}).
\tag{10}
$$

So in real space:

$$
\delta_R(\mathbf{x}) = \int \frac{d^3k}{(2\pi)^3} \, e^{i\mathbf{k} \cdot \mathbf{x}} \, \tilde{W}(kR) \, \tilde{\delta}(\mathbf{k}).
\tag{11}
$$

The variance is the ensemble average of the smoothed field squared. Write the product with two independent dummy wavevectors $$\mathbf{k}$$ and $$\mathbf{k}'$$:

$$
\sigma_R^2 = \left\langle \left[ \int \frac{d^3k}{(2\pi)^3} \, e^{i\mathbf{k} \cdot \mathbf{x}} \, \tilde{W}(kR) \, \tilde{\delta}(\mathbf{k}) \right] \left[ \int \frac{d^3k'}{(2\pi)^3} \, e^{i\mathbf{k}' \cdot \mathbf{x}} \, \tilde{W}(k'R) \, \tilde{\delta}(\mathbf{k}') \right] \right\rangle.
\tag{12}
$$

Pulling the integrations and the deterministic window functions outside the average bracket leaves:

$$
\sigma_R^2 = \int \frac{d^3k}{(2\pi)^3} \int \frac{d^3k'}{(2\pi)^3} \, e^{i(\mathbf{k} + \mathbf{k}') \cdot \mathbf{x}} \, \tilde{W}(kR) \, \tilde{W}(k'R) \, \langle \tilde{\delta}(\mathbf{k}) \, \tilde{\delta}(\mathbf{k}') \rangle.
\tag{13}
$$

The power spectrum is *defined* by the two-point correlation of Fourier modes. Because the universe is statistically homogeneous, different modes are uncorrelated unless they are exact opposites, so:

$$
\langle \tilde{\delta}(\mathbf{k}) \, \tilde{\delta}(\mathbf{k}') \rangle = (2\pi)^3 \, \delta_D(\mathbf{k} + \mathbf{k}') \, P(k).
\tag{14}
$$

Substituting this into (13):

$$
\sigma_R^2 = \int \frac{d^3k}{(2\pi)^3} \int \frac{d^3k'}{(2\pi)^3} \, e^{i(\mathbf{k} + \mathbf{k}') \cdot \mathbf{x}} \, \tilde{W}(kR) \, \tilde{W}(k'R) \, (2\pi)^3 \, \delta_D(\mathbf{k} + \mathbf{k}') \, P(k).
\tag{15}
$$

The Dirac delta function $$\delta_D(\mathbf{k} + \mathbf{k}')$$ forces $$\mathbf{k}' = -\mathbf{k}$$ everywhere, which does three things at once:

Firstly, The spatial exponential becomes unity: $$e^{i(\mathbf{k} - \mathbf{k}) \cdot \mathbf{x}} = e^0 = 1$$, so the position $$\mathbf{x}$$ drops out, as it must for a homogeneous universe. Secondly, the two window functions combine: $$\tilde{W}(kR) \, \tilde{W}(|\mathbf{-k}|R) = \tilde{W}^2(kR)$$ and thirdly, one factor of $$(2\pi)^3$$ cancels.

The double integral reduces to a single integral over $$\mathbf{k}$$:

$$
\sigma_R^2 = \int \frac{d^3k}{(2\pi)^3} \, P(k) \, \tilde{W}^2(kR).
\tag{16}
$$

Because the universe is isotropic, both $$P(k)$$ and $$\tilde{W}(kR)$$ depend only on $$k = |\mathbf{k}|$$, not on direction. We can therefore integrate out the angular part of the spherical volume element. Writing $$d^3k = k^2 \, dk \, d\Omega$$ and integrating over the full solid angle, $$\int d\Omega = 4\pi$$:

$$
\sigma_R^2 = \int_0^{\infty} \frac{4\pi k^2 \, dk}{(2\pi)^3} \, P(k) \, \tilde{W}^2(kR).
\tag{17}
$$

Simplifying the constant fraction, $$4\pi / (2\pi)^3 = 1/(2\pi^2)$$:

$$
\sigma_R^2 = \int_0^{\infty} \frac{k^2 \, dk}{2\pi^2} \, P(k) \, \tilde{W}^2(kR).
\tag{18}
$$

To write this in the form cosmologists conventionally use, multiply and divide the integrand by $$k$$. This isolates the logarithmic integration measure $$dk/k$$:

$$
\sigma_R^2 = \int_0^{\infty} \frac{dk}{k} \, \frac{k^3 P(k)}{2\pi^2} \, \tilde{W}^2(kR).
\tag{19}
$$

The bracketed quantity $$k^3 P(k) / (2\pi)^2$$ is conventionally denoted $$\Delta^2(k)$$, which is the **dimensionless power per logarithmic interval**. It is the natural way to ask "how much variance is contributed per decade of scale?" and it is what appears on the vertical axis of every plot of the matter power spectrum in the literature.

<img src="/assets/img/delta2_k.png" alt="The dimensionless power spectrum" style="width: 60%; display: block; margin: 2rem auto;">
*Figure 3: The dimensionless power per logarithmic interval, $$\Delta^2(k) \equiv k^3 P(k)/(2\pi)^2$$, with its peak normalized to 1 so that the shape is the focus. This is the quantity that appears on the vertical axis of every matter power spectrum plot, and it is the integrand of the $$\sigma_8$$ variance in equation (20). It rises as $$k^4$$ at large scales (primordial spectrum plus the $$k^3$$ weight), peaks near the horizon scale at matter–radiation equality ($$k \approx 0.02\,h/\text{Mpc}$$), and is roughly flat at small scales where transfer-function suppression cancels the $$k^3$$ growth. The shaded band marks the modes where the top-hat filter $$\tilde{W}^2(kR_8)$$ is non-negligible. The $$\sigma_8$$ integral in equation (20) is dominated by this overlap region — the peak of $$\Delta^2(k)$$ and the filter band coincide, which is exactly why $$R_8 = 8\,h^{-1}\text{Mpc}$$ was chosen. The absolute normalization is arbitrary; only the shape, the peak position, and the overlap with the filter matter for this discussion.*

So the final expression is:

$$
\boxed{\;\sigma_R^2 = \int_0^{\infty} \frac{dk}{k} \, \frac{k^3 P(k)}{2\pi^2} \, \tilde{W}^2(kR)\;}
\tag{20}
$$

Every quantity in this expression is calculable in $$\Lambda$$CDM: $$P(k)$$ comes from the transfer function and growth factor of Stages 1 and 2, $$\tilde{W}(kR)$$ is the top-hat filter in equation (7), and $$R$$ is a choice we make. Evaluating (20) at $$R = R_8 = 8\,h^{-1}$$ Mpc gives the number we want.

$$
\sigma_8 \equiv \sqrt{\sigma_{R_8}^2} \approx 0.811.
\tag{21}
$$

That is the number. For the $$\Lambda$$CDM parameters that best fit Planck, the variance of the density field smoothed on 8 $$h^{-1}$$ Mpc is $$0.811^2$$, and the square root is 0.811. Physically, if you pick any random 26-million-light-year sphere in the universe today, it will typically be either 0.81 times denser than the cosmic average or 0.81 times emptier than the cosmic average. This is a very decent measure of clumpiness, since if this value were 0.5, it would indicate that matter is more evenly distributed so there is less clumpiness. Similar if this value were greater, it would mean uneven distribution of matter and more clumpiness. If the universe was perfectly homogeneous, there would be no spatial deviation in density contrast and no structures would form on any scale and $$\sigma_8 = 0$$. So, we can establish that the standard deviation $$\sigma$$ of the density contrast measured at a scale of $$8\,h^{-1}$$ Mpc (therefore it is written as $$\sigma_8$$) is 0.81. 


### Why $$8\,h^{-1}$$ Mpc?

The choice is historical, but not arbitrary. A sphere of radius $$8\,h^{-1}$$ Mpc contains roughly the mass of a galaxy cluster which is about $$10^{14}$$ solar masses. It was chosen because it sits at the boundary between two regimes:

1. It is large enough that the density field is still approximately **linear**: perturbations have not yet collapsed and the evolution is well-described by perturbation theory. On smaller scales, structure has gone nonlinear and the linear power spectrum no longer applies.

2. It is small enough that the variance is **close to order unity**: the smoothed field is neither nearly uniform (which would give $$\sigma_R \approx 0$$ and be insensitive to changes) nor wildly nonlinear (which would require numerical simulations to compute reliably). Order-unity variance is exactly what you want in a diagnostic: it means a change in the underlying physics produces a measurable change in the number.

The scale was introduced in the 1980s, when the first galaxy surveys had enough data to measure clustering at this scale. It has remained the standard ever since because changing it would break continuity with decades of literature. But there is nothing deeply special about $$8\,h^{-1}$$ Mpc in the physics. It just happens to sit in the sweet spot between linearity and nonlinearity, and that is why it survives.

### The growth factor

The one remaining piece is $$D(z)$$, which tells us how perturbations grow between recombination and today. In $$\Lambda$$CDM, during matter domination, $$D(z) \propto a$$ so perturbations grow linearly with the scale factor. During dark energy domination, growth stalls. The full solution is obtained by solving the linear growth equation:

$$
D'' + \left(2 + \frac{H'}{H}\right) D' = \frac{3}{2} \Omega_m(a) D,
\tag{22}
$$

where primes denote derivatives with respect to $$\ln a$$. Solving this equation with the $$\Lambda$$CDM background gives the growth history that, combined with the transfer function, produces the power spectrum and the value of $$\sigma_8$$.

<img src="/assets/img/growth_factor.png" alt="The linear growth factor" style="width: 60%; display: block; margin: 2rem auto;">
*Figure 4: The linear growth factor $$D(z)$$ (top) and the growth rate $$f(z) = d\ln D / d\ln a$$ (bottom) in $$\Lambda$$CDM. Shaded bands mark the three cosmological regimes: radiation domination (yellow, left), matter domination (green, middle) where $$D \propto a$$ and $$f=1$$, and dark energy domination (purple, right) where growth stalls. The solid blue curves are the physical $$\Lambda$$CDM prediction, obtained by solving equation (22). The dashed red curves are a schematic illustration of what a *suppressed*-growth model would look like — not the LDS-SF prediction, which is derived in Blog 22, but a visual stand-in for the shape any resolution of the $$S_8$$ tension must have: identical to $$\Lambda$$CDM at high redshift, suppressed at $$z \lesssim 1$$. The bottom panel is the quantity that redshift-space distortion (RSD) measurements actually constrain — and the gap between blue and red at low $$z$$ is the observational signature of the tension.*

### Putting it together

So the chain is:

$$
\text{Primordial spectrum } \mathcal{P}_{\zeta}(k) \;\rightarrow\; \text{Transfer function } T(k) \;\rightarrow\; \text{Growth factor } D(z) \;\rightarrow\; P(k) \;\rightarrow\; \sigma_8.
\tag{23}
$$

Every step in this chain is calculable within $$\Lambda$$CDM. The parameters that enter are the six baseline numbers: $$\Omega_m$$, $$\Omega_b$$, $$h$$, $$A_s$$, $$n_s$$, and the optical depth to reionization. Given those six numbers, $$\sigma_8$$ is not a free parameter but a *prediction*. And the prediction is 0.811.

This is why the tension is relevant. If $$\sigma_8$$ were a free parameter that we fit to data, there would be no tension as we would just fit it to whatever the weak-lensing surveys see. But in $$\Lambda$$CDM, $$\sigma_8$$ is *derived* from the same six parameters that fit the CMB. If an independent survey (like weak-lensing) measure a different value, either the six parameters are wrong, or the theory that connects them to late-time structure is incomplete, or one of the measurements has a systematic error.

The rest of this series is about a fourth possibility: that the dark sector itself introduces new dynamics at late times, suppressing the growth of structure in a way that $$\Lambda$$CDM does not predict.

## What "reducing S8" actually requires

This is where it gets interesting. The $$S_8$$ tension is not a story about how much matter is in the universe, or how fast it is expanding, or how old it is. Those parameters are pinned by the CMB. What the tension tells us, if we trust it, is that the *process by which structure grows* over cosmic history is somehow not what our best theory: $$\Lambda$$CDM predicts.

In $$\Lambda$$CDM, density perturbations grow like this: during radiation domination, they grow logarithmically (slowly); during matter domination, they grow linearly with the scale factor; during dark energy domination, growth stalls because the accelerated expansion outpaces gravitational instability. The $$8\,h^{-1}$$ Mpc scale (the scale at which $$\sigma_8$$ is defined) is large enough that it never undergoes nonlinear collapse during most of cosmic history. It grows *linearly*, like a well-behaved cosmological perturbation. The growth of structure at this scale is therefore a clean prediction of the theory.

The weak-lensing surveys, by contrast, measure *late-time* structure. They are sensitive to the growth history, not just the growth amplitude, because the growth of structure at late times is what sets the amount of lensing. So the tension can be recast as a statement about *growth history*: Planck says structure should have grown to a certain amplitude by today. Weak lensing says it grew to slightly *less* than that. The disagreement is about the *rate* at which structure formed.

And the crucial observation is that the tension is *scale-dependent*. The CMB, at recombination, is essentially in perfect agreement between the two datasets because the CMB is a snapshot of the universe at $$z \approx 1100$$, and both datasets agree about what was going on back then. The disagreement only develops at *late times* ($$z \lesssim 1$$), and it is most pronounced at *small scales* (large wavenumber $$k$$).

This tells you exactly what kind of physics you need. We do not need a change to the early universe as that would spoil the CMB, neither do we need to change the background expansion as that would spoil BAO and supernovae. What you need is a mechanism that suppresses the growth of structure at late times and at small scales, while leaving everything else intact.

## The gauntlet

As you can probably imagine, this will not exactly be straightforward.

The obvious solution is to modify gravity. If gravity is weaker than General Relativity predicts at late times, structure grows more slowly, and $$\sigma_8$$ comes down. This is the strategy of $$f(R)$$ gravity and its many cousins. But modified gravity has a problem: if you change how gravity works at late times, you generally also change how it works *everywhere*, and unless you add a screening mechanism to hide the modification in the solar system, you violate local tests of GR. The screening mechanisms work, but they are baroque. They feel like epicycles.

The other obvious solution is to modify the dark sector. Dark matter and dark energy can exchange energy and momentum, slowing or accelerating the growth of structure depending on the details. Interacting dark sector models have been studied for decades. But here the problem is one of *predictivity*: there are so many ways to couple dark matter and dark energy that the models have a lot of freedom, and it is not obvious which one is correct. Often the couplings are adjusted by hand to fit the data, and the resulting models are not very constraining. My second paper explores this route.

There is a third strategy, and this is the one my first paper takes. What if the dark sector is not a single fluid, but a *structured* one. What if we assume a system with multiple interacting components whose internal dynamics produce scale-dependent effects? This sounds like an elegant way forward as we are not looking at an externally imposed modification, but an *emergent* one.

This is the Layered Dark Sectors with a Structuring Field framework or LDS-SF for short. And it will be our focus in the next few blogs.

## Summary

The $$S_8$$ tension is a persistent, roughly $$3\sigma$$ disagreement between the CMB prediction of how lumpy the universe should be and the weak-lensing measurements of how lumpy it actually is. It is primarily a story about the *growth rate* of cosmological structure at late times and at small scales. Any theory that resolves it must suppress growth *there* (at $$z \lesssim 1$$ and $$k \gtrsim 0.1\,h$$ Mpc$$^{-1}$$) while leaving the early universe, the background expansion, and the CMB untouched.

Modified gravity does this, but at the cost of changing GR everywhere. Simple interacting dark sector models do this, but with too much freedom to be predictive. The LDS-SF framework does it through internal dark-sector dynamics, and in the next five blogs, we will see exactly how.

Stay tuned. The tension is about to meet its match.


**References:**

[1] Planck Collaboration, *Planck 2018 results. VI. Cosmological parameters*, Astron. Astrophys. 641, A6 (2020).

[2] Heymans, C. et al., *KiDS-1000 cosmology: multi-probe weak lensing and relative clustering analysis*, Astron. Astrophys. 646, A140 (2021).

[3] Abbott, T. M. C. et al. (DES Collaboration), *Dark energy survey year 3 results: Cosmological constraints from galaxy clustering and weak lensing*, Phys. Rev. D 105, 023520 (2022).

[4] Verde, L., Treu, T., & Riess, A. G., *Tensions between the early and late Universe*, Nature Astronomy 3, 891 (2019).

[5] Naeem, M. & Farhan, M., *Layered dark structure with a structuring field: a $$Z_4$$-symmetric inert doublet-singlet realization and implications for the $$S_8$$ tension*, Physica Scripta 101, 125301 (2026).

[6] Ma, C.-P. & Bertschinger, E., *Cosmological perturbation theory in the synchronous and conformal Newtonian gauges*, Astrophys. J. 455, 7 (1995).

---
