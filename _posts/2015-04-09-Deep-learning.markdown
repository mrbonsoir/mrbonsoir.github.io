---
layout: post
title:  "Deep learning (ou deep learning in French)"
date:   2015-04-09 12:28:06 +0100
categories: blog post
---

### What was your question already?
How to explain deep learning to your friends, family members, neighbors, random stranger, dog? A very good question indeed. Rather than going deeply into neural networks and other festivities let's start with describing the problem we want to solve or at least let's give an example of what we are trying to do here.

Over the years I had to come with strategies if I wanted to explain what I do for living. Telling combinations of words such as "color science", "computer vision", "image processing", "digital photography" is usually not enough or saying "I do work with images" neither. I always found interesting to answer the question "why to you want to do that?" or "which problem do you want to solve?" instead of saying I'm this or that. So to explain what I can do I try to give an idea of the tasks I have to solve.

### What is the problem you are trying to solve already?
In some way asking these questions is already machine learning/deep learning-ish approach of solving a problem. In theory if someone asks you to solve a problem he knows the kind of results he want to obtain for a given input or starting point. What he doesn't know is what is happening between these two stages. Applied mathematics and optimization are a reasonable standard solution: you develop of model that recreate more-less accurately what is happening between these two stages, then for a new entree point your model will predict what an output will be.

I'm sure *big data* is an expression you have heard in the past years or months. It has of course different meaning depending who is giving a definition. But, coming back to images and the incredible amount of images we are producing daily there is a need to develop solutions/tools to be able to interact with these images. You have in your hand an extremely large image database and using keyword as a search query isn't enough anymore. Here is the problem: how to navigate, how to browse into large image database in a more natural way? There is a bit of database here but that is not the main point of my article, check my past post on graph and database if you are interested.

### Face recognition to recognition of everything
Working with images is fascinating, you see one image and automatically you extract some of its  information. Of course there is a long learning curve, when you see a tree, a car, a known object in a picture you don't even realize it, you know, you have learned over the years you spent on earth to recognize, categorize, organize the continuous stream of visual information that come to your eyes and is later processed in your brain.

If you think of face recognition, the mathematical tools are now pretty standard. We can with high probability find out faces in images, classification comes after the recognition. And if you train your model you will be able to recognize semi automatically in a database faces of different persons as the tools/filters can be tuned for a given target. It can be scary of course if the threshold that decide for a true recognition/classification isn't verified by a real human and that action leads to a rocket launch. Actually any automatic action issued from an algorithm decision having impact on a human being is pretty bad (hello mass surveillance and hello Terminator). You want help from robots not to help robots or it's too late anyway.

<iframe src="https://player.vimeo.com/video/12774628" width="500" height="477" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
<p><a href="https://vimeo.com/12774628">OpenCV Face Detection: Visualized</a> from <a href="https://vimeo.com/adamhrv">Adam Harvey</a> on <a href="https://vimeo.com">Vimeo</a>.</p>

An idea behind deep learning is to be able to learn what are into images - in a similar way as we human do - to extract features and to perform tasks on other images based on a trained neural network. I'm making shortcuts but that's the idea. To understand and to later mimic how information is circulating into the brain has been a dream of many researchers. Neural networks go into that direction. If a few years ago the algorithms were limited because of computer power the global picture is different now.

What is also interesting is that new strategies had to be developed to overcome the overload of data. In a way the systems were "over learning" and people talked about over-fitting the data. And it makes sens. If I'm not too mistaken our brain is not indefinitely expandable, meaning we are sorting information continuously. One big part of these tools is to perform drop-out which can be explained as "now that our system can learn we have to teach him to forget part of what he knows in real time".

### Cross disciplines 
A chance I see - for me - is the need in some industries for expert being not only expert in one field. Specially for this kind of large scale problems involving images, computer vision, real time and fancy applied research projects. To know only about machine learning or statistic is not enough, to know both about computer and machine learning tools is better.


