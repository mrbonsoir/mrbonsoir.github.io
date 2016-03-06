---
layout: post
title:  "Clash of the titans - optimization vs. machine learning"
date:   2015-04-15 12:17:06 +0100
categories: blog post
---
### In the beginning
What is important to know about machine/deep learning problems? First remark to myself is "what are we trying to solve in general?" and then "which method/technique do we choose?" or "which approach is most appropriate to answer a given problem?".

### Optimization for the people
Optimization is widely used to solve complex problems that don't have an analytic expression. But this doesn't mean that problems that have an analytic expression couldn't be solved using optimization.

Optimization relies on a provided model that "model" with reasonable efficiency a phenomenon (e.g. find the colorant combination of cyan, magenta, yellow and more for a give red, green, blue pixel) or anything you want. You may hear about derivatives, gradient, local minimum, cost function, quadratic form, linearity, non-linearity, iteration and more when you start messing around with optimization.

And it's completely possible to use optimization techniques as applied mathematics tools without knowing exactly how they work (e.g. you provide your model and the tools will perform the derivatives for you). In an engineering world you are connecting boxes, each one trying to solve a simple task taking for starting point what the previous is having for output.

### Deep learning for the people
Deep learning and neural networks let you do something clever with the way to solve your problem. First of all your problem has been defined and described, but optimization techniques did not provide expected results: it's not fast enough or it's simply not working. One possibility is that your model isn't good enough or way to complex.

The simple idea is to let a system to learn about an ecosystem. To do so we let the algorithms mimicking how our brain is working. The concept of learning is very important here because it is really what we want to achieve. We want that our algorithm learns in a first step by obtaining representative parameters/weights before giving us a result. Then once the learning is finished, for a given entree and with the help of the parameters the algorithm can give us answers. For example is this image an image of a car, an elephant and this with different degrees of confidence.

A big part of the learning is to prepare the training sample. You can't just give images to the algorithm. Applied to computer vision, deep learning methods try to extract features from images in a similar way of how we human recognize information in images. This step of features extraction goes by applying multiple filtering on the images and the resulting filtered images, using convolution and tile approaches. At the end you obtain classes of features and it's very similar to the filters used for face recognition. Only difference is the features that describe a human face are now almost standard and doesn't need to be computed or extracted again.

There exist competitions where for a given large database full of images and  keywords, people can submit their algorithms. Pretty interesting results are obtained and as in sport faster solutions are appearing often coming with new tools to handle large databases.

### Breaking the machine
Hopefully there is always something to improve. Because images can contain more than one object, you could have a bike and an elephant in the same picture. In that case what should reply our algorithm first? There is room for subjectivity here.

These algorithms have to deal with the constant stream of information we are processing, meaning that we are always learning - in theory of course because the world is full of lazy bastards which keeps the marketing and sales people happy making us predictable and therefore easy targets but I digress - and we have to find a way to give this ability to our algorithms or there is the risk for them to over-learn. I really like the metaphor of trying to make an algorithm able to forget part of what he is deep learning to be able to adjust its judgement.

The interesting problems are those that overcome the first limitations encountered. You could try to distinguish what are the elements in a picture (e.g. there is an elephant and a bike) or "simply" give to the image a score. If you take an artist, he will have the tendency not only to make the same picture but to add to its images something that defines the way he perceive the world around him, something pretty unique. A similarity factor or score can be very helpful when you are browsing a large image databases or "just" the internet.