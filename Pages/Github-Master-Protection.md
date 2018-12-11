---
title: Setting up GitHub branch protection
author: LazerFX
date: 2018-12-11
name: Github-Master-Protection
series: Setting Up the Website
---

# Setting up GitHub branch protection

So while working on setting this site up, I needed to ensure that I couldn't check into the master branch directly.  I'm trying to set things up with a proper flow - so CI/CD, an 'agile' design process, tests, and tasks/issues in GitHub's projects.  When I configured the `master` branch to be protected, however, I ran into an issue: I couldn't approve my own pull requests.

## A peculiar request?

The issue I was working on is the first on in my project - [Issue 1](https://github.com/LazerFX/website-engine/issues/1).  After trying a few things, I couldn't figure it out, and I didn't particular think that this was an odd query, so after searching, I posted on [Stack Overflow](https://stackoverflow.com/questions/53629263/single-user-github-repository-how-to-protect-master-but-allow-my-own-prs) with the hope of someone else having been in this situation before.

## An accidental solution

While I waited for a response, I continued to set up the pipeline and process.  I plumbed in Azure Pipelines (What was previously known as Visual Studio Team Services), and set up a blank CI pipeline (It runs a basic bash script currently).  Once I set that up - suddenly, I couldn't push into `master`.  I'd set the pipeline up so that it needed the 'test' to give back a successful result (Which it will do every time at present), and then it stopped all check-ins to the `master` branch.

## It's OK, I fixed it!

In the spirit of passing this forwards, I put an answer onto the StackOverflow question I had created saying how I managed to fix it, and with the details.  I'm still not completely satisfied, as the separate project to contain the pages will not have a CI pipeline (Although, I may create a dummy one just to give this protection).  Either way, problem solved, on to the next ones...