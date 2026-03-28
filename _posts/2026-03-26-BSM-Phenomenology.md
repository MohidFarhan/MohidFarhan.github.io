---

title: "Blog 15—The Gauntlet: How to Kill a Theory Before It Kills You"
date: 2026-03-28
categories: [Particle Physics, Dark Matter, Beyond the Standard Model, Phenomenology]
use_math: true
layout: single
author_profile: true
read_time: true
comments: true
excerpt: "We built a beautiful machine to explain the dark universe. But beautiful ideas are cheap. The question is: can it survive reality?"

---

## Introduction

In our last adventure, we constructed something audacious. We placed a second Higgs doublet in the universe, which is a field that sits quietly at the origin, invisible to light, stabilized by a $$Z_2$$ symmetry, and perfectly poised to be the dark matter. We called it the Inert Doublet Model, or IDM. We checked that the math was consistent, that the vacuum was stable, and that the lightest particle would be trapped, stable, and abundant which would make it a viable dark matter candidate. The primary objective behind this endeavour was to have a motivated theory of dark matter.

But, in particle physics, beautiful ideas are cheap.

For every elegant theory that survives, a thousand have died. They died in the pages of notebooks, in the silent rejection of peer review, or in the crushing data of an experiment that said, "No, the universe does not work that way." The universe is not a democracy and does not care how clever your Lagrangian is. It simply is. And our job is not to dream, but to interrogate those dreams until they confess whether they match reality.

Today, we are not builders. We are executioners.

We are going to take the IDM—our beautiful, fragile construction—and run it through a gauntlet of tests. These are not optional extras. They are the gates that every Beyond-the-Standard-Model (BSM) theory must pass to be taken seriously. Most models fail. They fail because they predict particles that should have been seen at the Large Hadron Collider but weren't. They fail because they predict too much dark matter, or too little. They fail because their math breaks down at high energies, or because they violate some subtle symmetry of the weak force that we have measured to exquisite precision.

This is the BSM Viability Checklist, or more formally refered to BSM Phenomenology. It is a hierarchy of scrutiny that separates fantasy from physics.

First, we check if the theory is mathematically sound. Does it break down when we push it to high energies? Does its vacuum collapse if we look at it funny? This is the bare minimum. A theory that fails here dies before it reaches an experiment.

Second, we check if it plays nice with the precision measurements of the Standard Model. The electroweak sector has been measured to absurd accuracy. If our new particles tweak the Z boson mass or the Higgs couplings by even a fraction of a percent, the theory is dead.

Third, we check if it survives the collider. The LHC is a blunt instrument: it smashes protons together and asks, "What comes out?" If our dark sector particles can be produced at the energies we are probing, we should have seen them. If we haven't, they must be hidden and be either too heavy, or too weakly coupled, or decaying in ways we have missed or simply do not have the technology to see yet.

Fourth, and finally, we check the dark matter specific tests. Does our candidate actually freeze out with the right amount of abundance? The $\Lambda$CDM predicts a very perticular amount of DM abundance and experiments like Planck 2018 have measured its relic density (a measure of abundance) with incredible precision. Futhermore, Can it hide from direct detection experiments that are hunting for it with xenon tanks deep underground? Can it avoid annihilating too aggressively in dwarf galaxies and contradicting telescope data?

Only after surviving all of this does the IDM earn the right to be called "viable." And even then, it is merely "not dead yet."

So buckle up. We are moving from the abstract beauty of Lagrangians to the gritty reality of experimental constraints. We are going to learn how to kill a theory—and in doing so, learn why the IDM, against all odds, manages to stay alive.

Let us begin with the autopsy of failed dreams, and work our way up to the survivors.

## Theoretical Consistency: Does the Math Hold Together?

Before we ever compare our model to experiment, we must ask a more brutal question: does the theory mathematically make sense? This is the lowest bar, but astonishingly, many BSM proposals trip over it.

There are three ways a theory can die at this stage.

First, it can violate $$\textbf{perturbative unitarity}$$. In quantum mechanics, probabilities must sum to one. When we calculate scattering amplitudes for processes like $$W^+W^- \rightarrow W^+W^-$$, if the probability exceeds one at high energies, the theory is mathematically inconsistent. For the IDM, this imposes bounds on the quartic couplings $$\lambda_i$$. Specifically, combinations like $$\lambda_3 + \lambda_4$$ must remain small enough that scattering processes do not blow up before we hit the Planck scale.

Second, there is $$\textbf{vacuum stability}$$. We checked that our inert vacuum is a local minimum, but is it the global minimum? And does the potential remain bounded from below for all field configurations? The IDM potential must satisfy:

$$
\lambda_1 > 0, \quad \lambda_2 > 0, \quad \lambda_3 + \sqrt{\lambda_1\lambda_2} > 0, \quad \lambda_3 + \lambda_4 - \lambda_5 + \sqrt{\lambda_1\lambda_2} > 0
$$

If these fail, the universe could spontaneously decay into a lower-energy state, or the potential could run to negative infinity in some direction. An unstable vacuum means the theory has no predictive power.


Third, and most subtle, is $$\textbf{UV completion}$$. In quantum field theory, couplings are not constants inscribed at the beginning of time. They are alive, shifting and breathing as we probe different energies. This phenomenon, known as running, arises because quantum corrections from virtual particles constantly reshape the strength of interactions depending on the distance scale at which we observe them. When we run the couplings to high energies using the renormalization group equations (RGEs), we track this evolution through a set of beta functions. For every coupling parameter in the Lagrangian, there exists a distinct beta equation that governs its flow. For a generic coupling $$\lambda$$, this takes the schematic form:

$$
\beta(\lambda) \equiv \frac{d\lambda}{d\ln \mu} = \frac{1}{16\pi^2} \beta^{(1)}(\lambda) + \frac{1}{(16\pi^2)^2} \beta^{(2)}(\lambda) + \cdots
$$

where $$\mu$$ represents the energy scale, and the terms on the right-hand side encode quantum corrections from one-loop diagrams ($$\beta^{(1)}$$), two-loop diagrams ($$\beta^{(2)}$$), and beyond. In the IDM, we possess five quartic couplings—$$\lambda_1,\lambda_2,\lambda_3,\lambda_4, and \lambda_5$$, and each carries its own beta equation. These equations form a coupled dynamical system; the trajectory of $$\lambda_2$$ influences $$\lambda_{345} \equiv \lambda_3 + \lambda_4 + \lambda_5$$, and quantum feedback from the gauge sector reshapes the entire potential as we climb toward the ultraviolet.

As we integrate these flows upward, we must vigilantly guard against two distinct catastrophes. First, the Landau pole: a critical scale where a coupling blows up to infinity, signaling that the theory ceases to make sense and loses all predictive power. Second, and more insidious, is vacuum instability: even if couplings remain finite, the running might drive them into the forbidden regions of parameter space where the stability conditions, and their siblings—are violated. The potential would become unbounded from below, and the universe would decay catastrophically into a lower-energy state. Using tools like SARAH to generate two-loop beta functions, which I will show for the Inert Doublet Model in a dedicated section.

Finally, we must check $$\textbf{anomaly cancellation}$$. Gauge symmetries must be preserved at the quantum level. If the hypercharge assignments of our new particles create a gauge anomaly, the theory is inconsistent. Fortunately, the IDM adds a full $$SU(2)_L$$ doublet with standard hypercharge, so anomalies cancel automatically, just as they do in the Standard Model. But, a lot of models were not so lucky.

## Electroweak Precision Tests: Do Not Disturb the Weak Force

The Standard Model has been measured with terrifying precision. The mass of the $$Z$$ boson is known to within $$0.002\%$$. The weak mixing angle is constrained to one part in ten thousand. If we add new particles that interact with the gauge bosons, we must not disturb these delicate measurements.

The IDM adds a full doublet of scalars: $$H^0$$, $$A^0$$, and $$H^\pm$$. These contribute to $$\textbf{oblique corrections}$$, which are quantum loops that modify the propagators of the $$W$$ and $$Z$$ bosons. These are parameterized by the Peskin-Takeuchi variables $$S$$, $$T$$, and $$U$$.

The $$T$$ parameter is particularly dangerous for the IDM. It measures custodial symmetry breaking, which is the violation of the approximate symmetry that keeps the $$W$$ and $$Z$$ masses related. Charged scalars and neutral scalars contribute differently to $$T$$ because they break this symmetry through their mass splitting. The contribution is roughly:

$$
\Delta T \approx \frac{1}{4\pi\alpha v^2} \left[ m_{H^\pm}^2 + m_H^2 - \frac{2m_{H^\pm}^2 m_H^2}{m_{H^\pm}^2 - m_H^2} \ln\left(\frac{m_{H^\pm}^2}{m_H^2}\right) \right]
$$

If $$m_{H^\pm}$$ is very different from $$m_H$$, $$\Delta T$$ becomes large and positive. Experimental constraints from LEP and the LHC require $$\Delta T \approx 0.05 \pm 0.12$$. This forces the mass splitting between the charged and neutral inert scalars to be small, typically less than $$50$$ GeV. It is a severe constraint that carves up the parameter space, forbidding regions where the charged scalar is light and the neutral scalar is heavy, or vice versa.

The $$S$$ parameter measures the running of electroweak couplings and is less constraining for the IDM, though it still prefers degenerate masses. The $$U$$ parameter is usually negligible.

This is why precision measurements are so powerful: even if we never produce the particles directly at a collider, their virtual presence in loop diagrams would have already altered the properties of the $$Z$$ boson in ways we would have detected in the 1990s at LEP.

## Collider Constraints: Hide or Die

If the inert scalars are light enough to be produced at the LHC, and if they interact with Standard Model particles with sufficient strength, we should have already seen them. The fact that we have not imposes strict bounds.

The smoking gun is the $$\textbf{charged scalar}$$, $$H^\pm$$. Unlike the neutral dark matter candidate $$H$$, the charged scalar cannot be stable, it decays into Standard Model particles. The dominant decay mode depends on the mass spectrum:

$$
H^\pm \rightarrow W^\pm H \quad \text{(if kinematically allowed)}
$$

or through off-shell $$W$$ bosons to leptons and neutrinos. Searches at the LHC for disappearing tracks, soft leptons, or missing energy plus charged lepton pairs place lower bounds on $$m_{H^\pm}$$, typically around $$100$$ GeV or higher depending on the decay mode.

Then there is $$\textbf{mono-X production}$$. If the $$Z_2$$ symmetry is exact, we cannot produce single inert particles. But we can produce them in pairs: $$pp \rightarrow H^0 H^0$$, $$pp \rightarrow H^0 A^0$$, or $$pp \rightarrow H^+ H^-$$. These processes are mediated by Higgs boson exchange or vector boson fusion. The signature is jets or gauge bosons recoiling against missing transverse energy (MET), carried away by the invisible dark matter candidates.

Current LHC Run 2 and Run 3 searches for mono-jets, mono-$$Z$$, and mono-Higgs place upper limits on the portal coupling $$\lambda_{345}$$. If $$\lambda_{345}$$ is too large, production is too frequent, and we would have seen an excess. If it is too small, the dark matter annihilates too slowly in the early universe, overclosing the universe.

Finally, there are $$\textbf{invisible Higgs decays}$$. The Higgs boson can decay into a pair of dark matter particles: $$h \rightarrow HH$$. The branching fraction for this is proportional to $$\lambda_{345}^2$$. Current LHC constraints limit the invisible branching ratio to less than about $$11\%$$. This directly bounds the portal coupling, forcing it to be small, typically $$\lambda_{345} < 0.01$$ for dark matter masses below $$m_h/2 \approx 62.5$$ GeV.

## Dark Matter Specifics: The Cosmic Accounting

Even if the IDM survives collider searches and precision tests, it must still account for the dark matter we see in the sky. This requires passing three cosmic trials.

First is the $$\textbf{relic density}$$. In the early universe, the dark matter particles $$H$$ were in thermal equilibrium with the hot plasma. As the universe cooled, they stopped interacting efficiently and froze out, leaving behind a relic population. The present-day abundance is:

$$
\Omega h^2 \approx \frac{1.07 \times 10^9 \text{ GeV}^{-1}}{g_*^{1/2} M_{\text{Pl}} \langle \sigma v \rangle}
$$

where $$\langle \sigma v \rangle$$ is the thermally averaged annihilation cross-section. The Planck satellite measures $$\Omega h^2 = 0.120 \pm 0.001$$. To match this, the annihilation cross-section must be approximately $$3 \times 10^{-26}$$ cm$$^3$$/s, which is the famous thermal relic cross-section.

In the IDM, dark matter annihilates through several channels. It can annihilate to $$HH \rightarrow W^+ W^-$$ and $$HH \rightarrow ZZ$$ via gauge interactions if $$m_H > m_W$$. It can annihilate to $$HH \rightarrow f\bar{f}$$ through Higgs boson exchange in the s-channel. There is also co-annihilation with $$A^0$$ and $$H^\pm$$ if the mass splittings are small.

Near the Higgs resonance at $$m_H \approx m_h/2 \approx 62.5$$ GeV, the cross-section is enhanced. Near the $$W$$ and $$Z$$ thresholds, new channels open up. The IDM can achieve the correct relic density for masses between about $$50$$ GeV and $$1$$ TeV, with specific gaps excluded by the $$Z$$ boson pole and Higgs width constraints.

Second is $$\textbf{direct detection}$$. Dark matter particles permeate the galaxy and pass through the Earth. Occasionally, they scatter off atomic nuclei in underground detectors like XENON-nT, LZ, or PandaX-4T. In the IDM, this happens through Higgs boson exchange:

$$
\mathcal{L}_{\text{int}} = -\lambda_{345} v h H^2
$$

The spin-independent scattering cross-section off nuclei is proportional to $$\lambda_{345}^2$$. Because $$\lambda_{345}$$ must be small to avoid invisible Higgs decays, the IDM naturally predicts a suppressed direct detection rate. For $$m_H \sim 100$$ GeV, the cross-section is typically many orders of magnitude below current limits, making the IDM a stealthy dark matter candidate.

Third is $$\textbf{indirect detection}$$. If dark matter annihilates today in the galactic center or in dwarf spheroidal galaxies, it produces gamma rays, positrons, or antiprotons. The Fermi-LAT telescope looks for excess gamma-ray emission from dwarf galaxies, placing limits on the annihilation cross-section today. Because the IDM annihilates primarily to $$W$$ bosons or $$b$$-quarks, it produces a characteristic gamma-ray spectrum. However, for thermal relic dark matter, the current annihilation rate in the present day is too low to be detected by Fermi-LAT unless the density is enhanced in substructures, which is a model-dependent assumption.

Finally, there are $$\textbf{structure formation}$$ constraints. If the dark matter is too light (below about $$10$$ keV), it free-streams out of small density perturbations, smoothing out structure and contradicting observations of the Lyman-alpha forest and the number of Milky Way satellites. The IDM dark matter is heavy ($$>50$$ GeV), so it is cold dark matter and passes this test easily.

## The Hidden Blades: Constraints That Kill in the Shadows

You have survived the four gates. But the gauntlet has deeper circles, reserved for models that dare to touch the forbidden sectors of the Standard Model. These tests do not merely ask if your theory exists—they ask if it has committed crimes against flavor, against time-reversal symmetry, against the primordial fire of the Big Bang itself. 

Most models die here, in the dark, long before they ever face a collider.

### Flavor Physics: The Precision Killers

If your model introduces new particles that couple to quarks or leptons, you must answer to the flavor sector. The Standard Model forbids $$\textbf{flavor-changing neutral currents (FCNCs)}$$ at tree-level, and experiments have measured rare processes like $$B_s \rightarrow \mu^+\mu^-$$, $$K^+ \rightarrow \pi^+ \nu \bar{\nu}$$, and $$B \rightarrow X_s \gamma$$ to excruciating precision. 

In the IDM, we survive by luck: the $$Z_2$$ symmetry prevents our new scalars from coupling to fermions directly. They speak to the Standard Model only through the Higgs portal and gauge bosons. But for models like the Two-Higgs-Doublet Model without a $$Z_2$$, or for Randall-Sundrum gravitons, or for leptoquarks, flavor physics is often the immediate death sentence. A single new particle with generic Yukawa couplings will generate FCNCs at one-loop, predicting branching fractions that differ from measurement by orders of magnitude.

Then there is the anomalous magnetic moment of the muon, $$(g-2)_\mu$$. The Brookhaven measurement experiment suggests a $$4.2\sigma$$ deviation from the SM prediction. If your BSM model cannot generate a positive contribution of roughly $$250 \times 10^{-11}$$, or if it generates the wrong sign or magnitude, you fail this test. The IDM struggles here as it can contribute to $$(g-2)_\mu$$ only through two-loop Barr-Zee diagrams, which are typically too small to explain the anomaly. This is not an immediate execution for the IDM, but it is a missed opportunity that other models must capitalize on to survive.

### Electric Dipole Moments: The CP Violation Hunters

Any BSM model that introduces new CP violation (which we have already discussed in the previous blog) must contend with the electron and neutron electric dipole moments (EDMs). The ACME collaboration has constrained the electron EDM to $$d_e \leq 1.1 \times 10^{-29}$$ e·cm. If your model contains complex phases in the new couplings, which is natural if you are trying to explain the matter-antimatter asymmetry of the universe, it will generate EDMs at one or two-loop order.

The IDM is safe here because the $$Z_2$$ symmetry forces all couplings to be real (or absorbed into field redefinitions), and the scalar potential can be made CP-conserving. But for models like the Minimal Supersymmetric Standard Model with CP-violating phases, or generic multi-Higgs models, the EDM constraints chop the parameter space into fragments. A complex $$\lambda_5$$ in the IDM would immediately face the firing squad of ACME and neutron EDM searches.

### Big Bang Nucleosynthesis and $$N_{\text{eff}}$$

Before the universe became transparent at recombination, it was a nuclear furnace during Big Bang Nucleosynthesis (BBN) lasting from one second to three minutes. The abundances of helium-4, deuterium, and lithium-7 are measured to percent-level precision. If your dark sector contains light species ($$\lesssim 100$$ MeV) that enter equilibrium with the Standard Model plasma, they will alter the expansion rate and the freeze-out of nuclear reactions, destroying the agreement with observed helium-4.

Additionally, the effective number of neutrino species, $$N_{\text{eff}}$$, is constrained by Planck and BBN to be $$N_{\text{eff}} = 2.99 \pm 0.17$$. Any new relativistic species present during recombination will shift this value. The IDM particles are required to be heavy ($$\geq 50$$ GeV), so they are non-relativistic during BBN and contribute nothing to $$N_{\text{eff}}$$. But axions, dark photons, or light sterile neutrinos face immediate annihilation by this constraint unless they are extremely weakly coupled or have specific temperature-dependent decoupling histories.

### Self-Interacting Dark Matter: The Astrophysical Mirror

Beyond relic density and direct detection, dark matter must not interact with itself too strongly. Observations of the Bullet Cluster and dwarf spheroidal galaxies suggest that dark matter behaves collisionlessly. If the IDM contained large quartic couplings like $$\lambda_2 v^2 H^2 H^2$$, the dark matter particles would scatter off each other in galactic halos, altering the density profiles of dwarf galaxies and creating offsets between the dark matter and stellar distributions during mergers.

The constraint is parameterized by the self-interaction cross-section divided by mass, $$\sigma/m \leq 1$$ cm$$^2$$/g (roughly equivalent to a barn per GeV). The IDM predicts $$\sigma \sim \lambda_2^2/(16\pi m_H^2)$$, which is typically negligible for weak-scale masses and couplings. But for models with light dark matter and strong self-couplings (such as certain hidden sector models) this is the executioner they cannot escape.

### Proton Decay: The GUT Guillotine

If your BSM model is a Grand Unified Theory (GUT) attempting to unify the strong, weak, and electromagnetic forces into a single gauge group like $$SU(5)$$ or $$SO(10)$$,you have invoked baryon number violation. The Super-Kamiokande experiment has constrained the proton lifetime to $$\tau_p \geq 1.9 \times 10^{34}$$ years for the decay $$p \rightarrow e^+ \pi^0$$. This requires GUT-scale masses above $$10^{15}$$ GeV and highly suppressed couplings.

The IDM is not a GUT and it respects baryon number at the renormalizable level. But any BSM model that dares to unify must present its throat to this blade. The $$\text{SU}(5)$$ model with minimal Higgs content was killed by proton decay decades ago and only its supersymmetric extensions survived briefly, and even those now face the same guillotine. 

There are almost certainly more tests that I might not be aware of or may have missed. These tests are relentless and pose great challenges to model builders and phenomenologists, but we are not completely defenseless. Over the years, many tools have been developed to compute the predictions of BSMs and their feasibility.


## Implementation of Constraints

Now, we are moving towards the interesting research part where we will apply specialized research tools to test different models beyond the standard model. At this stage, you are well eqipped to read the research literature and the physics landscape we have entered is no longer covered by books or youtube tutorials, since this is "active area of research" territory. This particular blog is confined to my personal research findings about the Inert Doublet Model, and the tools I used to get there. For greater details, you can explore the references. The research tools are not listed for now, as the instructions of using these tools deserve a blog of their own. 


### Figure 1: RGE Running and Landau Poles
![RGE Running](/assets/images/B15P1.jpg)

**Caption:** *One-loop renormalization group evolution of the quartic couplings $$\lambda_2$$ (controlling the inert sector self-interaction) and  $$\lambda_3, \lambda_4, \lambda_5$$ (the Higgs portal couplings). The blue curve hits a Landau pole at $$Q \sim 10^{7}$$ GeV for initial $$\lambda_2 = 0.2$$, while $\lambda_{345}$ remains relatively more perturbative. This demonstrates that the IDM can not make reliable prediction beyond $$\sim 10^7$$ GeV, and is an Effective Field Theory (EFT) with a UV-cutoff. Since the usual dark matter candidates are far lighter than the IDM VU-cutoff, it is a reliable EFT in regimes considered with a caveat of requiring new physics to reach the Planck scale.*

### Figure 2: 2HDMC Parameter Space Scan
![2HDMC Scan](/assets/images/B15P2.jpg)

**Caption:** *The CP-even-odd parameter space of the IDM, scanned using theoretical constraints (perturbative unitarity, vacuum stability) and electroweak precision tests (S, T, U parameters). Gray points violate theoretical consistency. Orange points are mathematically valid but excluded by the T-parameter constraint $$\Delta T < 0.12$$ (95\% CL), which requires near-degenerate masses $$m_A - m_H \lesssim 50$$ GeV. Green points survive both theoretical and precision electroweak constraints. Red stars mark specific benchmarks: BP62 (Higgs funnel), BP100 (low mass), and BP200 (co-annihilation region).*

### Figure 3: Relic Density Calculation (micrOMEGAs)
![Relic Density](/assets/images/fig1.jpg)

**Caption:** *Dark matter relic density $$\Omega h^2$$ as a function of the Higgs portal coupling $$\lambda_L \equiv \lambda_{345} = \lambda_3 + \lambda_4 + \lambda_5$$ for varying mass-splitting parameters $$\delta = m_A - m_H = m_{H^\pm} - m_H$$ (assuming $$m_{H_C} = m_{H_3} = 550$$~GeV). The horizontal bands indicate the $$3\sigma$$ Planck 2018 constraint $$0.120 \pm 0.012$$ (shaded region). Smaller $$\delta$$ values enhance co-annihilation channels, suppressing the relic density for $$\lambda_L \geq 0$$, while large $$\delta$$ (e.g., $$\delta = 5$$~GeV, yellow curve) shows reduced co-annihilation and higher $$\Omega h^2$$. The vertical dashed line marks $$\lambda_L = 0$$, where annihilation through the Higgs boson is suppressed. The maximum abundance is, unsurprisingly, recorded when the Higgs-DM coupling was at its lowest.*

### Figure 4: Direct Detection Constraints (XENON-nT/LZ)
![Direct Detection](/assets/images/B15P4.jpg)

**Caption:** *Spin-independent scattering cross-section $$\sigma_{\rm SI}$$ versus dark matter mass. The shaded blue and cyan regions are excluded by XENON-nT (2023) and LZ (2023) at 90% CL. The green band shows the IDM prediction. The IDM naturally predicts $$\sigma_{\rm SI} \sim 10^{-11}-10^{-13}$$ pb, lying 2-3 orders of magnitude below current sensitivities and approaching the neutrino floor (dotted black line) where astrophysical neutrino backgrounds become irreducible. Red stars mark viable benchmarks that evade direct detection. The neutrino floor is a fundamental experimental bound on dark matter detection caused by the increased sensitivity of the involved methods. If this senstivity goes beyond a certain cross section, we can misinterpret dark matter particles as neutrinos. In this regime, the risk is that a dark matter detectection could hide behind the noise of neutrino detections refered to as the "neutrino fog".*

### Figure 5: Invisible Higgs Decay Constraints (HiggsBounds)
![Invisible Higgs](/assets/images/B15P5.jpg)

**Caption:** *Branching ratio of the 125 GeV Higgs boson decaying to dark matter pairs, $${\rm Br}(h \to HH)$$, as a function of $$m_H$$ for different values of the portal coupling $$\lambda_{345}$$. The red shaded region above the dashed line ($${\rm Br}_{\rm inv} > 11\%$$) is excluded by LHC combined Higgs coupling measurements. The kinematic limit $$m_H < m_h/2 \approx 62.5$$ GeV is shown by the vertical dotted line. For $$m_H < 62.5$$ GeV, the IDM requires $$\lambda_{345} \lesssim 0.01$$ to avoid exclusion, naturally suppressing direct detection rates.*

### Figure 6: Mono-X Constraints vs Relic Density (LHC)
![Mono-X Exclusion](/assets/images/B15P6.jpg)

**Caption:** *The corridor of survival in the $$(m_H, \lambda_{345})$$ plane. The red shaded regions are excluded by LHC mono-X searches (mono-jets, mono-Z, mono-Higgs with missing transverse energy). The blue shaded region produces under-abundant dark matter ($$\Omega h^2 < 0.1$$), overclosing the universe. The viable parameter space is the narrow green band where the coupling is large enough to annihilate the correct relic density (avoiding the blue region) but small enough to have escaped LHC detection (avoiding the red region). The Higgs resonance at $$m_H \approx 62.5$$ GeV allows temporarily smaller couplings.*

### Figure 7: The Execution Map (Combined Constraints)
![Execution Map](/assets/images/B15P7.jpg)

**Caption:** *The complete execution map of the IDM in the $$(m_H, m_A)$$ plane. Yellow regions violate electroweak precision tests (particularly the T-parameter, which constrains the mass splitting $$m_A - m_H < 50$$ GeV). Red regions below $$m_H < 45$$ GeV are excluded by the Z-pole resonance (incorrect relic density). Purple regions above 550 GeV violate perturbative unitarity. The surviving viable parameter space (green) is a narrow wedge near the $m_A = m_H$ diagonal, bounded by the LEP charged scalar limit ($$m_{H^\pm} \gtrsim 100$$ GeV) and unitarity constraints.*




