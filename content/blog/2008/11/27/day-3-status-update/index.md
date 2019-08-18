---
title : "Day 3 status update"
description : ""
tags: []
date: '2008-11-27 00:00:00'
---

<i>Originally posted at <a href="http://postcardstohell.livejournal.com/69660.html">http://postcardstohell.livejournal.com/69660.html</a></i>

Had to go into town and see about changing banks today, so I didn't get as much done.

Wasn't entirely happy with the state-based sheep AI, so I switched it out for a simple flocking system. Avoidance behaviour is working pretty well - I can herd individual sheepies around with my ship pretty well - but they don't really flock yet.

I need to adjust how the enemy ships work too - they're *way* too efficient early on, then they get rubbish at hunting once the sheep are more spread out. I'm using a half-assed drunkard's walk algorithm at the minute(follow random vector for random time), switching to single-minded pursuit once a sheep comes into range. This kind of sucks on two levels - the random walk never really travels much of the world, and the chase mode is way to accurate to give the sheep a chance to escape.

Hopefully I can get the wrinkles ironed out of the behaviours sometime tomorrow so I can get on to adding the shooty parts.

<!--more-->
