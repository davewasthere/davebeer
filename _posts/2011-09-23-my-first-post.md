---
layout: post
title: Hosting your blog with GitHub pages
description: Having found wordpress both great, but also a little slow/annoying/clumsy to extend, I decided to go back to static pages with a twist. You know it makes sense...
---

Okay, [GitHub Pages](http://pages.github.com/) is pretty amazing. [Jekyll](https://github.com/mojombo/jekyll/wiki) just makes it even more magic, as it will apply templates to your posts giving you plenty of control over formatting, but allowing you to easily change your site.

The beauty of hosting a blog this way, is the pages are completely static. So delivery time is always going to be incredibly quick. Running Wordpress using a shared server instance, I was getting around 1000msec to deliver an incredibly light homepage. On GitHub, that's normally down around the 150-180msec range. Pretty much an order of magnitude faster.

And these days, speed counts. Especially if your blog gets slashdotted/reddited/digged (well, maybe not digg any more) or HackerNews'd. The static site has a good chance of surviving that load. Admittedly, a well cached Wordpress site should do as well, but I've lost count of the number of unavailable Wordpress blogs when the going gets tough.

And that's not to say your site has to be completely static either. You've always got things like Disqus/Facebook or GetSatisfaction to dynamically include commenting on your site without adding extra load to your server.

That said, I've not found it completely straight-forward. I wanted to be able to edit my site from any browser, so needed some sort of front-end to GitHub. In the end I found [Cloud9](http://c9.io) which looked the business. GitHub does offer a code editor now, but you can't create files, which is a bit of a pain.

So the process was; Create a github account then create a repository for your blog. Create a Cloud9 account. Sign into c9 using your github account. Clone your repository. Start editing.
That was all fairly easy. But I'm either struggling with Git (having come from an SVN background) or there's something a little odd with Cloud9. I'm editing from a few different machines and I thought all of the repository is hosted with Cloud9. But weirdly, when I've switched machines, I've ended up having much older versions of files when I open them.

Maybe it's all a lot simpler when I'm a little more solid on Git commands. For now I'm just hacking away with Add, Commit, Diff and Push. Mostly I want to get to a point that I'm happy with what Jekyll has to offer and figure out the rest of the toolchain as I go.
