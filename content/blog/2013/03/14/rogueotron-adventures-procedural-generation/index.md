---
title : "Rogueotron - Adventures in Procedural Generation"
description : ""
tags : ["1gam", "march", "rogueotron"]
date : 2013-03-14 20:46:35
---

I'm a couple of days into development on Rogueotron now and the basics are starting to come together a bit.  Thanks to the horrors of Regular Paid Employment I've only been able to put a couple of hours a night into it during the week but I've managed to get the basic movement/firing and transitions between rooms working with some stylishly blocky placeholder graphics.



<a target="_new" href="https://s3.amazonaws.com/beercave.co.uk/gameamonth2013/month3/pics/rogueotron1.png"><img width="280" src="https://s3.amazonaws.com/beercave.co.uk/gameamonth2013/month3/pics/rogueotron1.png"/></a>
<a target="_new" href="https://s3.amazonaws.com/beercave.co.uk/gameamonth2013/month3/pics/rogueotron2.png"><img width="280" src="https://s3.amazonaws.com/beercave.co.uk/gameamonth2013/month3/pics/rogueotron2.png"/></a>
<strong style="width:600px; display:inline-block; text-align:center">Not about to win any awards for visuals any time soon, I admit...</strong>


<!--more-->

The next job on the list if I want to have any business describing this as any kind of roguelike is procedurally generated maps. Since this is based on Robotron, I'm planning on generating the map as a series of rooms rather than the more continous dungeon layout of most roguelikes. Something along the lines of Smash TV seems appropriate.


To make the maps a bit more interesting than just pure randomness, I'm borrowing the  <a href="http://www.squidi.net/three/entry.php?id=4">Environment Tree</a> mechanic from  <a href="http://www.squidi.net/three/index.php">Three Hundred Mechanics</a>, which is an all-round excellent resource for all things procgen related.
 

I've already played with the idea back when I was working on Gun Bastard so I know it's pretty easy to tweak the tree-generation described in the article to generate the kind of map I want. I've currently got a nice little Python implementation up and running that looks a bit like this:



<p style="width:600px; margin-left:auto; margin-right:auto;">
<a target="_new" href="https://s3.amazonaws.com/beercave.co.uk/gameamonth2013/month3/pics/procgen1.png"><img width="190" src="https://s3.amazonaws.com/beercave.co.uk/gameamonth2013/month3/pics/procgen1.png"/></a>

<a target="_new" href="https://s3.amazonaws.com/beercave.co.uk/gameamonth2013/month3/pics/procgen2.png"><img width="190" src="https://s3.amazonaws.com/beercave.co.uk/gameamonth2013/month3/pics/procgen2.png"/></a>
<a target="_new" href="https://s3.amazonaws.com/beercave.co.uk/gameamonth2013/month3/pics/procgen3.png"><img width="190" src="https://s3.amazonaws.com/beercave.co.uk/gameamonth2013/month3/pics/procgen3.png"/></a>




It's a little rough on item placement right now, and could do with some tweaking to filter out "boring" maps but it should make for a decent base to build on once I get it ported over to Java.
