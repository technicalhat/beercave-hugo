---
title : "New game project"
description : ""
tags: []
date: '2008-11-25 00:00:00'
---

<i>Originally posted at <a href="http://postcardstohell.livejournal.com/69528.html">http://postcardstohell.livejournal.com/69528.html</a></i>

It's my week off, so I thought I'd get a bit of work done on a project I've been ignoring for a while. I've been widdling around in <a href="http://www.pygame.org/">pygame</a>/<a href="http://matthewmarshall.org/projects/rabbyt/">rabbyt</a> in the hopes of getting a little game hacked together in time for next year's <a href="http://www.retrovision.org.uk/rv2009/index.htm">Retrovision</a>.

Every year the welcome pack includes a disk with a few games on, and waaay back in June the <a href="http://www.yakyak.org/viewtopic.php?f=20&amp;t=72342">shout</a> went out for entries. Being my usual organised self, I played around with a few things for a week or so and never really got anything much done, but with the deadline for inclusion coming up fast I thought I'd better get my finger out.

<!--more-->

Originally, I was planning on doing a side scrolling shooter, but, y'know, it's been done. By people way better at it than me. So, after flailing around for half of Monday wondering what I should do, I decided to revisit the Sinistar clone I'd been playing with when I first got started with pygame.

The first thing I found was that I could avoid a *lot* of headaches by using rabbyt (which is openGL based) and moving the viewport around to track my ship, rather than having to translate the positions of all my objects. Plus, by offloading all the heavy lifting to the video card, rabbyt's sprite library has performance to burn, so I could initially be lazy just render my whole universe, whether it was visible or not.

That *did* leave me with the issue of how to make my universe wrap around at the edges, Asteroids style.  I solved it with a bit of creative thinking. Since this is a <a href="http://www.llamasoft.co.uk/frontpage.php">Llamasoft</a> themed game I decided to set it on a farm and replace the asteroids of the original with sheepies, with dastardly aliens abducting the sheepies to build their deathstar. That way, my play area is bordered with a fence and I don't have to bother wrapping it around at the edges. Cunning, no?

So, as of the end of day 2 I've got the following working:

* Fully scrollable play area.
* Ship with asteroids-style controls
* Wandering sheep with state-machine based AI. They wander around, graze, randomly panic, and occasionally poo :D
* Sheep run away from the ship
* Alien ships wander the play area, abduct sheepies, and take them back to build their deathstar. Right now they're maybe a *little* too efficient - in the last test run they managed to clear an 8000x8000 playfield of 100 sheep in about a minute...
* Alien deathstar builds itself up from abducted sheepies and then comes to life.

Still to do:

* Add weapons to ship so I can defend the sheepies.
* Tweak the alien AI a little. Those little guys are *way* too efficient
* Collect sheep-poo to use as bombs against the deathstar
* Scoring
* Head-up display with score, lives, etc.
* Sound &amp; music
* Menus, high score table, possibly attract mode
* Various fancy graphical effects
* This thing is in dire need of a cool name. Answers on a postcard(tohell). guys.

And just to raise the antici...

...pation levels a bit, here's a couple of screenies.

<a href="http://s24.photobucket.com/albums/c12/b33rman/gamedev/RV%202009/?action=view&amp;current=screen1.jpg" target="_blank"><img src="http://i24.photobucket.com/albums/c12/b33rman/gamedev/RV%202009/screen1.jpg" border="0" alt="Screenshot 1" /></a>

My plucky ship (which badly needs a new graphic more in keeping with the theme) faces off against the mighty deathstar. If it looks weird, it's because the shadows were being rendered on top of their sources when I took this. D'oh!

<a href="http://s24.photobucket.com/albums/c12/b33rman/gamedev/RV%202009/?action=view&amp;current=screen2.jpg" target="_blank"><img src="http://i24.photobucket.com/albums/c12/b33rman/gamedev/RV%202009/screen2.jpg" border="0" alt="Screenshot 2" /></a>

Here we see several dastardly aliens dragging poor, defenceless sheepies towards the deathstar with their tractor beams. Sadly, there's nothing I can do, because I haven't coded in weapons yet...
