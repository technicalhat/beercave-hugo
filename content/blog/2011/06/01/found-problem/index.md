---
title : "Found the problem"
description : ""
tags : []
date: '2011-06-01 20:40:12'
---

I finally got around to sitting down and taking a look at the performance problems with Sheep Snaggers 2 tonight. A 5 minute run with profiling switched on pointed me right to the middle of my font handling routine where I found this:

<img src="http://i24.photobucket.com/albums/c12/b33rman/gamedev/SS2/oops.png"/>

So while I was probably right about how inefficient I'm being with my texture usage, it looks like the bigger problem is that I was <i>looking in the wrong bloody cache</i>, with the end result that every time I was rendering a character I was generating a brand new texture - oops!

To make things worse, since the score counter was using that font routine, it was rendering at least half a dozen new character textures <i>every single frame</i> - hardly surprising that I was chewing up VRAM at a rate of knots.

I still need to find out how it runs on one of the RV homebrew laptops, but based on the profiler results for the fixed version I reckon it should be ok, in which case I can delay optimising things for a future project and get back to the important business of making it possible to shoot Mecha Markie up the arse!

<!--more-->