---
layout: post
title:  "Notes on NLP and color"
date:   2017-04-10 10:21:06 -0800
categories: blog post
---

This post is a never ending story and a follow up on a previous article on [graph and NoSql][link-post-graphs-en-stock].

### How to organize my research?
I started to work on a few projects the last two months, projects involving color science, color space, finding the right JNDs (or Just Noticeable Differences) for our algorithms, display modeling and more.

As usual with this type of R&D projects there is a bibliography stage in order to figure out what you understand about the topic and what have the people done about it. Pretty fast you are making cross references and identify which papers, authors, keywords are important to that topic. If you want to really understand and go further you need to read/re-do all of this work.

### Déjà view
One more time when I'm facing this working situation where I'm missing a tool to represent the interactions between those publications. If you write a research article you pretty much have the connections between the works of others in your head, basically who is referring to whom, you tell your story while adding references in your writing instead of drawing a genealogy research tree. Having in my hand a tool to kind of visualize those connections will be nice as a support, something between illustration and text.

### The database
A research article has always its sources listed with it, each source having as well links to other articles. The question I'm often facing is how do I build my DB - which I already have, e.g. **bib** file containing a list of references with *year*, *authors*, *reference title* and more - in order to request information I can't directly see but only briefly grasp?

### The requests and the wishes
Regarding the requests I know what are the question I would like to have the answer from my DB:
+ what is the degree of relationship between author A and author B.

In term of Natural Language Processing (NLP) I would be also really interesting to compare words used by different group of researchers. Ideally I could like to create:
+ graphs of connections between researchers based on their publications
+ graphs of keywords to visualize how fields and sub-fields are represented.

[link-post-graphs-en-stock]: http://mrbonsoir.github.io/blog/post/2014/05/28/Graph-en-stock.html
