---
layout: post
title: "Rebuilding blog website with Jekyll"
date: '2024-09-10 15:33:16 -0400'
author: mrbonsoir
categories: post data github 
---

In the past weeks I have been working on a few things:
+ my blog a [color scientist on the internet][mygithublog-link]
+ cleaning my github repositories
+ data analysis of a run club path
+ writing new blog post about running and maps

# Blogging with jekyll

I use the ability of github to [host blog][githubjekyll-link] using [jekyll][jekyll-link] framework build in [ruby][ruby-link].

I went a bit deeper to really understand how the static website was generated in order to try locally before to publish online.

# Working with gpx traces

For that I have created a new repository called [datavizRun][datavizRun-link] with tools to load gpx files and produce visualizations of those files.

It is based on Python programming language.

The biggest improvement was the usage of [Folium][folium-link] to produce beautiful embedded in blog post maps.

There is a big room of improvement for how I handle my gpx data and I'm continuously learning how to use better [Pandas][pandas-link] data structure.

# Cleaning my github repository

I did put some repositories in archive or delete them, looking at pseudo code more than 8y old is embarrassing. 

# The power of Liquid templates

At first I thought I will create another blog website, still using github hability to host static website.

But while learning more about [jekyll][jekyll-link], how to change theme and how it is working I realise I can simply add my new posts as usual, a list of the post is available when you reach my blog, and I can add page that will - each time the website is created - list all posts about running.

It always fun to learn new tools, for now I'm just scratching the surface of [liquid][liquid-link] an open source template language created by [shopify][shopify-link] early 2000.


[pandas-link]:https://pandas.pydata.org/

[mygithublog-link]:https://mrbonsoir.github.io/

[datavizRun-link]:https://github.com/mrbonsoir/datavizRun

[folium-link]:[https://python-visualization.github.io/folium/latest/]

[jekyll-link]:https://jekyllrb.com/

[liquid-link]:https://shopify.github.io/liquid/

[ruby-link]:https://rubygems.org/

[shopify-link]:https://www.shopify.com/

[githubjekyll-link]:https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll