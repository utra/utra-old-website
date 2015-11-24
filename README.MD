# UTRA Website

This is the website for UTRA (University of Toronto Robotics Association). The site is a static site made using [Jekyll](https://jekyllrb.com).

## Making changes

A nice thing about Jekyll is that all of the content on the pages is written in markdown, a very simple to write language that gets transformed into HTML. If you aren't familiar with writing Markdown, this [cheat sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) can help.

To make your changes:

1. Fork this repository
2. Make your changes locally, either creating new Markdown files for events (in /pages/events), or modifying existing team pages (in /teams). If you want to preview your changes, [install jekyll](http://jekyllrb.com/docs/installation/), run 'jekyll serve' in the command line from the root of this folder, and navigate your browser to localhost:4000.
3. Commit and push your changes to your local branch.
4. Submit a pull request to here. The webmaster can accept your changes and they'll go live.

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
