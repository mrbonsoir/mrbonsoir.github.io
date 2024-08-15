---
layout: post
title:  "datavizRun"
date:   2024-08-06 09:09:09 -0500
categories: blog post
---


# Dataviz of gps run traces

A few days ago I started a small project about data visualisation. The data being gps traces of a [run club][runrite-link] I joined in 2021.

Here is the new repository called [datavizRun][datavizRun-link].

The motivations are:
+ to improve my data science skills
+ to make sens of data 
+ to produce nice visuals
+ to answer questions about those data
+ to have fun playing with data

# Status of the project afer one week

I think I passed the stages of:
+ gathering data
+ formating/cleaning data
+ reaching the 20% Pandas level
+ interacting with the formated data and getting answers
+ producing basic visualizations
+ identify flaws in my data, _eg when the conversion of .gpx files to my data structure revealed some information are missing_

## DataBase

I did choose to represent my data as:
+ a list of DataFrame
+ single DataFrame highlighting information about the list

## Pipeline

I have for now three [notebooks][datarunVizNotebook-link]:
+ one for importing the raw data, eg the .gpx files and save them as .csv files
+ one for datavisualization and making request about the database such as _what is the longest run?, what is the average run distance?_ ... and this is pretty easy as since I have information in a Pandas DataFrame I can easily extract many insigths
+ one for a second cleaning pass

# What's next?

For sure to generate more visuals, add more raw files meaning re-running my notebooks in the right order to update the database. The list of to-do is infinite:
+ improve my code = _get faster answer about the database_
+ create more visuals
+ add dynamic to the visuals _as for now everything is static_ and ideally put everything into a [TouchDesigner][TouchDesigner-link]. project

[datavizRun-link]:https://github.com/mrbonsoir/datavizRun
[datarunVizNotebook-link]:https://github.com/mrbonsoir/datavizRun/tree/main/notebook
[TouchDesigner-link]:https://derivative.ca/
[runrite-link]:https://www.instagram.com/runritemtl
