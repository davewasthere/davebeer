---
layout: default
title: Private credentials on public github repository
published: true
description: I mess up and accidentally commit some SMTP credentials into a public repo. In under 24 hours, I learn my lesson.
---

I was pretty happy doing my first hackathon. I took part in Bendigo's first [Random Hacks of Kindness](http://www.rhokaustralia.org/) weekend hackathon for charity. My chosen charity was [Bendigo Foodshare](https://bendigofoodshare.org.au/). They currently distribute bulk food to agencies and run a very lean operation. However, there's an opportunity to redistribute prepared food (say from over-catered events for example), if it can be done without taking up a lot of Foodshare's time - as they've really got to focus on where they can have the most impact, with the larger food movements.

So our team came up with a pretty reasonable concept of a web-app that Suppliers can list Donations that they have available - and then an email goes out to around 40 vetted agencies, and the first agency that can pick up the Donation can claim it. After which, it's the agencies that distribute the food to the needy families, soup kitchens, etc...

![Our lovely web app](/img/foodshare.png)  
**Our lovely winning application**

The web-app was pretty straight-forward. It was when setting up the email notifications where I came a bit unstuck. Initially I tried signing up with Sendgrid. But they (rightly in hindsight) flagged my account as high-risk and wouldn't let me sign up. Although to be fair, they also tweeted afterward saying they want to get me sending emails, so think that they're pretty helpful really.

But I also had an existing account with another transactional email provider, so quickly set up and authenticated my test domain so we could get up and running. (This was Mistake No.1 - I should have sandboxed this domain, not fully verified it.)

The next day I had an email saying that my domain has been disabled due to bounces. Now, I knew that the students I was working with had used the odd invalid email address while testing. Perhaps 4 or 5 emails might have gone out to invalid accounts, so I thought the disable was a little on the harsh side.
But when I looked at the stats, in the one hour the baddies had access, there were nearly 3000 dropped emails - and slightly more successfully delivered ones.

The penny dropped.

I'd committed the SMTP host's username and password in with our public github repo for all to see. And it didn't take the baddies very long to both find it, and start abusing it. School-boy error Dave! I'm perhaps too used to working with private repos. :)

Anyway, it was quickly resolved and my transactional email provider was rather understanding under the circumstances.

And just a note if you've done something similar (and a quick search shows that there are plenty people who have committed secrets to public repos on github)... Remember that you have to burn those credentials. Once exposed you can't 'hide' them any more with another commit. Trash them completely!