---
published: true
layout: default
title: Just a little more details would be nice
description: "If you're running windows with Ruby/Jekyll, you're a second class citizen"
---

I'm finding it a bit irritating getting a page build error in my blog. I suspected Prose.io initially just because there's some weird stuff happening with the cursor in the new editor, but github isn't really helping by giving the rather generic error 'page build failed'. That really doesn't tell me much.

Problem is, running windows, it's pretty difficult to get an installation of Ruby, the dev tools, the Jekyll gem and all that running properly. It's possible, I'm sure, but not really supported.

I actually have a lot of fun developing for windows. I like Visual Studio 2012 and MVC4. The toolset just keeps getting better and more pleasurable to work with. But there are times that I sorely consider switching to Ubuntu and developing solely in Linux. Probably single page web-apps with a ruby on rails backend... but it's seriously going to feel like starting from scratch.

In the end, it took about an hour to sort. Installed Ubuntu 13.04 desktop on a USB stick, add a few packages (ruby, rubydev and jekyll) install git, set up a new ssh key and clone my repository, then try and build it with Jekyll.

Turns out, an old post had an unescaped ampersand character within a a-tag's href field. In the past, that's never been an issue. But looks like there's been a minor breaking change. I modified the offending file and we're back up running again. Joy!