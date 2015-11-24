# UTRA Website

This is the website for UTRA (University of Toronto Robotics Association). The site is a static site made using [Jekyll](https://jekyllrb.com).

## Making changes

A nice thing about Jekyll is that all of the content on the pages is written in markdown, a very simple to write language that gets transformed into HTML. If you aren't familiar with writing Markdown, this [cheat sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) can help.

To make your changes, fork this repository, edit the files you want to change (the Markdown of the pages are located in /teams (team pages) and /pages/events (event pages), commit them to your forked branch, and submit a pull request. This can be accepted by the webmaster and the change will go live right away. For events, you simply need to create a new Markdown file and format the [front matter](http://jekyllrb.com/docs/frontmatter/) and title the same way as the files currently there. Jekyll will take care of adding them to the list of events, moving them from upcoming to past (assuming you have put the date/time in the front matter correctly), and clear them once the list becomes too full.

* * *

Here is a sample file:
````
---
layout: post
title: Sample Event Name
date: 2015-12-31
categories: events
---

This is a sample event file called {FILENAME}.md
````
