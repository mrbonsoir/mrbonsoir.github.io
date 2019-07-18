---
layout: post
title:  "Color blindness for the people"
date:   2019-07-15 9:22:06 -0500
categories: blog post
---

## Introduction
In that post I want to show you two things, one is a kind of *behind the scene tour* of a work I have done on color blindness at my work last year, secondly how do we go from the problem to a prototype, what were the tools that we used during prototyping.

The work of a scientist is to observe phenomena, possibly to understand and to explain them. Ideally you want to be able to recreate an observation with the right parameters such that you can offer some kind of solution. In our example the phenomenon is color blindness or color vision deficiency (CVD). We want to be able to modify images such that human with CVD can access the same information as people with normal vision.

As we don't have on demand test persons that are color blind we need to use color vision model to simulate how such personns will see the world with their colors. Different color vision models and CVD exist, meaning one type of CVD can be simulate differently.

I did mention prototyping, we will have a look at the transformation applied to the images to perform those CVD simulations. It's mostly matrix transformation. I used, wait for it, Python programming language for that.

## Color blindness
A good start is to look at the wikipedia page on [color blinbness][CVDwiki-link]. The eye has three cones acting as light sensors called LMS for **Long**, **Medium** and **Short** wavelengths. A *popular* type of CVD is a missing or misplaced cone resulting in a modified processing of the signal once received and transmitted to the brain.

Already a choice can be made on *where the deficiency starts* that will influence the simulation of an image viewed by a person with CVD. Some simulation will stop at the **LMS** level, meaning the projection of the signal on the cone space and other with go further and integrate how the signal is modified and pre-processed for the brain.

For the rest of this post we will remain in **3D** space, work in **LMS** and **RGB** color spaces. This will be convenient for the CVD simulations.

### CVD with one LMS cone missing
The most simple and straightforward approach is to consider one of the **LMS** cones missing. If the image is displayed in 3D space where the axis are the **LMS** cones, having one missing cone come done to have a reduced volume of color in 2D. The challenge being to defined this reduced volume.

If we assume that the reduced volume has been defined we need to do: RGB -> LMS -> L'M'S' -> R'G'B' to get the simulated version of the image as it was seen by a color blind person:
+ RGB -> LMS we convert an image pixel from RGB to LMS space using matrix operation
+ LMS -> L'M'S  is where we map all points to the reduced gamut corresponding to a defined CVD, it's a matrix operation
+ L'M'S' -> R'G'B' we convert back the image pixels to RGB color space to see the result of the simulation and it's a matrix operation as well

### Some code
A glimpse of code how to simulate how an image will look to person with CVD.

```
import numpy as np
import matplotlib.image as image
img_rgb = image.imread('some_image.jpg') # numpy array (n x m x 3)

# RGB to LMS
img_lms = np.einsum("ij, ...j", rgb2lms, img_rgb)
# where rgb2lms is a 3x3 matrix to go from RGB to LMS.

# LMS to modify LMS (it changes with the CVD to simulate)
img_lms_mod = np.einsum("ij, ...j", lms2lms, img_lms)
# where lm2lms is a 3x3 matrix to go from LMS to L'M'S',
# it changes with the type of CVD.

# LMS to RGB
img_rgb_mod = np.einsum("ij, ...j", lms2rgb, img_lms_mod)
# lms2rgb is a 3x3 matrix to go from LMS to RGB.
```

In the lines above we simply multiply each vector (a pixel in **RGB** or **LMS** space) by a 3x3 matrix. I invite you to check the [np.einsum][einsum-link] function which is an amazing tool for matrix operation.

### Some examples
Below five images modified using the code above. First line the original images, then protanopia, deuteranopia and tritanopia simulations. The images selection represents natural (column 2 and 4) and art (column 1, 3 and 5) content.

![](/data/imMontage.jpg)

### Missing, misplaced and more advanced CVD simulation
The previous model is convenient, easy enough to compute but lack degrees of CVD strength. There are different flavours of CVD, meaning all the people are not color blind the same. Identicaly for people with normal vision they don't all have the same exactly cone responses, but the average spectral sensitivy per cones has been measured and is heavily employed in color science, check the wiki page on the [CIE 1931 color space][CIE1931-link] for more information.

In a bit more complex approach, the reduced color volume is not a 2D plan but a reduced volume in 3D. So to simulate different strenght of CVD we need another approach to compute this volume.

The approach proposed by [Machado, Oliveira and Fernandes][MachadoColospacious-link] can simulate different strenghts of CVD from partial to total. The strenght is expressed by moving the peak of sensitivy of the chosen deficient cone (there is a bit more than that but it's basically that). Because the cones response is wired in such a way that an intensity and chromaticity information is transmitted to the brain, changing the peak sensitivies require to use a more advanced [color vision][ColorVision-link] model. At the end new RGB values can be obtained by a matrix operation and code implementation is available in the [Python module Colorspacious][colorspacious-link].


### Some examples
The image below are organised as those shown above. Only difference is they processed using the [Colorspacious][colorspacious-link] code using a CVD factor of 80 where 100 means full CVD as in the first series of images.

![](/data/imMontageMachado.jpg)

## Discussion
There is an extensive and interesting list of references on the topic, from CVD simulation, CVD test evaluation in order to find out if you are color blind and to which degree, image modification for better visual comfort to people with CVD, human color vision model... Depending of the problem you are trying so solve you will use this or this vision model to test your approach.

One very important aspect which is not taken into account here is how the brain is processing the signal once the cones have received it. Reducing the vision system of the common deuteranomaly, protanomaly and tritanomaly as view of the world in *2 colors* is a crude approximation. Assuming someone is color blind, when he/she sees leaves in something else than expected green (e.g. when the simulation transforms an image of a tree with green leaves into something not green at all) doesn't mean that person does recognize a tree with leaves.

Problems can really arise with someone looking at graphical information, some not natural content, e.g. a map with saturated colors where the textual information simply dissolve in the background (once we simulate this image information for different type of CVD). In that type of configuration it will be interesting to modify part of the image content to avoid the lost of information.

## More reading to go into CVD in depth
Below a non exhausitve list of article which are interesting to explore the topic:
+ [Computerized simulation of color appearance for dichromats (1999)][computeSimu-link]
+ [Corresponding-pair procedure: a new approach to simulation of dichromatic color perception (2004)][correspondingPair-link]
+ [Real-Time Temporal-Coherent Color Contrast Enhancement for Dichromats (2010)][RealtimeTemp-link]
+ [Mitigating Color Dificiency in Graphical Display (2018)][MitigatingColor-link]

[correspondingPair-link]:https://www.semanticscholar.org/paper/Corresponding-pair-procedure%3A-a-new-approach-to-of-Capilla-D%C3%ADez-Ajenjo/a14e7cce4da19c65f8a5ebfa12501cb981b87dc3
[MitigatingColor-link]:https://onlinelibrary.wiley.com/doi/abs/10.1002/sdtp.12152
[RealtimeTemp-link]:https://www.semanticscholar.org/paper/Real-Time-Temporal-Coherent-Color-Contrast-for-Machado-Neto/78cc2c83aa52a6b01aa31e5eff9f7793081328e6
[computeSimu-link]:https://www.semanticscholar.org/paper/Computerized-simulation-of-color-appearance-for-Brettel-Vi%C3%A9not/bd7a98c1eaf3d7f83335629e80040138f0eecfc4
[einsum-link]:https://docs.scipy.org/doc/numpy/reference/generated/numpy.einsum.html
[IRYStec-link]:http://www.irystec.com/
[CVDwiki-link]:https://en.wikipedia.org/wiki/Color_blindness
[ColorVision-link]:https://en.wikipedia.org/wiki/Color_vision
[MachadoColospacious-link]:https://colour.readthedocs.io/en/develop/colour.blindness.html#machado-oliveira-and-fernandes-2009
[colorspacious-link]:https://colorspacious.readthedocs.io/en/latest/
[CIE1931-link]:https://en.wikipedia.org/wiki/CIE_1931_color_space/
