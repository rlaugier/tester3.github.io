---
title: Asgard/NOTT, the first Nuller of the VLTI
author: Romain
date: 2026-05-01
categories: [Research themes, Fundamental instrumentation]
tags: [instrument, nulling, exoplanets]
render_with_liquid: false
math: true
---
## Introduction

Asgard is a new visitor instrument currently under commissioning at the VLTI. Asgard assembles in the same system a number of different novel instrument concepts. Bifrost is the short-wavelength high-spectral dispersion combiner, led by Stefan Kraus. NOTT is the L-band nulling beam combiner and will become the first specialized high-contrast instrument of the VLTI.

NOTT is designed to reach contrasts of up to $10^{-5}$ and therefore become sensitive to young giant exoplanets around nearby stars. Due to its extreme angular resolution capabilities, it may even be able to detect and characterize some mature hot jupiters.

In addition to exoplanets, NOTT should also be able to detect the light from hot zodiacal disks around mature stars. 

## Nulling interferometer

In the past years, interferometry has succesfully offered a path to extract information at angular resolutions smaller than what is available to a regular telescope. This has been done using the relationship formalized in the Zernike-von-Cittert theorem, which links the visibility of fringes in the recombination of two light beams collected from differente locations to the complex amplitude of the intensity distribution of the source. This resulting signal is proportional to the contrast between the star and the planet, in such a way that uncertainty associated with the measurement of starlight affects the measurement. This leads to photon noise of the bright star, as well as the stellar variability both weigh in on the scale of the signal to noise ratio. This results in fundamental and practical limits existing on the sensitivity to planetary companions to nearby stars.

Nulling interferometry goes around this limitation by setting aside the starlight, sending it to so-called bright outputs, and recording off-axis light at so-called dark outputs, where little or no starlight is present. This is done by adjusting the optical path and phase of the beams at the inputs of the combiner so that on-axis light interferes constructively on the bright output, and destructively on the dark outputs.

The capability to control the phase of the incoming beams is pivotal to obtain meaningful measurements and this is why nulling interferometers have been so rare in the past. However, with interferometric instruments such as GRAVITY demonstrating fringe-tracking capability at and below 100nm RMS, current infrastructures should now enable the proliferation of nuller.

Within Asgard, the fringe tracking is provided by the Heimdallr module which works in the K band. Wavefront quality and fine pointing control are also crucial to the quality of nulling measurement. Within the Asgard suite, these roles are filled by Heimdallr and Baldr.


## Technical innovations

NOTT innovates on many aspects. Here are a few **to which I was able to contribute**:

### Integrated optics

Integrated optics are like integrated circuits built for optics rather than electronics. They are made of waveguides similar to optical fibers drawn inside of slab of glass. Their pattern brings light from the different telescopes together to interfere and carries the result of the combination to outputs on the other side of the chip. From there, the light propagates freely to a spectragraph which disperses the light from the outputs onto an infrared detector.

Compared to a bulk optics solution, integrated optics are extremely compact. This compactness makes it easier to fit the whole combiner into a cryostat, therefore reducing the thermal emission of the component. More importantly, it allows for an extreme stability of its function.

Since the waveguide only carries a single mode, they also act as a spatial filter for the instrument, defining its field of view.

### Injection system

Injecting light into a single-mode waveguide is never trivial. Most integrated optics instruments, (PIONIER, GRAVITY) first inject light into single mode fibers which are then brought together against the front of the chip. However, there are few options for optical fibers in the infrared, and they are mechanically very fragile. For this reason NOTT is using the less common approach of injecting directly into the integrated optics chip.

To this end, all four beams are focused by OAPs onto slicer. This faceted mirror brings the pupils of the four beams together, while their image spots are separated by a fixed distance. This common beam is then collimated and enters the cryostat where an injection lens produces four images at the entrance of the integrated optics chip for the light to excite the modes of the waveguides and be guided for recombination. The faces of the slicer are convex in order to bring the instrument's pupils into focus at the cold stop.

### Atmospheric dispersion

Like any instrument observing from the ground, Asgard/NOTT is sensitive to the dispersion of air. In the general case, the beam of light entering an instrument propagates through the layers of the atmosphere. When it is collected by the instrument, this creates an imbalance across the beam, as the wedge of ground-level air is thicker in some parts of the beam than in others. In an imager, this disperses the light, creating little spectra instead of perfect images.

In the case of an interferometer, this so-called transverse dispersion effect is also accompanied by a longitudinal effect from one beam to the next, created by air inside of the delay lines and transport tunels. In the L band, the transverse dispersion is small enough to be neglected. However, the longitudinal dispersion can add up to more than 100m of ambient air replacing the vaccum of space.For most interferometers, this is compensated by adding to each beam a pair of glass prisms sliding in front of one another and creating a variable length of glass.


Due to its nature as a nuller, NOTT requires a control of input phase across the full spectral range. The resonance of $$CO_2$$ at $$4.3 \mu m$$ creates a unique, strongly wavelength dependent signature in phase, which cannot be corrected with glass prisms. To correct for this, the NOTT is equipped with optical chambers of variable length in which $$CO_2$$ gaz is held, which can compensate exactly for more than 100m of the atmospheric gaz, in its present day concentration. NOTT will be the first instrument to use this method to control atmospheric dispersion.

> *Update from July 2026:* This image shows the NOTT LDCs during their integration in Leuven. The rubber belows containa atmospheric-pressure $$CO_2$$ and can exchange their content to adjust the length of gaz seen by the beams.\\
> ![A view of the NOTT LDCs](/assets/img/ldc_naked.jpg){: width="600" }


> Please contact me via email.
{: .prompt-tip }
