---
layout: post
title:  "CIC26 and HDR movie workshop"
date:   2018-11-12 15:15:15 -0500
categories: blog post
author: Jeremie Gerhardt
---

# [Color Imaging Conference][ColorImagingConference-link] (CIC) goes to Vancouver
*Another year, another Color Imaging Conference, another location, for the 26th edition it's Vancouver (Canada, BC).*

## Enter the arena
One thing for me about this conference, that I'm attending for a couple of years, is to always stay humble as there is often the temptation to think changes are slow to come. Humble because I should remember how little I was, little I knew back in time. I don't know much more than a few years back but I feel more confident regarding what I understand or don't understand. And if you have color science questions, then CIC is the place to be.

### Courses, article and workshop
I had the chance to attend two short courses of the Short Course program, one course on variational Color difference (*Variational Color Image Enhancement inspired by Human Vision* by [Edoardo Provenzi][edoardoprovenzi-linkedin]) with mathematical expressions included obviously, a second one High Dynamic Range display (*The Art of Making Better Pixels: High Dynamic Range (HDR) Display Concepts and Technologies* by [Timo Kunkel][timokunkel-linkedin] from [Dolby][dolby-link]).

I presented an article we submitted my colleagues at [IRYStec][irystec-link] and I a few months back, an article entitled *OLED display power model and its application to lossless perceptual algorithm*. The basic idea behind is to say it's important to be able to evaluate the display power consumption cost of an image on OLED display. In this era of tailoring the display to the user it's not enough to rely on image quality metric or image quality assessment to evaluate the quality of your new algorithm. Integrating a power consumption cost is another quality factor to take into account. I was surprised and happy to find some echo of this problematic during the conference, especially in regards to HDR display on screen or [projector][MTTBarco-link]. I love conferences for that, it can show you pretty fast if you are ok or completely wrong.

I also organised a workshop on HDR and Movie Production, the conference committee asked me if I could find people that were willing to talk about this topic and I jumped into that mission almost immediately.

### The conference
It’s basically like going back to school where you have to attend hours of short lectures on various topics. Sometimes it’s hard to stay focus, but here and there you grasp some interesting ideas, formulations and of course the authors of the articles you are reading are there too!

These days I’m into perceptual display but I always keep an eye or ear on article about printing. I did my PhD in multi-spectral color reproduction, graduate in 2007, and it’s nice to see things you thought were impossible or complicated back in time that are now in use for real. Especially I think of multi-inks printing system making use of Neugebauer primaries as usable and controllable colors *Halftone structure optimization using convex programming* from [Peter Morovic][petermorovic-linkedin], [Jan Morovic][janmorovic-linkedin] and All at [HP][hp-link],  pretty cool.

Below a non exhaustive of articles for this year that I found interesting: JPI-First Multi-scale Daltonization in the Gradient  Domain, Perceptually Based Restoration of backlit Images, A Study of Visible Chromatic Contrast Threshold based on Different Color Directions and Spatial frequencies, An Alternative Multi-scale Framework for Variational Perceptually-inspired Contrast Enhancement of Color Images, A Colour Appearance Model based on Jab Colour Space, Efficient Multispectral Facial Capture with Monochrome Cameras, Evaluation of HDR TVs Using Actual HDR content, Reviving Traditional Image Quality Metrics Using CNNs, Optimal Text-Background Lightness Combination for Enhancing  Visual Comfort when Using a Tablet under Different Surrounds, The Preferred Type of Tone-Curve in a Transparent OLED  Display, Assessing Color Discernibility in HDR Imaging using Adaptation Hulls, Single Anchor Sorting of Visual Appearance as an Oriented Graph and check the [CIC website][ColorImagingConference-link] for further information.

### Keynotes
The evening and keynote talks given by the four speakers were particularly interesting and captivating. Keynote and evening talks are the opportunity for the speakers to tell each a story, reveal how discoveries are made, how research works sum up over time (**A Brief Story of Superpixels** by [Radhakrishna Achanta][radhakrishnaachanta-linkedin], how very similar problems are tackled by neighbour communities (**Colour and Consumer Cameras: The Good, the Bad, the Ugly** by Michael Brown), how a research project becomes a product (**High dynamic range on the big screen** by [Anders Ballestad][andersballestad-linkedin]) or how people use color science in their profession (**Color in Narrative** by [Andrea  Chlebak][andreachleback-linkedin]).

## Workshop HDR and movie
### Context
This year I got the opportunity to organize a workshop for the CIC workshop session. Topic was very interesting to me, HDR and movie production. HDR is the new thing coming to the mainstream world of color. There is not one single definition, depending of what you do with it you will use different approaches, different words that can sometimes lead to confusion for both professionals and newbies.

The movie production is particularly interesting because it brings different people together, all the way from science, engineering to art. In the last 25 years the digital wave has redefined the way we make and consume movies: multiple digital cameras, VFX, color grading, possibility to almost instantly visualise the final look of the movie after shooting a scene, different specialities, very different way to work with light, different softwares, different architectures, different representations of color, different color spaces, different displays for the consumers and now HDR.

A recurring question when a new movie project is initiated is which workflow to choose? Before it was easy as all was physically printed on film, now the field of possibilities is infinite. A response to this possible recipe for disaster was [ACES][aces-link], [OpenColorIO][OpenColorIO-link] which are different and similar in the same time but help to be consistent with your workflow or color pipeline.

HDR has obviously not made the production easier. As for the digital wave, not all the technologies involved in the production of movies have evolved or reached a stable state synchronously. For example HDR displays exist but the differences between professional and consumer equipments are still huge both in prices and technical specifications.

That’s the starting point from this workshop. Bringing people behind the professions involved the production of moving images, let them talk about their work, their challenge, their experience in relation to HDR.

### Looking for speakers
I happen to know a bit about this field, the world of people crafting movie. Therefore I immediately did send a bunch of emails to my related contacts and people I didn’t know, spread my request to my color connections. I rapidly got replies, mostly positives or when the person couldn’t join but was intrigued I was left with a new name to reach out.

The exact day preceding the workshop we manage to meet all of us. I knew half of the speakers thanks to previous CIC and being in Vancouver [last August][SIGGRAPHpost-link] for [SigGraph][SIGGRAPH-link], but for the other half it was the first time we met irl. What was suppose to be a short meeting to prepare the speakers order and verify that we don’t repeat ourselves lasted more almost two hours of engaging discussion. I could not hope for better.

### During the workshop
The story we did want to tell is how science, engineering, art and content creation are connected along the journey to produce a movie. The panel we had was covering some of the key professions involved in that journey.

Below a short resume of each speaker presentation.

#### Image Display by [Timo Kunkel][timokunkel-linkedin] (Dolby, San Francisco, Ca)
Timo introduced to us the science behind HDR display. I will say his part was maybe the most known to the workshop audience as many color scientists were in the room.

But being a scientist in a company and therefore being involved into the making of products that will be used by not color scientists requires some additional skills, in other words to be able to explain to very different people what you are doing and what are your constraints.

I was a very good introduction for the workshop, good for audience who was with us right from the beginning and not left behind. I can only recommend Timo’s short course on the topic that he regularly gives at CIC.

#### HDR Post-Production by [Chris Davies][chrisdavies-linkedin]  ([MTT/Barco][MTTBarco-link], Vancouver, BC)
Chris gave us a glimpse of the setup diversity you will encounter when you are setting a movie production workflow. You need to be pretty aware of who is doing what, how people like to work. A big challenge in HDR movie (or series) production is to have the possibility to see all along the production journey how the HDR will look.

It may some sound crazy, but the HDR version could be appearing only at the end of production when the final master is released (it’s not completely crazy actually because before, physical printed movie time, there were always a delay between shooting and developing and being able to see the originals images, you had rushes - now dailies - but you were not waiting a scene to be developed to go on with the next scenes to shoot, but you were relying on the DP’s work and the lab’s trust to go on). It means that while on set the director of photography (DP) may not have an HDR display with him, most likely only the colorist or color grader will be able to grade the HDR and/or LDR version at the post-production facility. But here again professional HDR display are rare and expensive so you may have to use a consumer HDR display.

That’s not all, HDR display have different sizes and available dynamic, and what a colorist need for working is maybe different than what a producer want to judge the production state. It’s not a static world.

#### VFX by [Mario Rokicki][mariorokicki-linkedin] ([DNEG][DNEG-link], Vancouver, BC)
Mario was kind enough to replace his colleague Sean Cooper that had too much work at DNEG London to join us.

I learn a lot from Mario’s presentation (from the others as well) and here a list of key points I keep in mind regarding VFX and HDR: VFX people are working in HDR for a fair amount of time already, because VFX has to recreate everything virtually they had to deal with “how to do we encode sunlight and artificial light that have very different dynamic in the same scene?” So before HDR display they had to work with HDR content, without going too much into details you can check links below to dig more into that matter or science, but for me the fact that they are used to work in controlled light environment, pretty dark, that the image they looking at is the not final rendering is fascinating. The final look will appear when all the different contents are mixed and graded.

#### Color Grading by [Dermot Shane][dermotshane-linkedin] (independent colorist in Vancouver, BC)
We started with science and engineering and we are slowly moving toward the art of color manipulation.

In his talk introduction Dermot quoted Picasso “transform the sun into a yellow spot”. That aspect of his work was well described as well as the language. The colorist/color grader is another key role in the production workflow, he or she has is the last link between the movie director and the final look of the project, he/she needs to translate the DP visions into the available technology. Vocabulary is important and Dermot illustrated his presentation with a series of short video sequences where he explained what was tried to be achieved in those short videos. Understanding how a movie scene is constructed in term of lighting is obviously important. In his last example Dermot did show us a scene and the corresponding making off, a very dark scene from Harry Potter - dark in the sense of low light - that actually required a lot of light on stage. It can be counterintuitive but it tells us a lot of on how movie maker are capturing and manipulating light in its whole dynamic.

#### Movie grammar for HDR  by [Shane Mario Ruggieri][marioeuggieri-linkedin] ([Dolby][DOLBY-link] in  Sunnyvale, CA)
We have come full circle with Shane Mario concluding each speaker talk. Shane Mario is a colleague of Timo's that started the workshop. He has many roles and experiences from Sr. Production Engineer, Producer and Colorist part of Dolby Laboratories' Advanced Technology Group since 2010. One of his tasks is to go beyond creating HDR test charts and help develop storytelling in HDR.

The new HDR language and grammar is an important new realm. These new terms will change how people make movies, how they tell stories with light, shadow and images. It’s a valuable and rare skill to be able to talk to scientists and artists and this is the world Shane bridges daily. During his talk Shane presented his new Temporally based HDR light response technique called “The Thomas” as used in his short movie One Way Ticket. Here he linked audience adaptation, physical reactions and emotional responses to the story by using temporally based lighting scheme (the Thomas). It was interesting how we react to change of illumination, basically story telling with HDR directly crafting the audience reactions not only on an emotional level but a physical one too. One interesting point he made was  “One thing you want for sure is to avoid bright images for HDRness sake… it’s like repeatedly poking people with the 3D effect to their frustration…to be interesting, HDR has to embrace temporal and psychophysiological aspects only available in HDR.”


### Panel discussion
Good thing is HDR has evolved a lot in the past years but there are still a lot to do.

There is a need for better transforms based in science for previewing how HDR look.

There is a need for bigger, brighter HDR display, but switching too rapidly is dangerous too, for e.g. in VFX the artists work with LDR display and are used to be in muted environment.

And again language, all the people involved in the production of a movie are dealing with the same material, light, but each of them has a different vocabulary, goal, mission to handle it. This aspect of movie production hasn’t changed and still movie are produced.

Finally a great pleasure for me to have been able to bring all these talented people in the same room. So a big thank-you to the speakers for sharing their experiences.

## Links to continue on this topic
A few links if you want to know more on the movie production workflow:
+ [postperspective][ColorGradingHDRArticle-link] website
+ [A colorist interview][interviewmaxinegervais-link] on *the new world* of HDR
+ [OpenColorIO][opencolorio-link]
+ [ACES][aces-link]


[ACES-link]:https://www.oscars.org/science-technology/sci-tech-projects/aces
[DOLBY-link]:https://www.dolby.com/us/en/brands/dolby-vision.html
[ColorGradingHDRArticle-link]:https://postperspective.com/colorist-weighs-new-world-hdr/
[ColorImagingConference-link]:http://www.imaging.org/site/IST/IST/Conferences/CIC/CIC_Home.aspx
[DNEG-link]:https://www.dneg.com/
[interviewmaxinegervais-link]:https://postperspective.com/colorist-weighs-new-world-hdr/
[IRYStec-link]:http://www.irystec.com/
[OpenColorIO-link]:http://opencolorio.org/
[OpenEXR-link]:http://www.openexr.com/
[MTTBarco-link]:http://www.mtt-innovation.com/
[SIGGRAPH-link]:https://www.siggraph.org/
[SIGGRAPHpost-link]:http://mrbonsoir.github.io/blog/post/2018/08/17/SIGGRAPH2018.html

[andreachleback-linkedin]:https://www.linkedin.com/in/andersballestad
[andersballestad-linkedin]:https://www.linkedin.com/in/andersballestad
[timokunkel-linkedin]:https://www.linkedin.com/in/timo-kunkel-bb021917
[marioeuggieri-linkedin]:https://www.linkedin.com/in/shanemarioruggieri
[dermotshane-linkedin]:https://www.linkedin.com/in/dermot-shane-855a39163
[mariorokicki-linkedin]:https://www.linkedin.com/in/mario-rokicki-68769938
[chrisdavies-linkedin]:https://www.linkedin.com/in/chrisdavies123
[radhakrishnaachanta-linkedin]:https://www.linkedin.com/in/radhakrishna-achanta-916532
[edoardoprovenzi-linkedin]:https://www.linkedin.com/in/edoardo-provenzi-95b8bb21
[petermorovic-linkedin]:https://www.linkedin.com/in/petermorovic
[janmorovic-linkedin]:https://www.linkedin.com/in/janmorovic/
[hp-link]:hp.com/go/gsb/
