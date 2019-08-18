---
title : "SS2 : Picking up where I left off"
description : ""
tags : []
date: '2011-01-03 17:18:45'
---

Hmm, seems I've been here <a href="http://www.beercave.co.uk/2009/09/08/buggeration">before</a>.

I'm taking a look around at Sheep Snaggers 2 before I get back on with it, and while it's not actually <em>crap</em>, there's an awful lot of "ooh, I wouldn't do it like <em>that</em>" in there.

Worst offender has got to be the way I'm running 3 separate rendering loops to cope with the world wraparound effect, then running them <em>again</em> to render the radar. That's basically down to broken thinking - I got stuck on the idea of the gameworld as fixed, which leads to having to pile up a variety of hacks in order to deal with the world wrapping around at the ends.

Since everything in the game is getting updated every frame anyway, it'd be a wee bit more efficient to just have the ship/camera x position fixed at zero and move everything else around it. That way my render loop is just "draw everything within the screen boundaries" and the radar loop is just "draw everything"

While I'm doing that, it's probably not a bad idea to resurrect some of the component architecture stuff I was playing with for <a href="/category/tags/dethtank">DethTank</a>, which should help tidy up the hierarchy a bit.

Gamewise, there's one or two things that need throwing out. I'm planning to lose the title screen and just run the main game scene continuously as an attract mode with some title text as a HUD overlay when not in play. I can just swap out the player controller for a simple AI routine easily enough.

The fireball/ramming power up needs to go too. It's a fun mechanic, and one I plan on exploring in a later project, but it just doesn't fit in well with the Sheep Snaggers theme. The whole point of the game is about rescuing sheep from aliens before they can build their death star so I need to stick closer to the original Defender template.

<!--more-->

Another thing that's going away is the level structure. Instead I'm going to go with perpetually spawning sheep and a never ending supply of aliens and just keep cranking up the difficulty over time. Hopefully all this will help add a bit more focus into the project and save me from getting stalled...