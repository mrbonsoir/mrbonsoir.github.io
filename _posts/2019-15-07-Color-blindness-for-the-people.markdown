---
layout: post
title:  "Color blindness for the people"
date:   2019-07-15 9:22:06 -0500
categories: blog post
---

## Introduction
In that post I want to show you two things, one is a kind of *behind the scene tour* of work I have done on color
blindness at my work last year, how do we go from the problem to a prototype, secondly what were the tools
that we used during prototyping.

The work of a scientist is to observe phenomena, possibly to understand and to explain them. Ideally you want
to be able to recreate an observation with the right parameters such that you can offer some kind of solution. In
our example the phenomenon is color blindness or color vision deficiency. We want to be able to modify images
such human beings with defined CVD can access the same information as people with normal vision.

As we don't have on demand test persons that are color blind we need to use color vision model that will modify
a given image to make it *look* as it was seen by a color blind person. Different color vision models exist meaning
the same image can be simulated differently.

I did mention prototyping, so we will also have a look on the transformation applied to the images. It's mostly matrix transformation
and different approaches, implementations are available. I used, wait for it, Python programming language for that.

## Color blindness
A good start is to look at the wikipedia page on [color blinbness][CVDwiki-link]. The eye has three cones acting as
light sensors called LMS for Long, Medium and Short wavelengths. The most *popular* CVD being a missing, misplaced cones resulting
in a modified processing of the signal once received and transmitted to brain. Already there a choice can be made on the
where the deficiency starts that will influence the simulation of an image viewed by a person with CVD.

### One LMS cone missing
The most simple and straightforward approach is to consider one of the LMS cones missing. If the image is displayed in 3D space
where the axis are the LMS cones, having one missing come done to have a reduced volume of color in 2D. The challenge being to
defined this reduced volume.

If we assume that the reduced volume has been defined we need to do: RGB -> LMS -> L'M'S' -> R'G'B' to get the simulated version of
the image as it was seen by a color blind person.

### Some code
A glimpse of code how to simulate how an image will look to person with CVD.

```
import numpy as np
import matplotlib.image as image
img_rgb = image.imread('some_image.jpg') # numpy array (n x m x 3)

# RGB to LMS
img_lms = np.einsum("ij, ...j", rgb2lms, img_rgb)

# LMS to modify LMS (it changes with the CVD to simulate)
img_lms_mod = np.einsum("ij, ...j", lms2lms, img_lms)

# LMS to RGB
img_rgb_mod = np.einsum("ij, ...j", lms2rgb, img_lms_mod)
```
In the lines above we simply multiply each vector (a pixel in rgb or lms space) by a 3x3 matrix. I invite you to check the [np.einsum][einsum-link] function which is an amazing tool for matrix operation.

### Some examples
Below five images modified using the code above. First line the original images, then protan, deuteran and tritan simulations. The image selection represents natural (column 2 and 4) and art (column 1, 3 and 5) content.

![](/data/imMontage.jpg)

### Missing, misplaced and more advanced CVD simulation
The previous model is convenient, easy enough to compute but lack degrees of CVD strength. There are different flavours of CVD, meaning all the people are not color blind the same (the same as we don't all have the same exactly cone responses). In a bit more complex approach, the reduced color volume is not a plan in 2D but a reduced volume in 3D.

The approach proposed by [Machado, Oliveira and Fernandes][MachadoColospacious-link] is available in the Python module [Colorspacious][colorspacious-link]. It allows to simulate different degrees of CVD, from partial to total. Here as well the new RGB values can be obtained by a matrix operation. And there are a few example in the previous link.

### Some examples
The image below are organised as those shown above. Only difference is they processed using the [Colorspacious][colorspacious-link] code using a CVD factor of 80 (where 100 means full CVD as in the first series of images).

![](/data/imMontageMachado.jpg)

## Discussion
There is an extensive and interesting list of references on the topic, from CVD simulation, CVD test evaluation in order to find out if you are color blind and to which degree, image modification for better visual comfort to people with CVD, human color vision model... Depending of the problem you are trying so solve you will use this or this vision model to test your approach.

One very important aspect which is not taken into account here is how the brain is processing the signal once the cones have received it. Reducing the vision system of the common deuteranomaly, protanomaly and tritanomaly as view of the world in 2D colors is an approximation. Assuming someone is color blind, when he/she sees leaves in something else than expected green (when the simulation with the approach as in the code above gives us something unusual for color) that person will still sees a tree with leaves.

Problems can really arise with someone looking at graphical information, e.g. a map with saturated colors where the textual information simply dissolve in the background. In that type of configuration it will be interesting to modify part of the image content.

[einsum-link]:https://docs.scipy.org/doc/numpy/reference/generated/numpy.einsum.html
[IRYStec-link]:http://www.irystec.com/
[CVDwiki-link]:https://en.wikipedia.org/wiki/Color_blindness
[MachadoColospacious-link]:https://colour.readthedocs.io/en/develop/colour.blindness.html#machado-oliveira-and-fernandes-2009
[colorspacious-link]:https://colorspacious.readthedocs.io/en/latest/
