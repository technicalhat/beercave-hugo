---
title : "Oh behave!"
description : ""
tags : []
date: '2009-01-29 00:00:00'
---

I spent the last couple of days reading over the <a href=@http://code.google.com/p/owyl/@>Owyl</a> docs, and I've managed to implement some basic AI in Gun Bastard.

I've got two different follow behaviours for the bad guys, a "shoot object x if you can see it", and I've farmed the player controls out to joystick move and fire behaviours rather than them being in the game loop.

<!--more-->

My player control code now looks like:

{{< highlight python >}}
repeatAlways(
parallel(
limit(behaviour.joystickFire(ship, list=World.mybullets, stick = stick), limit_period=.1)
,
repeatAlways(behaviour.joystickSteer(ship, stick = stick))
,policy=PARALLEL_SUCCESS.REQUIRE_ALL
)
)
{{< /highlight >}}

I'm writing all my behaviours to work against my standard sprite objects, so I should be able to reuse the routines as I add new enemy types by just adding existing behaviours to them- *way* less ugly than some of the Sheep Snaggers code. :D

<a href="http://s24.photobucket.com/albums/c12/b33rman/gamedev/gun%20bastard/?action=view&amp;current=screen015.jpg" target="_blank"><img src="http://i24.photobucket.com/albums/c12/b33rman/gamedev/gun%20bastard/th_screen015.jpg" border="0" alt="Photobucket" /></a><br />
Screenshot : Me being pursued by a few of my newly intelligent bad guys.
