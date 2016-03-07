---
layout: post
title:  "Graphs en stock"
date:   2014-05-28 17:46:06 +0100
categories: blog post
---

Several meetings on Meetup and now one day of workshop on graph database organized by people behind [Neo4j][link-neo4js]. Answers bring new questions, what can I do with this approach? Using cypher you can ask your database in an almost *natural language way* and find information in your database. A nice feature presented here [GraphGists][link-graphgist] allows you to run live query on the web and render graphs, several examples are presented.

Now for me the question is what do I do with that? Looking at my thesis references I could explore where I found relevant information (even so I kind of know the main source of information) or in which direction I could go. It is very close to study a social network, you are looking at the connections between authors and topic of research.

Regarding this blog, each post is a node and the nodes are sharing common features (keywords and dates) that can be used to navigate through the "database of stories". Here I would have to build my database (and being able to update it as the blog is evolving at each new entree) and to manage to create a nice visualization (a graph) that could be displayed for each post (to show how it it related to the others) or to give the possibility to look for all posts sharing similar keywords (and create new path into the database).

Regarding color science and metamerism, it could be interesting to illustrate this matter for a database of spectrum (knowing that different surfaces with specific spectral properties can be perceived identical under a common illuminant).

To me it is a lost about visualization and d3js is knocking on the door.

[link-neo4js]: http://neo4j.com/
[link-graphgist]: http://neo4j.com/graphgists/