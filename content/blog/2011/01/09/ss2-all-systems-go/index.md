---
title : "SS2 : All systems go"
description : ""
tags : []
date: '2011-01-09 21:06:41'
---

It's coming to the end of the first week of the newly restarted Sheep Snaggers 2, and so far things are going pretty well. 

Once I decided to ditch the old codebase and start from scratch, I managed to make some pretty decent progress on the new stuff.

Here's the first test of the sprite system:
<a href="http://i24.photobucket.com/albums/c12/b33rman/gamedev/SS2/screen104.jpg">
<img width="600" src="http://i24.photobucket.com/albums/c12/b33rman/gamedev/SS2/screen104.jpg" />
</a>

Which pretty quickly turned into this
<a href="http://i24.photobucket.com/albums/c12/b33rman/gamedev/SS2/screen095.jpg">
<img width="600" src="http://i24.photobucket.com/albums/c12/b33rman/gamedev/SS2/screen095.jpg" />
</a>
as I got the movement and radar code online.

After a brief graphical overhaul, and bringing the <a href="/2011/01/04/ss2-keeping-control">new input system</a> online it was starting to look a bit better.
{{< youtube L7AL4M6bnzg >}}

Only trouble was, with the new visual look that player sprite isn't very visible.
A brief attempt at drawing a new Starsheep sprite convinced me that a new approach was needed:

<a href="http://i24.photobucket.com/albums/c12/b33rman/gamedev/SS2/screen106.jpg">
<img width="600" src="http://i24.photobucket.com/albums/c12/b33rman/gamedev/SS2/screen106.jpg" />
</a>

So I whipped out my trusty copy of <a href="http://www.blender.org">blender</a> and spent several hours swearing at the screen until I managed to produce this rather nifty 3D chappie, along with a sweet Immelman turn to change direction.

<!--more-->

{{< youtube NBW_nvhp8AQ >}}

Unfortunately, the new look Starsheep was making my old alien sprites look a bit shoddy, so several more hours of swearing got me these guys:

<a href="http://i24.photobucket.com/albums/c12/b33rman/gamedev/SS2/screen103-1.jpg">
<img width="600" src="http://i24.photobucket.com/albums/c12/b33rman/gamedev/SS2/screen103-1.jpg" />
</a>
Much better.
Finally somewhat satisfied with how things were looking, I also managed to get the collision detection system working this evening, so now I've got all the important parts in place to hopefully start focusing on the gameplay side of things rather than mucking about in the guts of the engine.