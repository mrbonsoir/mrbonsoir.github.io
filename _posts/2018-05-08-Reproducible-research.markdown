---
layout: post
title:  "Reproducible research"
date:   2018-05-08 15:21:06 -0500
categories: blog post
author: Jeremie Gerhardt
---

To continue on sharing my longest work experience in a startup - [IRYStec][IRYStec-link] in Montreal - I will talk today about [reproducible research][wiki-reproducibility-link] and more how to concretely achieve it.

## The struggle continues

First of all I'm lucky enough to be able to continue research activities since I finish my Phd in 2007, I'm employed as senior color scientist after all, meaning not only I have research projects but I can also communicate some aspects of it. In other words I'm allowed submit parts of my work to conferences and therefore make some of our research available to the people.

## Making tools

Doing research you spent a lot of time developing tools, frameworks to ease the conduct of experiments and to facilitate the reproduction of those experiments. What you certainly don't want is that the same command to run a function or a script gives you each time different results.

Working in a startup where all the teams are in the same office gives you the chance to be closer to your colleagues and their specialities. My colleagues developers for whom the challenge - one of them - is to translate the work of the research team, advanced prototypes into a product. This means re-building something to make it stable and reproducible.

## The magic

Changing habits is difficult but learning new tools is fun too, hard at the beginning but so rewarding after you improved something. The motivation to try and/or learn something new can comes from different sources. Often it's driven by laziness, you know that this framework, this set of guidelines will make you gain time, so you learn it.

I'm using git for a while but until recently in a very simple fashion. Working in a team made me realised the power of git, the various configurations I met made me see that, working alone on a project versus working in collaboration to others.

## More hocus pocus and wizzardy

More magic happen when I went digging into [docker][wiki-docker]. I was looking for a better solution than [Python virtual environment][python-virtualenvs] which is already a huge step into improving your Python development skills, controlling on your working environment. I'm usually prototyping with the head in [Jupyter notebook][jupyter-notebook], once again working alone it's fine, but as soon as you want to share you work with someone else the trouble starts as we almost always don't have the same working environment (linux, mac, windows...). We may use the same Python version but not exactly with the same list of modules or external softwares installed on your machine. A long list of little differences that can compromise the reproducibility of your work.

After some googling, I came back to my colleagues and start to question them to help me to setup a reproducible working environment for Python and a jupyter notebook. I thought of jupyter notebook server, but being not completely convinced we looked into the docker direction. I'm still amazed with the results. We came a up a solution inspired from existing solutions that suits me: create a docker with Ubuntu, with the necessary Python modules, the possibility to run a Jupyter notebook server in the docker while accessing local notebooks and data. In other other words you control you data as usual, but the working environment is totally transportable, as today I can work at the office on my desktop computer running Ubuntu or being outside on my Mac and being sure I have the same working environment everywhere.

## Why is it cool for research?

It's a topic - reproducible research - more visible in research publications. Many of us are running experimentations on a computer, but each of us uses slightly different setups. It's extremely frustrating to read the work of another researcher that is public, article available, data available, code totally or partially available, you run some code and you don't obtain the same results when you are lucky to be able to run something.

I can only see benefit in sharing - when it's possible - also the tools used to obtain you results, not only the equations and results, the code and working environment too. In the same spirit I often enjoy visiting conferences which are covering slightly different domains to my own expertise. Sometimes the way a problem is solved will give you a hint on how to solve another problem. On those beautiful ideas I stop.

## Petit à petit l'oiseau fait son nid

Therefore I created this new repository I called [researchlab][researchlabdocker-link] (to be exact I modified an existing solution with the invaluable help and knowledge of my colleagues) where you can find information to build a docker image containing Python and jupyter notebook, together with bash script to use it. Continuing on that incredible achievement - for me - I re-modified this project to setup a digital atelier for my side projects. Very cool.


[IRYStec-link]:http://www.irystec.com/
[researchlabdocker-link]:https://github.com/mrbonsoir/researchlab/
[wiki-reproducibility-link]:https://en.wikipedia.org/wiki/Reproducibility
[wiki-docker]:https://en.wikipedia.org/wiki/Docker_(software)
[python-virtualenvs]:http://docs.python-guide.org/en/latest/dev/virtualenvs/
[jupyter-notebook]:http://jupyter.org/
