---
layout: default
title: 4k monitors at 60Hz
published: true
description: The trick to getting your 4k monitor running at 60Hz. HDMI 2.0, DisplayPort and DualLink DVI.
---

I'm enjoying 4k monitors. I still have several low-res ones (if you can call 2560x1440 low res), but I bought a couple of [Samsung U28D590 Monitors](http://www.absolutegeeks.com/samsung-u28d590-4k-uhd-monitor-review/) recently and had no trouble driving them at 4k 60Hz using DisplayPort. However it wasn't until I tried to replicate this setup at a client's site when I ran into problems.

The graphics card they'd ordered was definitely reasonable. GTX 1050 Ti with DVI, two HDMI outputs and one DisplayPort. Which is comparable to the GTX 660 Ti that I run at home (soon to be upgraded to a GTX 1070 - roughly 2-3x faster). So I was surprised when I couldn't drive either panel at 60Hz.

The two cables they had were DVI -> HDMI, and a standard HDMI cable. Initially, I thought it was the HDMI cable, possibly the cables were only HDMI 1.4, so limiting the throughput, restricting us to 30Hz? (I don't know if that's even a thing, but it seemed plausible)

Using a DisplayPort cable, it was trivial to get one of the panels to refresh at 60Hz, but the other refused to play ball. And since the 1050 Ti appeared to only have one DisplayPort output, we were limited to either DVI (which the Samsungs don't have) or HDMI.

It wasn't until I took a cable home and tried it on my monitors that I realised that there's nothing wrong with the HDMI cable at all. It's the monitors themselves that are limited to HDMI 1.4, so unless you drive them using DisplayPort, you're totally out of luck.

Now, I'm sure that's not the same for all situations. But it's definitely worth checking the specs of your 4k monitor to make sure that the interfaces you're using actually support 60Hz. Either via Dual-link DVI, or DisplayPort most likely. And if the options are limited, then make sure you've a graphics card with the ports needed and the cables to match.

