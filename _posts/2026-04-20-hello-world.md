---
layout: post
title: "Hello World"
date: 2026-04-19 09:00:00 +0000
categories: [general]
tags: [welcome, intro]
excerpt: "Welcome to the new blog and a quick introduction to what you'll find here."
---

Welcome to my new blog!

Installing this blog was quite easy. Especially since I didn't really do any of it myself.

I searched around a little bit looking for a simple self-hosted blog solution. I didn't really consider github pages because it's only for static html. When I first saw it mentioned that people were using it for blog posts, i assumed it used some client-side ajax calls to an API for storing blog posts or something. 

That's how server side brained I am. Maybe it's because simple blog sites are used so frequently in programming tutorials. But really, a static website is fine for this as it's just a collection of documents. Static just means it only updates as frequently as you update it.

Also, I was curious about using Jekyll. I've seen the mention of Jekyll themes every time I've set up a github pages site, and I've wondered what it is for a while. Turns out it's exactly what I was looking for - a simple way to create website using markdown. Once you set up the site template, you just plug in markdown files and Jekyll puts everything together for you.

At first I went into VS Code and, using the github copilot chat, I just told it to set up an empty Jekyll site. I didn't even have Jekyll installed locally, i just pushed it straight up to the repo, enabled pages and checked it out. The content was there, but the css wasn't.

Rather than trying to fix this, I had a better idea. Let's let github itself do this. It should know how to use its own product on its own platform. So, I deleted the files I had created and pushed the changes. Then, on the github website, i went into copilot chat and gave it the same instructions. 

It was quite interesting how this worked, it created a queue of 8 tasks to complete. Then it created an issue in the repo and wrote out those 8 tasks. As each task completed, it would update the issue. 

At the end, it created a pull request that I had to review and approve. To my great shame, this is not something I've ever done before. I've always worked in very small dev shops, and we used TFS mainly. Code reviews were very informal, usually just a quick glance through on our weekly sprint planning. Or maybe working duo with another dev. 

I wasn't really sure what I was doing, but I fumbled my way through approving the pull request, and the site was up!

I pulled the repo down to my machine and started writing some content. The next step was getting it running locally. It's pretty straightforward, however I needed to install Ruby before I could install bundle which is required. 

Editing the markdown feels very familiar. VS Code has this nice markdown preview pane too.

The problem is images... when the site gets pushed to github, the markdown looks for those images with a different local path than it does locally. That means you need to write this kind of syntax for images: 

     ![keyboard]({{ '/assets/comfortcurve3000.jpg' | relative_url }})

And then that doesn't render properly in the markdown preview pane.

So, I settled for embedding an html preview pane next to the markdown editing. I have to save the file and refresh the page to see the changes, but it works.

That's about it. I want to look more into vs code extensions for Jekyll or the themes they mention on github.