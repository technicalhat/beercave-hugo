---
title : "Beerman's adventures in voxel-land, part 4 : Now featuring actual gameplay"
description : ""
tags: ["voxel engine"]
date : 2015-01-25 22:58:00
---


Ah, weekends. When I get to unwind from sitting at a desk writing code all week by... oh... right.

Anyway, I managed to make a fair bit of progress this weekend. It's looking a bit less like a tech demo and a bit more like a game

Previous Entries : [Intro](/blog/2015/01/14/beermans-adventures-voxel-land) [Part 1](/blog/2015/01/15/beermans-adventures-voxel-land-part-one-triangles-cubes-blocks-oh-my) [Part 2](/blog/2015/01/20/beermans-adventures-voxel-land-part-two-blowing-chunks) [Part 3](/blog/2015/01/22/beermans-adventures-voxel-land-part-three-it-moves)

<!--more-->
 
## Day 6

With the basic rendering in place, it's time to make a start on an actual videogame. Most of the major effort for day 6 was building a simple voxel "sprite" loader. Basically it takes a png file of slices through the model and used that to populate the block data.

I'll probably need to come up with a proper editing tool at some point, but for now it means that at least I can edit models with a standard paint package rather than tediously typing in big lists of numbers.

{{< figure src="shipmodel.png" caption="And there it is. one expertly drawn spaceship voxel sprite!" alt="A basic spaceship sprite">}}

Most of the rest of the time was spent tidying up the code a bit, moving things that I'd hacked together in place out to their own subsystems, renaming things to be more sensible, that sort of thing. I got a basic control system and player movement in place, called it a night, and settled down with a curry, a few beers and a spot of Saints Row 4.

## Day 7

Bugs, bugs, bugs! That was the theme for much of day 7. Nothing major, just fiddly little cosmetic things with the draw order being out of whack. On the plus side, it did inspire me to build in a handy debug overlay so I could keep track of what's going on without resorting to command line output. Which came in really handy when I then spent several hours trying to figure out why my newly added particle system wasn't rendering (short answer - because I wasn't telling it to. I spend a whole bunch of time and effort setting up a big list of particle cubes and then rendered precisely none of them. D'oh!)

{{< figure src="particles1.png" alt="Some particles">}}

Once I finally figured that out though, the rest came together pretty quickly.

{{< youtube vl9FUZyotmk >}}

With the particles working, I added in a basic enemy sprite (borrowed from [D.I.Y. SYNSO](http://bagfullofwrong.co.uk/bagfullofwords/abuse-my-ip-make-games/) ), added collisions, and got the little buggers to explode in a shower of particles.

{{< figure src="kaboom.png" alt="A particle explosion">}}

{{< youtube yYHJTvDPNOc >}}

<span style="text-align:center;width:600px; display:block"><b>This is really starting to look quite videogamey now</b></span>

