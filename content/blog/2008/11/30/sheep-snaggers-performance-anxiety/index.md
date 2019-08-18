---
title : "Sheep Snaggers : performance anxiety"
description : ""
tags: []
date: '2008-11-30 00:00:00'
---

<i>Originally posted at <a href="http://postcardstohell.livejournal.com/70031.html">http://postcardstohell.livejournal.com/70031.html</a></i>

I'm sick of referring to this project as "my RV game project", so I'm officially making Sheep Snaggers at least a working title. Cheers, Amy!

Got the AI to a point that I'm pretty much happy with now. The sheep flock relatively convincingly, and the aliens hunt them quite nicely. 

Unfortunately, the sheep AI is now crippling perfomance. The sweet spot for staying above 60fps looks to be around 20 sheep in my world, which kind of sucks.

<!--more-->

Possible options for improving performance:

1. Delve ninja-like into the guts of the ai code and figure out where the slow parts are.
2. Maybe break down my AI code so each item only updates once every x frames
3. Make off-screen sheep stupider. Anything that's not visible only has to work with an approximation of the real function - nobody will be able to tell.
4. The lazy man's way out - peg the fps to 30 and make everything move faster.

Think I'll play around with 2 and 3 for a while before I start trying anything complicated, like 1 would involve. Option 4 is the definite last resort. I should be able to hit 60fps for a simple game like this, dammit!

*EDIT*

That seems to work nicely. I turned the AI updates down to 1 frame in 60 and now I've got a nice healthy 70fps, which is pretty much what I get with AI switched off. Doesn't seem to have harmed the behaviour patterns either.

Might still update the AI to have a visible/invisible mode. I might still need the extra cycles when I add in bullets and collision detection.
