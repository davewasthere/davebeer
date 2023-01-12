---
layout: '../../layouts/Post.astro'
title: Ubuntu to the rescue
description: Repurposing my old laptop, one with a busted screen.
date: '2012-09-24'
---

Earlier this year I managed to break the screen on my trusty laptop that I've had for the last four years. Bit gutting really, as I still loved using it and still haven't seen anything released since that I like any better. (Although the Asus Zenbook is getting close)

I've also noticed my power usage increasing quite a bit since I've started working on a new project. I'm leaving my development server on 24/7 which is really sucking through the juice. It's noticeable at least.

So to hit two birds with one stone, I decide to set up my old laptop as a low-power server. The tricky bit is installing an operating system on it. Neither the VGA, nor the HDMI, output any sort of display until the OS is loaded. Which makes installing a new one a little difficult as I think the BIOS isn't set up correctly to boot off USB.

So by removing the SSD HDD, transplanting it into another machine and installing a fresh copy of Windows 7 I thought I could then swap it back and windows would figure out what it needs to do to output to VGA at least. But it looks like Windows doesn't particularly like being transplanted like that. Testing it in a laptop with a working screen, I just get BSOD during bootup. I'm guessing Windows 7 is a little more fragile than XP used to be when you try and do this.

So in the end, it was Ubuntu I turned to. Installed Ubuntu while the harddrive was in another machine, then put it back in the original laptop and sure enough after boot I get a nice HDMI output. And I've got to say.. all the other problems I had getting various bits and piece to work last time, for some reason were a doddle this time round.

But unfortunately, I needed a Windows OS for my server, so ended up going for VMware Player. I actually wanted VMware Server, as I wanted headless operation, but that seems to be unsupported now. You'd have to use vSphere Hypervisor, but I'd be back with the same issue of how do I install it without a screen as I doubt that'd transplant particularly well.

In hindsight, I should have used VirtualBox, but I really can't be arsed reinstalling Windows now that I've activated one of my precious licences. But the added benefit of having Ubuntu as the host OS means I can do a hell of a lot more with the box. Overall a win and a great use of some old equipment.
