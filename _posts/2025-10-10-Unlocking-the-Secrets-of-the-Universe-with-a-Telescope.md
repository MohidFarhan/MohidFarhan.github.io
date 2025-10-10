---

title: "Blog 6: Unlocking the Secrets of the Universe with a Telescope"
date: 2025-10-10
categories: [Astronomy, Cosmology, Astrophysics, Modern Physics, Atomic and Molecular Physics]
use_math: true
layout: single
author_profile: true
read_time: true
comments: true
excerpt: "A telescope is humanity’s window into the cosmos, transforming distant light into insight about the universe’s hidden structure and origin."


---

## Introduction

In today’s blog, we will explore how light carries the universe’s secrets, and the ingenious ways astronomers decode them. You will need a basic understanding of light’s dual nature, photon emission and absorption, and a few ideas from modern physics. Together, we will see how telescopes turn simple photons into profound knowledge once thought unreachable, even by the brightest minds.

Let's first understand what "light" is. In most cases, "light" refers to an entity that illuminates our surroundings by reflecting from surfaces, into our eyes, which the brain pieces together to form the images that we see. We utilize this exact property through telescopes, when we point them towards celestial objects.

## What is light?

Put simply, visible light is basically electromagnetic radiation, with a narrow range of wavelengths (400-700 nm). Our eyes are effective filters that dial out all radiation that does not adhere to this narrow window.  
However, a telescope has no such constraints, as it can see all electromagnetic radiation. This radiation can be thought of as quantized packets of energy called photons, which is also a very useful definition for our purposes. These photons are massless and do not interact with each other, but can be emitted, absorbed or transferred. 
But how useful can a collection of photons be? Sure, you can see stuff like stars and galaxies, but is that it? Is it possible to find the velocities, radii, temperature, chemical composition or anything of that sort? Or is it just photons bouncing off stars that take forever to reach us, and maybe lose all that information while doing so?

## The Miracles of a Telescope

Well, by leveraging no more than a few lenses and a metallic structure, we can manipulate these pesky photons into confessing so many secrets of the universe.  
I will not get into the structure of a telescope and/or its types. The layman definition of "a telescope helps us see stuff that is far away by collecting a lot of light" is enough for this blog. So, you can think of it as a device which registers the falling of photons on its lens. I have had the opportunity of using telescopes during an internship in the National Center for GIS and Space Applications (NCGSA), where I had unrestricted access to their 10-inch telescope. I will tell you everything I learned.

## Astrophotography

The most obvious use of a telescope is to take high resolution images of the cosmos, referred to as "astrophotography". There exist specialized software for different requirements, and one can use whichever serves their purpose. But the task is not as simple as sticking a DSLR onto the eyepiece (the thing with which you see through the telescope) and snapping a picture. Although that works decently for instagram friendly pictures which can be heavily edited to look cool and attractive, they suffer from unwanted noise in the image and become unauthentic due to excessive editing. 

This is why seasoned astrophotographers take 4 types of images: Darks, flats, biases and lights. Think of them as ingredients of a cake. 

Lights: These are the actual images of your target, the "flour" of our cake. You take long-exposure photos to gather as many photons from a distant celestial object as you can. But these aren't perfect; they're mixed with noise. We take as many of these as you can. The more light frames you have, the better your final signal-to-noise ratio will be.

Darks: This is the "salt," the unwanted side effect of the long exposure. Even with the lens cap on, your camera's sensor heats up and creates thermal noise, showing up as "hot pixels" and grainy static. Dark frames are taken to measure and remove this specific type of noise. These are taken with the lens cap on and must have the exact same exposure time and temperature as your lights. Since dark noise is dependent on heat and time, these two variables must be controlled. It is instructive to take around 20-30 of them.
     
Biases: The "baking soda," a fundamental ingredient you can't get rid of. This is the baseline electronic noise from your camera's sensor just by being turned on and reading out its charge. It's always there, no matter the exposure time. We take bias frames to measure this constant electronic hum.  These are also taken with the lens cap on, but with the fastest possible shutter speed your camera allows (e.g., 1/4000s). Since bias noise is constant, you can take these at any time, but it’s a good idea to take them at the same temperature.

Flats: The "sugar", used to balance the flavor. These frames capture the unevenness in your optical system. This includes dark corners (vignetting), or tiny dust specs on your lens or sensor. Flats are used to correct for these imperfections. These are taken with an even source of light. You can do this by using a flat panel, or by covering your telescope with a white t-shirt and pointing it at a uniformly bright sky at dawn or dusk. The key is to take them with the exact same focus and optical setup as your light frames.

## Integration of Images

Now that we have all the ingredients, it's time to "bake" the perfect image in software. This is where a program like Siril shines. It takes all your frames and performs a series of calculations to remove all the noise and flaws, leaving you with a clean signal.

The general process is a series of subtractions and divisions. Siril first creates "master" frames by averaging all of your darks, biases, and flats. This averaging removes random noise from the calibration frames themselves, giving you a very precise map of the unwanted signals.

Then, Siril performs the magic with this equation:

$$
Calibrated \hspace{0.1cm}Light=\frac{
(Light\hspace{0.1cm}Frame -  Master\hspace{0.1cm}Dark) − Master\hspace{0.1cm}Bias}{(Master\hspace{0.1cm}Flat − Master\hspace{0.1cm}Bias)}
$$

It sounds complex, but it's just commands through code, directing the software to:

Remove the thermal noise: Subtract the Master Dark from each Light Frame. This gets rid of the heat noise and hot pixels.

Remove the baseline noise: Subtract the Master Bias from the result. This removes the fundamental electronic noise.

Correct for dust and vignetting: Divide the entire result by the difference of the Master Flat and Master Bias. This corrects for uneven illumination and dust spots, giving you a smooth, evenly lit image.

After this process, Siril stacks all of your calibrated light frames together. This stacking process is what dramatically improves the signal-to-noise ratio, revealing the faint details of the cosmos. By carefully following this procedure, we take a collection of noisy, flawed images and turn them into a single astrophotograph that truly shows the universe as it is.

Be advised: you can use any software, but my recommendation is Siril due to its user-friendliness and straightforward processing. Here are a few images taken by our internship team after processing in black and white: 

## The Seahorse Nebula (1200 light-years away)

![Figure 1](/assets/images/Fireworks.PNG)

## The Dumbbell Nebula (1360 light-years away)

![Figure 2](/assets/images/dumbell.PNG)

## The Eagle Nebula (7000 light-years away)

![Figure 3](/assets/images/EN.png)

## The Trifid Nebula (5200 light-years away)

![Figure 4](/assets/images/Capture.PNG)

## The M13 Globular Cluster

![Figure 5](/assets/images/M13.png)


## Close Range Astrophotography

 While taking pictures of relatively closer bodies, like planets in our solar system, we used more specialized software like PIPP and Registax. PIPP is a program we used to stack images to, in our case, be processed by registax. You can convert a video of an object moving through space, to a set of frames where the planets is aligned in a place of your choosing. This is a free and effective way of ensuring maximum results with minimum noise. 
 
 Then, registax uses the set of frames created by PIPP, discards the poor frames where noise is abnormally high, and with the application of filters tuned for close-ranged astrophotography, gives us a satisfactory final image. When we peered through the telescope to a planet like Jupiter or Saturn through our telescope (10-inch), it is a very small dot. The magic of the aforementioned process gives us zoomed in images that are edited for authenticity.

 Here are some of the photographs we took, with minimal editing:

## Jupiter

![Figure 6](/assets/images/Jupiter.png)

## Saturn

![Figure 7](/assets/images/Saturn.png)

## What else can we know?

A collection of photons can give us much more than just images. We will now take a look at spectroscopy. By attaching a diffraction grating to a telescope and pointing it towards an object, you can obtain streaks of light alongside an object. That streak is basically a bar-code, because not only does it look like one, it is also unique for almost every object in the universe, which i will explain. Note that this is an amateur's setup, and for research-grade observations, you need spectrographs and more complex arrangements. But in our internship, we improvised! 

As the light from the star passes through the grating, it is diffracted into a spectrum. Instead of a single point of light, you'll see a streak of colors, with the star's light in the center and a spectrum extending to the sides, looking like and quite literally acting like a bar-code you would see on a Nutella jar you'd buy from Walmart. 

This bar-code is essentially photon intensity as a function of wavelength. So it tells the numbers of photons of a particular wavelength striking the lens, extended for a large range of wavelengths, if given a long enough exposure time. 

## Interpreting the Cosmic Barcodes

This bar-code is a plot of the intensity (photon population) on the y-axis with wavelength on the x-axis. Let's understand how that is useful.

![Figure 7](/assets/images/HD.png)

This is what ypu get when you point it towards something hot, dense and luminous. But, point it towards empty space in the universe, with a sensitive enough spectrograph and you would obtain a Planck distribution that peaks at a particular wavelength. 

This would be a continuous, uniformly bright line if it were pointed towards a hot and dense object. We call this a continuous spectrum. A continuous spectrum is produced by a hot, dense object, such as the filament in an incandescent light bulb or the core of a star. In these environments, atoms are packed so tightly that their energy levels overlap and smear out. As a result, they emit light at all wavelengths, creating a smooth, continuous band of colors without any specific lines or dips.

![Figure 8](/assets/images/CMB.png)

What is this about !?!

Now, I will use two of the most simplest formulas in physics to give you a ball-park estimate of how wavelength can be connected with temperature The energy of a photon can be given by:

$$
E=\frac{hc}{\lambda}
$$

where $$\lambda$$ is the wavelength,
and this energy can be related to temperature in a statistical relation:

$$
E=k_BT
$$

where $k_B$ is the Boltzmann constant. Equating the two above equations gives us:

$$
\frac{hc}{\lambda}=k_BT
$$

and solving for Temperature:

$$
T=\frac{hc}{\lambda k_B}
$$

This gives you a good back-of-the-envelope estimation of how temperature can be reinterpreted as a function of temperature. 

Now that you have an intuition, we can move to a precise method which is the Wien's displacement law:

$$
T = \frac{b}{\lambda_{\text{max}}}
$$

which is basically the same thing, but the constant b absorbs all the constants in the previous estimation in a manner that is more consistent with experiment, with the emergent value being:
$$
b=2.898 \times 10^{-3} \hspace{0.1cm}m⋅K
$$

A very accurate spectrograph will give a value of $$\lambda$$ to be 1.06mm. With simple value-plugging you find that $T=2.7K$. Does that value ring a bell?

It should, because you have picked up the Cosmic Microwave Background, and this is the temperature of universe! Is that not insane? We have measured the temperature of the UNIVERSE using O levels physics. The same analysis can be done when you zoom into a star or any other object, that's how powerful the simplest formulas of physics are, now imagine the secrets that more complex formulas can bring. And we are not done yet...because I have not even started the bar-code part yet. 

This argument should also make it clear as to why all stars of the same spectral types have the same temperatures: since their peaks are on similar wavelengths.

## Spectral Dips

I pointed the 10-inch telescope, with attached grating,  to Saturn and using a software called BASS Spectrum, I obtained the following graph. 

![Figure 8](/assets/images/SaturnSS.png)

What are these dips? To understand that, we also need simple high-school-level physics knowledge (or A-levels physics at best). We need to interpret what a dip implies at first.

A dip in this context is a sudden drop of intensity for a particular wavelength, meaning that for some reason, less photons of that particular wavelength reach the lens of our telescope. Let's keep this in the back of our minds and move to O-levels chemistry now.

Let's think of the simplest atom we know: the Hydrogen atom: an electron orbiting a proton. Now, we know that the ionization energy is the energy required to remove the electron, situated in the ground state. We know that the electrons reside in shells, and to move from one shell to the other, they must receive a very particular "push",and if the push is too hard or too small, and the electrons can't leap from one shell to the next. Shells can also be interpret as quantized energy levels, and the quantization implies that the energy absorbed by the electron must have an exact value to transition from one shell to the next.

Now, the change in energy between shells can be calculated from the Rydberg's relation.

$$
\frac{1}{\lambda} = R_H \left( \frac{1}{n_1^2} - \frac{1}{n_2^2} \right)
$$

where:

$$\lambda$$ is the wavelength of the emitted or absorbed photon, $$R_H$$ is the Rydberg constant for hydrogen, with a value of approximately $$1.097 \times 10^7 \text{ m}^{-1}$$, $$n_1$$ is the integer representing the final energy level and $$n_2$$ is the integer representing the initial energy level, where $$n_2 > n_1$$.

So this implies that if the electron is to receive a photon of some highly specific wavelength $$\lambda$$, it would jump from shell $n_1$ to $n_2$, and the most crucial implication is that this wavelength is different from every transition and for every atom. And we can leverage this fact, and use it to develop fingerprints of atoms.

## Let's Back Track

Now, back to the mystery of the missing photons, or the systematic absence of photons with a particular wavelengths. See how the pieces piece together?

Those missing photons are not coincidence, but fulfill the exact wavelength needed for transitions of electrons between shells, so instead of reaching the lens of our telescope, they get absorbed by the atoms comprising of the object that we are observing. 

And since this wavelength is different for every shell changes for every atom, it's an effective unique ID given to every single atom in the universe. One can look at the wavelength on which the dip occurs, enter it into the database and know what type of the atom is the culprit! 

I found this absolutely incredible and the fact that we never even touched college-grade physics makes it even more insane. The impact to simplicity ratio of this method is probably the highest I have seen in any of the methods so far. 

## Spectrum of 68 Draconis

We also obtained a spectrum of 68-Draconis, which is a star in the Draco constellation. Now the graphs that I obtained begins to make sense, and you might notice a very prominent dip at $$\lambda=656nm$$. This wavelength exactly corresponds to the equivalent energy required for an electron in the hydrogen atom to move to shell n=2 to n=3. So while I took the readings, the hydrogen atoms of Saturn (with electrons in their second shell) absorbed some of the photons with wavelength of 656 nm, and the lens of the telescope felt this change, by registering fewer photons of that exact wavelength. Moreover, this magnitude of the dips also make it easy for us to estimate the composition of elements comprising of the Saturn. Most of it, understandably, is hydrogen and helium as they are the most abundant atoms in the universe and hydrogen's spectral lines are of particular interest to an astronomer.

Obviously, the same technique can be applied to study any celestial object and their chemical composition, making this one of the most powerful techniques in all of physics. 

We can also determine recessional velocities of objects by using the same technique. We have discussed cosmological redshift in blog 4: it is a process in which the photons being emitted from distant objects have their wavelengths shifted towards the red region (increased) due to the recessional velocity of the objects from Earth. The cause of this redshift is discussed in blog 3 so feel free to read through that if you haven't already. This means that the entire spectrum is shifted to the right, and by measuring the amount of this shift, we can determine that change in wavelength and, hence, the corresponding recessional velocity. However, one needs a very good telescope and/or noise pollution-free skies to see the incredibly shuttle shift in wavelength, and our humble  equipment fails us here, despite attempts. It remains a work in progress, and through this blog series, I will keep you updated. Until next time, keep on physicsing.
    


 

 

        
