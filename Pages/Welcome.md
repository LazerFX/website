---
title: Welcome to The Lazy Developer's Blog
author: LazerFX
date: 2018-12-04
name: Welcome
---

# Welcome to the Lazy Developer's Blog!

Thanks for stopping by.  This blog has been created by me, Peter Street, also known as LazerFX, to document my personal adventures in development.  Hopefully, as time goes by, I'll demonstrate how you can set up a website in .NET Core with a full CI/CD pipeline for very list cost.  I also plan to have pages covering .NET technologies, with associated sample code and demonstration pages within the website.

I intend to use modern technology to develop the site.  If it gets large enough, a microservices-based architechture will be used, but initially, a simple dockerised .NET Core infrastructure will handle the site.  Two github repositories will be created.  The first will be the site engine.  This will be developed separately from the content, allowing for live-update without having to push full containers to the endpoint.  The second repository will contain the site content.  The DevOps pipeline will inject credentials into the engine container to connect to the content repository and perform a git pull (possibly I'll set up a webhook so it auto-pushes - need to look into how this will happen without having to constantly spam `git pull` equivalents...)

The pages will be written in Markdown, with `yaml` tags to denote page titles, series links, etc.  There will be a little non-standard extension to the Markdown to allow for images to be handled nicely (This may continue to be extended, as time goes on).