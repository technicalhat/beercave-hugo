---
title : "Ludum Dare 26 / 1GAM April : GunBoat"
description : ""
tags : ["1gam", "gunboat", "releases", "ludum dare"]
date : 2013-04-30 23:37:58
---

"Hey, weren't you making some kind of OutRun-inspired racing game?", you're no doubt wondering. Well yes, that was indeed the plan - but as (according to the internets) every famous military leader in history<a href="#footnote1">*</a> said, "No battle plan ever survived contact with the enemy."


So yeah, that game's not by any means dead yet, but with the end of the month approaching far too quickly it was becoming apparent that I wasn't going to get it anywhere near done in time., Too much time spent twatting around trying to get the rendering perfectm not enough spent making it actually playable.


Fortunately, last weekend was <a href="http://www.ludumdare.com/compo">Ludum Dare 26</a>, which gave me an excuse to temporarily shelve the racer and get down to some Jammin'. The theme this time around was "minimalism", and I conveniently had an idea lying around that I reckoned would more or less fit.


<a href="/games/gunboat"><b>Enough already - show me the damn game!!!</b></a>

<!--more-->

So where did this one come from? Well, weirdly enough I had a dream last week where I was playing a 3D boat-shooting game with nicely animated waves. Woke up around 4am and thought "thanks, subconscious - that's a great idea", and promptly emailed it to myself. This living in The Future thing comes in handy sometimes :) So early Saturday I got up, checked the theme and thought "yeah, I can use that".


Visually, I wanted something fairly retro, with a call-out to the old UKResistance <a href="http://www.ukresistance.co.uk/2005/11/blue-sky-in-games-campaign-launched.html">blue skies</a> aesthetic, because far too many LD entries seem to go down the "must make art. must be depressing" route. So job number one was making a nice sunny day...


<div style="width:600px; margin-left:auto; margin-right:auto;">
<a href="/games/gunboat"><img width="600" src="https://s3.amazonaws.com/beercave.co.uk/gameamonth2013/month4/pics/1.sky.png"/></a>
<strong style="width:600px; display:inline-block; text-align:center">Yeah, that'll do nicely :)
</strong>
</div>

Next job was getting the sea in place. Basically each layer is just a row of blocks in a sine wave, with the amplitude and frequency scaled relative to the z distance so that they don't all sync up.


<div style="width:600px; margin-left:auto; margin-right:auto;">
<a href="/games/gunboat"><img width="600" src="https://s3.amazonaws.com/beercave.co.uk/gameamonth2013/month4/pics/2.sea.png"/></a>
<strong style="width:600px; display:inline-block; text-align:center">Quite relaxing, isn't it?
</strong>
</div>

After that, I needed some happy little boats sailing on the peaceful seas.


<div style="width:600px; margin-left:auto; margin-right:auto;">
<a href="/games/gunboat"><img width="600" src="https://s3.amazonaws.com/beercave.co.uk/gameamonth2013/month4/pics/3.boats.png"/></a>
<strong style="width:600px; display:inline-block; text-align:center">One might even say "picturesque"
</strong>
</div>

<div style="width:600px; margin-left:auto; margin-right:auto;">
<a href="/games/gunboat"><img width="600" src="https://s3.amazonaws.com/beercave.co.uk/gameamonth2013/month4/pics/4.gun.png"/></a>
<strong style="width:600px; display:inline-block; text-align:center">Yeah, sod that. Eat laser, you bastards!
</strong>
</div>

And a sod-off big gun, because hey, videogames. Sod-off big guns kind of go with the territory.


So, if we're going to be shooting things they should probably explode. If only there was <a href="http://www.merseyremakes.co.uk/gibber/2010/08/the-videogame-explosion/">somewhere I could learn all about how to do explosions</a>] 


<div style="width:600px; margin-left:auto; margin-right:auto;">
<a href="/games/gunboat"><img width="600" src="https://s3.amazonaws.com/beercave.co.uk/gameamonth2013/month4/pics/5.crazysplode.png"/></a>
<strong style="width:600px; display:inline-block; text-align:center">OK, that might be a little *too* much explosion
</strong>
</div>


<div style="width:600px; margin-left:auto; margin-right:auto;">
<a href="/games/gunboat"><img width="600" src="https://s3.amazonaws.com/beercave.co.uk/gameamonth2013/month4/pics/sanesplode.png"/></a>
<strong style="width:600px; display:inline-block; text-align:center">That's a bit more like it
</strong>
</div>

So with that lot done, Saturday was drawing to a close and I was feeling pretty confident about getting something finished. Clearly there was nothing else for it but to catch an early showing of Evil Dead on Sunday. Wow - they did not fuck around with that one...


OK, back to it and it's Sunday evening, I've got most of a game, it just needs a little polish. Titles, level transitions, being able to lose. You know - the boring stuff ;) So I stuck on my hacking hat<a href="#footnote2">**</a> and just barely managed to bash something together before bedtime. There was just one thing missing...


<div style="width:600px; margin-left:auto; margin-right:auto;">
<a href="/games/gunboat"><img width="600" src="https://s3.amazonaws.com/beercave.co.uk/gameamonth2013/month4/pics/spudbonus.png"/></a>
<strong style="width:600px; display:inline-block; text-align:center">The People's Theme : "Potato"</strong>
</div>


You can <a href="/games/gunboat"><b>download GunBoat</b></a> from the <a href="/games">games page</a>


<a id="footnote1">*<a>Seriously - I've seen that quote attributed to everyone from Patton to Napoleon to Sun-Tzu to, I dunno, some fucking Klingon dude. It gets around.

<a id="footnote2">**</a>OK, not literally. I've got a Viking hat and a cowboy hat but no hacking hat. Maybe I should get one...
