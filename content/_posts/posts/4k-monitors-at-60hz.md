---
title: 4k monitors at 60Hz
description: The trick to getting your 4k monitor running at 60Hz. HDMI 2.0, DisplayPort and DualLink DVI.
date: '2017-06-08'
---

I'm enjoying 4k monitors. I still have several low-res ones (if you can call 2560x1440 low res), but I bought a couple of [Samsung U28D590 Monitors](http://www.absolutegeeks.com/samsung-u28d590-4k-uhd-monitor-review/) recently and had no trouble driving them at 4k 60Hz using DisplayPort. However it wasn't until I tried to replicate this setup at a client's site when I ran into problems.

The graphics card they'd ordered was definitely reasonable. GTX 1050 Ti with DVI, two HDMI outputs and one DisplayPort. Which is comparable to the GTX 660 Ti that I run at home (soon to be upgraded to a GTX 1070 - roughly 2-3x faster). So I was surprised when I couldn't drive either panel at 60Hz.

The two cables they had were DVI -> HDMI, and a standard HDMI cable. Initially, I thought it was the HDMI cable, possibly the cables were only HDMI 1.4, so limiting the throughput, restricting us to 30Hz? (I don't know if that's even a thing, but it seemed plausible)

Using a DisplayPort cable, it was trivial to get one of the panels to refresh at 60Hz, but the other refused to play ball. And since the 1050 Ti appeared to only have one DisplayPort output, we were limited to either DVI (which the Samsungs don't have) or HDMI.

It wasn't until I took a cable home and tried it on my monitors that I realised that there's nothing wrong with the HDMI cable at all. It's the monitors themselves that are limited to HDMI 1.4, so unless you drive them using DisplayPort, you're totally out of luck.

Now, I'm sure that's not the same for all situations. But it's definitely worth checking the specs of your 4k monitor to make sure that the interfaces you're using actually support 60Hz. Either via Dual-link DVI, or DisplayPort most likely. And if the options are limited, then make sure you've a graphics card with the ports needed and the cables to match.

**EDIT:** Okay, turns out, unless your monitor supports HDMI 2.0, you're pretty much limited to DisplayPort for 4k @ 60Hz. Which means you basically need a graphics card with two DisplayPort outputs. Dual Link DVI only supports 2560x1440 @ 60Hz, any higher resolutions are 30Hz. And with a bit of searching, I can't find any adapter that converts HDMI 2.0 to DisplayPort 1.2. It might be possible, but they're not cheap/readily available. Definitely easier to choose the correct graphics card in the first place. 

<div style="text-align: center;">
<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" viewBox="-30 -210 2570 2248" style="width: 200px; height: 200px;">
  <g transform="matrix(1 0 0 -1 0 1638)">
   <path fill="currentColor"
d="M1210 72q10 -1 19.5 2.5t17 9.5t12 14.5t4.5 18.5q0 49 -45 52q-55 4 -100 21t-81 39.5t-63 47.5t-45 46.5t-27.5 36.5t-10.5 16q-15 26 -43 26q-21 0 -34 -15.5t-13 -35.5q0 -14 5 -23q1 -3 12.5 -21.5t33.5 -45t55.5 -57.5t78.5 -59t100.5 -48t123.5 -25zM1817 485
q25 0 46 9.5t36 26t23.5 39t8.5 48.5q0 64 -47 117q-23 25 -48.5 38.5t-55.5 13.5q-26 0 -47 -10.5t-35 -27.5t-21.5 -40t-7.5 -48q0 -66 45 -117q45 -49 103 -49zM543 782q0 -20 13.5 -33.5t33.5 -13.5h18q59 0 119 -11.5t115.5 -29t103.5 -38t84 -38.5t57.5 -30t23.5 -13
q13 -8 26 -8q20 0 34 14.5t14 34.5l-1 11q-4 30 -23 64.5t-50 72.5q-31 39 -72 78t-92 80q-51 40 -93.5 69.5t-77.5 49.5q-15 6 -25 6q-20 0 -34.5 -12.5t-14.5 -36.5q0 -28 25 -42q75 -44 144 -98t132 -117q-224 93 -397 93q-63 0 -63 -52zM2382 269q0 -40 -2 -73.5
t-5 -61.5l-9 -10q-36 -50 -193 -93q-78 -22 -174 -39.5t-211 -30.5q-114 -13 -224 -18.5t-218 -5.5q-114 0 -243.5 6t-277.5 20q-146 13 -262 36t-203 52.5t-146 64t-89 70.5q-3 9 -5 31.5t-2 58.5q0 61 8 117t24 110t40.5 108t57.5 112q67 118 153.5 200.5t189.5 149.5
l-199 308q-14 20 -14 45q0 16 6 31t17 26t26 18t33 7q44 0 68 -37l210 -322q122 48 242 72.5t239 24.5q94 0 177.5 -8.5t161 -26t152 -45t149.5 -64.5l181 330q24 42 71 42q36 0 58.5 -25t22.5 -57q0 -24 -10 -41l-184 -336q77 -61 133 -118t94 -111q37 -53 66 -109.5
t49.5 -120t31 -134.5t10.5 -153z" />
  </g>

</svg>
</div>
