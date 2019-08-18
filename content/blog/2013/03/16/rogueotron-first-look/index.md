---
title : "Rogueotron - first look"
description : ""
tags : ["1gam", "rogueotron"]
date : 2013-03-16 22:47:09
---

I've been a busy little Beerman today. The map generator is now ported across to Java and fully plugged into the game, which means I've got an actual consistent world to wander around rather than just spawning a random room every time you go through a door.

With that in place, I've got a very basic enemy generator (it only spawns grunts right now) in place and a Director class that locks you in the rooms until they're cleared, which is pretty much just about enough to call it a game - not a very *fun* game just yet, but there's still two weeks to go.

Here's how it looks right now...

<!--more-->
{{< youtube Unh4UzigCVA >}}

I also spent a bit of time mocking up how I want the UI to look. I was originally planning on having the UI elements along the top of the screen, similar to how <a href="http://store.steampowered.com/app/113200/">Binding of Isaac</a> does it. Trouble is, with a widescreen layout the play area is already too short vertically, so once you add the header it ends up looking less like a room than a corridor.

Instead, I've moved all that information into a sidebar on the right of the screen, which also has the beneficial effect of making the play area a bit more square.

<p style="width:600px; margin-left:auto; margin-right:auto">
<img width="600" src="https://s3.amazonaws.com/beercave.co.uk/gameamonth2013/month3/pics/layout.png"/>
It also leaves me with a whacking great chunk of dead space in the bottom right, but after consulting with the thoroughly helpful folks on the <a href="https://plus.google.com/u/0/communities/117275686212402755276">One Game a Month Google+ Community</a> I've got plenty of ideas on how to fill it. For now though, it's time for my regular Saturday night skeleton-twatting.

