---
title : "Beerman's adventures in voxel-land, part 6 : The best laid plans"
description : ""
date : 2015-03-25 20:45:00
---

Previous Entries : [Intro](/blog/2015/01/14/beermans-adventures-voxel-land) 
[Part 1](/blog/2015/01/15/beermans-adventures-voxel-land-part-one-triangles-cubes-blocks-oh-my) 
[Part 2](/blog/2015/01/20/beermans-adventures-voxel-land-part-two-blowing-chunks) 
[Part 3](/blog/2015/01/22/beermans-adventures-voxel-land-part-three-it-moves)
[Part 4](/blog/2015/01/25/beermans-adventures-voxel-land-part-four-now-featuring-actual-gameplay)
[Part 5](/blog/2015/03/25/beermans-adventures-voxel-land-part-five-the-hard-parts)

As mentioned in the last installment, I've got about a week and a half left to finish up the voxel game before ROM. Clearly then, this is the perfect time to start working on another game!

{{< figure src="./trenchrun.png" caption="A basic spaceship sprite" alt="A basic spaceship sprite"  >}}

<!--more-->

The homebrew tournament's been a feature for a couple of years now - basically it's a high score contest played on games coded by attendees and friends. This year though, the field was looking a bit on the thin side - a few of my regulars didn't have anything available for one reason or another, and it was down to just myself and Piku of [NCOT software](http://ncot.uk/).

Not wanting to leave it with just the two games in there, I had a think about what I could build on the voxel code that wouldn't take much development time, and settled on a sort of hybrid of Flappy Bird and the Star Wars trench run. Pilot your _[totallynotanxwinghonest]_ fighter down an endless, randomly generated trench, with points awarded for distance. 

So having got a fair bit done on the shooter on Saturday, I sat down around 6pm Sunday evening to have a play. By 11 it was looking something like this:

{{< youtube VpFNBiGS-5c >}}

Not much of a game there yet, but it does fly really nicely.

Monday night was mostly spent tweaking performance and tidying up a few rendering issues, then Tuesday's job was making a start on the collision detection. 

{{< youtube F3wYhdVxWMg >}}

So far, it just flags a collision if your ship's centre point is inside of a non-empty chunk - if I don't want the game to be either stupidly easy or horrifically unfair I probably need to make that a bit more accurate, which means I need to check if any of the ship's blocks intersect with any blocks in the surrounding chunks. This may involve maths!

