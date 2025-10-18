---

title: "Blog 3—Measuring the Cosmos: From Parallax to the Edge of the Universe"
date: 2025-08-30
categories: [Cosmology, Astronomy, Particle Physics, Astrophysics]
use_math: true
layout: single
author_profile: true
read_time: true
comments: true
excerpt: "How do we measure something we can’t touch? From the tiny wiggle of a nearby star against the night sky to the stretching fabric of space itself, astronomers have built a cosmic ruler that spans billions of light-years. Each step extends our reach deeper into the universe. We will dive into how we use a simple combination of eyepieces, lenses and gratings to peek into the edge of the universe."

---

## Introduction

Have you ever come across an enormous number with the words "light years" next to it? If yes, then naturally, one must wonder how we got to this number.
Are these distances even real, or do scientists make them up and pull them out of nowhere? I mean, who will question them anyway? Let's answer these questions.

Today, we will take a deep dive into the ingenious methodology of determining cosmological distances.
We will start with methods of determining nearby objects and then progressively move to the farther objects, until we reach the edge of our universe.
To develop an understanding of astrophysics and cosmology, it is pivotal to understand the methods of determining large distances, so bear with me.

## The Stellar Parallax

I want you to hold your thumb inches away from your eyes. Close your right eye while keeping the left one open and vice versa. Notice something?
You may have found that your thumb shifts position relative to the background. This is not because your thumb magically moved when you switched eyes, but has more to do with angles and how your brain perceives depth. By measuring the angle of the shift and knowing the distance between your eyes, you can determine how far away your thumb is. And all you need is basic trigonometry.
Why did I make you do this random task? That's because scientists also do the same random task to determine stellar distances, but on a much larger scale.
Unfortunately, your eyes are too close for this method to work on distant stars, since the "shift" angle is too small and impossible to measure. Then how can we use this method?

The answer is surprisingly simple. You capture the star on your telescope. Then wait six months before doing the same again, having your telescope in the same location for maximum accuracy.
The idea is to leverage the distance traveled by the Earth, in order to attain a large enough angle such that it is measurable. After 6 months, the Earth is on the other side of the Sun, implying that the "distance between our eyes" is 2 Astronomical Units (AU) in-between the stellar snapshots, where AU is the distance between the Earth and the Sun. This makes sense in the diagram shown below.

Consider a nearby star observed from Earth at two opposite points in its orbit around the Sun, six months apart. The baseline of this observation is the diameter of Earth's orbit, which is 2 AU, giving a right triangle with a baseline of 1 AU, distance to the star (d), and Parallax angle (p), measured in arcseconds which is one of 3600 parts of a degree.

![Figure 1](/assets/images/ParallaxDiagram_ManimCE_v0.19.0.png)

**Figure 1**: A visualization of the trigonometry involved with stellar parallax (very very not to scale).

Using basic trigonometry:

$$
\tan p = \frac{1}{d}
$$

For very small angles (which parallax angles always are), we can use the small-angle approximation:

$$
\tan p \approx p \quad \text{(in radians)}
$$

Thus:

$$
p~(\text{radians}) = \frac{1~\text{AU}}{d}
$$

To convert to arcseconds:

$$
p~(\text{arcseconds}) = \frac{206265~\text{arcsec}}{\text{radian}} \cdot \frac{1~\text{AU}}{d}
$$

Defining 1 parsec as the distance at which a star has a parallax of 1 arcsecond:

$$
d~(\text{parsecs}) = \frac{1}{p~(\text{arcsec})}
$$

where 1 pc = 206265 AU.

This proves to be a simple yet elegant method of determining stellar distances. By measuring the shift angle in arcseconds, we can immediately obtain a reasonable estimate of its distance from us.

Stellar parallax yields very accurate results for determining distances of solar system objects, and other nearby neighboring stars, but breaks down beyond 10 Kpc due to our limitations of measuring angles. So, if you would have noticed, there exist background stars in the diagram, which do not shift much, if at all. These stars are beyond 10 Kpc. We, therefore, run into a challenge. How would we measure the distances to those stars?

## How far did Stellar Parallax get us?

10 Kpc is an impressive distance, and already it's an unfathomable distance. Upon conversion, we find that it is roughly 32,600 light years. This means that light, the fastest entity in the universe, takes 32,600 years to travel this distance!

If we see a star 30,000 LY from us, we are seeing the star as it was 30,000 years ago, because light that left it 30,000 years ago is only reaching us at that point. Conversely, if aliens inhabiting near the stars pointed their telescopes to us, assuming a powerful enough zoom, they would see humans painting mammoths on cave walls and walking on glaciers resulting from the latest ice age.

This is already an insane distance BUT our galaxy, the Milky Way, is 100,000 LY in diameter. We can barely determine the distances of one-third of the contents of our own galaxy, let alone those of other galaxies. This realization humbled us quickly and made us push to find another method that was successful at the larger scales.

## Spectroscopic Parallax - A misleading name

Stellar parallax can reach distances up to approximately 10,000 parsecs, but only with extremely precise instruments like the Gaia space telescope, and only for relatively bright stars. For dimmer or more distant stars, parallax becomes unreliable. In such cases, spectroscopic parallax offers an alternative method.

This method does not involve actual parallax angles. The star's spectral type and luminosity class are determined using its spectrum. From that classification we know the intrinsic brightness of the star and an estimate of the star’s absolute magnitude (M) is obtained using standard stellar models or HR diagrams. m is the apparent magnitude of a star if it were 10 pc from Earth.

The apparent magnitude (M) is a measure of the star's brightness as seen from Earth, hence the word "apparent". This quantity can be measured observationally through a telescope. This quantity can be small despite the star being very bright, given that it's distant. This is because of the fact that brightness falls off with distance.
M and m is all you need to determine the distance, thanks to the distance modulus formula.

$$
m - M = 5 \log_{10}(d) - 5
$$

Solving for d:

$$
d = 10^{\frac{m - M + 5}{5}} \quad \text{(in parsecs)}
$$

The derivation of this formula, as well as how it can be used, is in the appendix. For now, all you need to know is that the formula leverages the fact that the larger the deficit in the apparent and absolute magnitude of a star, the greater the distance. If the apparent magnitude is equal to the absolute magnitude, the distance is 10 pc by definition. If the apparent magnitude is much smaller than the absolute magnitude, then the star appears dim although it is intrinsically bright, meaning that it must be much farther than 10 pc, and vice versa, if the star appears bright but is actually dim, it must be much closer than 10 pc.
This formula determines the exact values, and will also be useful ahead. These exact values are shown through figure 2.

![Figure 2](/assets/images/B2P1.png)

**Figure 2**: The distance modulus as a function of distance from the observer, in logarithmic scale.

## Cepheid Variable Stars

The method of spectroscopic parallax only improved our readings for dim stars, without improving much of our range. To go intergalactic, we turn to Cepheid variable stars. Cepheid variable stars are pulsating stars whose brightness varies in a predictable cycle. Their importance comes from a precise relationship between their pulsation period and intrinsic luminosity.

Discovered by Henrietta Swan Leavitt while studying stars in the Small Magellanic Cloud. All Cepheids in the same galaxy are roughly at the same distance, allowing the variation in brightness to be attributed to intrinsic luminosity. The longer the pulsation period, the brighter the star.

This relationship allows astronomers to infer the absolute magnitude M from the observed period. The empirical Period–Luminosity relation for Classical Cepheids is often written as:

$$
M = a \log_{10}(P) + b
$$

where M is the absolute magnitude, P is the period in days, and a and b are calibration constants determined observationally.

![Figure 3](/assets/images/B3P2.png)

**Figure 3**: The Magnitude plotted as a function of the period of the star's brightness cycle.

Once M is known, the task is the same. We determine m observationally and use the distance modulus formula again. By leveraging the best of today's technology, the James Webb Space Telescope, this method gives us readings of up to 20 Mpc. This translates to 60 million LY which is so insane, that if aliens that far away were to point their telescopes on Earth, they would see the event that wiped out the dinosaurs, or even the dinosaurs if they're lucky!.
This upgrade easily increases our range from a fraction of our own galaxy to, comfortably, the local group and the Virgo supercluster.

## Type 1a Supernovae

60 Mpc is not bad but in cosmological scale, even calling it the tip of the iceberg would be generous. Let's keep going farther and farther. In the regime we are currently in, the distance modulus remains our only hope and so the challenge is to keep on coming up with methods of determining the absolute magnitude and the intrinsic brightness of the distant objects. I write "objects" and not stars because stars are not bright enough anymore, but supernovae sure are.
Supernovae are violent explosions that occur due to the gravitational collapse of huge stars. They are known to be among the most energetic events in the known universe. You know it's serious when a single event outshines galaxies for weeks.

Type Ia supernovae are thermonuclear explosions of white dwarfs in binary systems. When the white dwarf accretes enough mass from its companion star to approach the Chandrasekhar limit (about 1.4 solar masses), it undergoes runaway nuclear fusion and explodes. These supernovae have very consistent intrinsic luminosities, making them excellent standard candles.

These supernovae have very consistent intrinsic luminosities, making them excellent standard candles. Their peak absolute magnitude is approximately around 19.3. The light curve (brightness vs time) follows a predictable shape, which can be used to refine the intrinsic brightness even further. These supernovae were instrumental in determining that the universe's expansion was accelerating, leading to the concept of Dark Energy, which will be a discussion for a future blog.
Once again, since we know M, we can easily know everything else needed to use the distance modulus formula. 

But by using the Type 1a supernovae as standard candles, our distance determination range increases to a whopping 1 Gpc, by using the James Webb Space Telescope. This is the equivalent to 3 billion LY.
This upgrade means that the aliens would now see an Earth restricted only to unicellular, microbial life. This younger, 1.5-billion year old Earth was a lot hotter than today, with completely different continents, and a whole lot of volcanic activity and crater formations. It is believed that Mars had liquid water at around this time, though that is debatable.

## Cosmological Redshift

3 billion LY is almost a quarter of the observable universe. There's more than 3 quarters STILL left, which makes us realize the utter scale of the universe we are a part of. There are no events bright enough for us to reliably determine M and latch onto the distance modulus formula, so is this it?
The answer is a resounding no thanks to the final boss: cosmological redshift. In this method, astronomers rely on the expansion of space itself to determine distances using redshift. As light travels through expanding space, its wavelength stretches. This effect is called redshift, denoted by z. This is because of the scale factor, denoted by a(t). This variable is responsible for stretching the fabric of spacetime itself and the fact that observations suggest that a increases with time makes for some interesting implications. Firstly, this suggests that lengths are not universal constants over a long enough time frame, and to accurately model the universe, this constant change in length due to the expansion of the universe should be accounted for. It also means that wavelength of a photon travelling in a particular direction does not stay the same, and evolves over time. Simulation 1 shows an intuitive depiction of this phenomenon. 

<!-- Animation of vacuum fluctuations -->
<p align="center">
  <img src="/assets/images/Adobe Express - PhotonRedshift.gif" width="500" alt="The Cosmological Redshift"/>
  <br><em>Simulation 1: The wavelength of a photon changing with time, for a case where the scale factor increases linearly with time.</em>
</p>


It is therefore wasy to see that all photons travelling through billions of years have a measureable increase in wavelengths which is captured by spectrographs that are sensitive enough. It is this very increase that is termed as redshift, because if you increase the wavelength of a photon in the visible electromagnetic range, its spectrum shifts towards the infra-red region. The farther away a galaxy is, the more its light is redshifted. This relationship was first discovered by Edwin Hubble in 1929. For small redshifts where z exceeds or is near 0.1, the velocity at which a galaxy appears to be receding is:

$$
v = H d
$$

where v is the recession velocity, H is the Hubble constant (units: km/s/Mpc), and d is the distance to the object in megaparsecs (Mpc).

Solving for distance:

$$
d = \frac{v}{H} = \frac{cz}{H}
$$

c is the speed of light. 

![Figure 4](/assets/images/B2P4.png)

**Figure 4**: The Hubble's law which does not account for redshift.



This approximation works well for nearby galaxies (100 MLY), where there is little redshift. For more distant objects where z exceeds 1, cosmological models must be used to relate redshift and distance accurately.
At high redshifts, the universe’s expansion has changed over time, so the simple linear Hubble law is replaced by integrals over the expansion history. Redshift-based methods can measure distances to quasars and galaxies billions of light-years away.

Combined with supernova observations, they have revealed that the universe’s expansion is accelerating. While the cosmological modeling is a complex topic that will be covered in future blogs, the surreal fact is that with the high z methods, we have been able to track the distance of objects that are almost as old as the universe, which is estimated to be around 13.8 billion years old.

Viewing an object this far away, you're seeing so far back in time, that if you could see only a few thousand years more back in time, you would see the big bang. As a matter of fact, this is of primary interest to cosmologists who are motivated to learn about the big bang and early universe. This method of viewing back to the ancient universe is a cornerstone of observational High Energy Physics and, outside of large detectors and colliders, remains our best beacon of hope to understand the origin of the universe.

As for our alien friends looking in our direction, they would not see us and might never see us and we might never see them. Due to the expansion of the universe, we would recede from each other faster than the speed of light. Meaning that the photons trying to reach us are fighting for a lost cause. The ruthless expansion of the universe means that, despite being the fastest entity in the universe, their finish line is moving away from them faster than they can run. And this will continue to happen till the end of time.

And as always, keep on physicsing.


# Appendix

## Deriving the distance modulus

Astronomers use the **magnitude** scale, where a star appears *fainter* if its magnitude is *larger*. This comes from two facts:

1. **Magnitude–flux relation:**

$$
m_1 - m_2 = -2.5 \log_{10}\left(\frac{F_1}{F_2}\right)
$$

2. **Inverse-square law for brightness:**

$$
F(d) = \frac{L}{4\pi d^2}
$$

where L is the luminosity and d is the distance.

---

Now, let m be the apparent magnitude of a source at distance d, and M its absolute magnitude (i.e. what it would look like at 10 pc). Using the flux ratio:

$$
m - M = -2.5 \log_{10}\left(\frac{F(d)}{F(10\,\text{pc})}\right)
$$

Substitute the inverse-square law:

$$
m - M = -2.5 \log_{10}\left(\frac{L/(4\pi d^2)}{L/(4\pi (10\,\text{pc})^2)}\right)
$$

Simplify:

$$
m - M = -2.5 \log_{10}\left(\frac{(10\,\text{pc})^2}{d^2}\right)
$$

$$
m - M = -5 \log_{10}\left(\frac{10}{d}\right)
$$

Rearrange:

$$
m - M = 5 \log_{10}\left(\frac{d}{10}\right)
$$

And finally, writing explicitly with d in parsecs:

$$
m - M = 5 \log_{10}(d) - 5
$$

Thus, as d increases, the flux falls and m rises, making the star **fainter in appearance but larger in magnitude**.

---

## Example

**Problem:** A star has apparent magnitude m = 10 and absolute magnitude M = 5. Find its distance.

Start with the distance modulus:

$$
m - M = 5 \log_{10}(d) - 5
$$

Insert values:

$$
10 - 5 = 5 \log_{10}(d) - 5
$$

$$
5 + 5 = 5 \log_{10}(d)
$$

$$
10 = 5 \log_{10}(d)
$$

$$
\log_{10}(d) = 2
$$

$$
d = 10^2 = 100 \ \text{pc}
$$

---

**Sanity check:** At twice the distance (200 pc), flux drops by a factor of 4. Magnitude increases by 1.5. The star would look fainter with an apparent magnitude of 11.5, consistent with the magnitude definition.
