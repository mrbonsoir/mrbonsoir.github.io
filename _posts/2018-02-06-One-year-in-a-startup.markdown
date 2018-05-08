---
layout: post
title:  "One Year in a startup"
date:   2018-02-06 9:21:06 -0500
categories: blog post
---

## A year already

One year in the same company, two countries and many more new stuffs learned during that time.

Let's re-introduce myself. I'm a color scientist and I have worked on various projects in the past 10 years, all of them having in common a signal to be processed, often the signal being an image visible by a human observer.

I'm doing now r&d in a startup in Montréal, working on image quality and perceptual display. Being in a startup with experienced colleagues is a pretty good setup.  

On one side learning and improving an algorithm to improve image quality. The research point of view allows you to optimize, implement this algorithm. The goals are image quality and feasibility. You take your Matlab, your python, your pen and paper, process images, compute differences, eventually run psychophysic experiments, anything that can be done not in real time.

On the other side, as I said I'm working in as startup ([IRYStec][IRYStec-link]) and the challenge is to be able to quickly port a research project into production. Running your algorithm on your desktop computer is different than running it on a portable device in real time with more than one display technology... But that's where it's interesting too and that's where you/I learn new stuffs.

## Keep learning

Interesting because you have to learn new tools, here programming tools like openGL in order to program shader, re-think your algorithm for applying it in real time on a different hardware. And usually it's less powerful than what you were used too... But it can help because it forces you to tackle your problem with another angle. You started with image processing, human vision system, perceptual display, JND and you finish with computer vision, electronic, hdr and shader programming.

The evaluation of your work is different too. You don't validate your solution with the same criteria if your are in research or in production. It seems obvious but your algorithm - if it has something to do with human vision - has quality cost (you want your image to be better or the original quality preserved such that perceptually the difference isn't noticeable) and processing cost (if applying your new algorithm improves the visual quality but can only be ran at 10 fps it's also a quality issue).

Luckily you are not supposed to do everything, you and your colleagues have different skills, but you both should have crossover knowledge. Your supervisor should be able to fill the gap at the beginning or it's like having two groups speaking a different language trying to solve the same problem hoping that magically they will understand each other. Understanding a minimum of how your office neighbor is working is more than relevant. It's like your are on a fast car trying to catch a train and are looking for the jump that will help your to land on this moving train (this a beautiful picture of research and production).

## Kafkaesque bonus track, OLED vs LCD

OLED is trying to take over the world dominated by LCD technology. The big name are slowly switching to this technology. You can be almost sure that the middle names will follow until a new display technology arrives on the market. Take that planned obsolescence.

What is confusing for consumers and researchers/engineers like me is the fact that two distinct TV displays can reach the same quality standard. Standard defined by experts, people from the industry. Standard saying these TVs have the same quality, also they produce different visual experience...

It's safe to say that if your setup is dark, no parasite lights around your TV, you may choose an OLED display to exploit the good *behavior* of OLED in dark level, a pixel to 0 don't produce light.

It's also safe to say that if your setup is quite bright, you will need a pretty bright display to compensate the ambient parasite light, therefore you may choose an LCD TV display. LCD are usually brighter than OLED, but it's important too to distinguish between OLED TV display and portable OLED display...

And we talk later about HDR which is pretty fun too. Especially when a device is said to be *HDR ready* and is actually not an HDR display but a device that can perform *video tone mapping* which is the action of mapping HDR content to a regular (or LDR) display. Here too there are plethora of HDR encoding :-)

[IRYStec-link]:https://www.irystec.com/
