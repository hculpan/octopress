---
layout: post
title: "Blog setup"
date: 2014-05-30 21:23:31 -0400
comments: true
categories: 
- blog
- web development
---
So I hope I now have my blog completely setup and secure at it's new home at http://www.piduino.info.  As you may have noticed, I'm using Octopress to manage this blog.  [Octopress](http://octopress.org/) is a static site generator based on Jekyll and written in Ruby (a language I know next to nothing about).  For those who don't know, a static site generator works by taking my blog posts that are written as normal text files ([Markdown](http://daringfireball.net/projects/markdown/) files to bemore precise) and converts them to html and constructs the full blog as a set of static files.  A normal blog site managed by, say, Wordpress would be dynamic.  That is, when you access the site, it pulls data in from data sources (most likely a database) and builds the web page for you at that moment.  But a static site generator builds all the pages ahead of time.  This is good for that don't change frequently (like this one), and it also means that I don't really need to have much to host the website.  I just need a server (which I've acquired through [DigitalOcean](https://www.digitalocean.com/)) and a basic web server, which is [Nginx](http://wiki.nginx.org/Main) in my case.

Following this [example](http://fideloper.com/node-github-autodeploy), I put my blog source code into a [GitHub project](https://github.com/hculpan/octopress).  I then setup a Node.js server using the script from the afore-mentioned blog post, and wrote a quick shell script to pull any new changes from git and rebuild my blog site automatically.  So now all I have to do is write my post, commit it and push it to my GitHub repo for the blog, and everything else will be handled automatically for me.  Kinda neat!