---
layout: '../../layouts/Post.astro'
title: Migrating Wordpress users to .Net
description: Fun and games figuring out what hashing algorithm has been used so I can migrate users with their credentials intact
date: '2012-08-20'
---

Having a little bit of fun today trying to figure out which algorithm has been used on a Wordpress site I'm in the process of rewriting (in ASP.Net MVC).

The original site is creaking at the seams, so I'm writing a new bespoke system to handle the workload. But one of the tasks I need to do is migrate all the existing users across. Fortunately, the version of Wordpress uses some sort of nice one-way encryption for all user passwords. That's nice for security, but makes my job just that little bit more difficult.

Now looking at the data from the original database, I can see an account that I know the password of, and I can see a 34 character value starting with $P$B...  which all of the passwords begin with.

A quick google shows that wordpress uses a framework called <a href="http://www.openwall.com/phpass/" rel="nofollow">phpass</a>. Another little google finds a <a href="https://www.phpbb.com/community/viewtopic.php?f=71&amp;t=1771165" rel="nofollow">port of phpass written in c#</a> by <a href="http://www.digilitepc.net/" rel="nofollow">Ryan Irecki</a> (a fellow Kiwi?).

I was hoping the passwords would all be BCrypted, but a little bit of experimentation showed that they are indeed just MD5-based salted and variable iteration hashes. The only modification Ryan's code needed was to switch out the $H$ header for $P$ and voila! Portable password checking on .Net.

Now at least, users will be able to log into the new site with their migrated records. After a successful login, because I'll have access to a valid password for the user temporarily, I'll be able to create a new hash using either BCrypt or PBKDF2, which will be a lot more secure.
