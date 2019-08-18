---
title : "Checking in"
description : ""
tags : ["1gam", "beercave racer", "blender"]
date : 2013-05-14 20:43:57
---

Well, this game's certainly turning out to be a learning experience. And the main lesson is "don't pick your projects just because you think it'd be cool to play with the tech." The main factor in deciding to try this one was that I thought the retro-3D rendering looked fun and like something I could reasonably implement in a weekend. What I didn't take into account is that once that was done I'd be in need of a big old stack of graphical content to make it interesting. 


It didn't take me long to figure out that there wasn't a hope in hell of me generating the vehicle sprites by hand unless I was planning on releasing "poorly drawn blob racer 2013". Letting computers do the hard parts is pretty much my job description though, so I figured I could offload all that tricky perspective business to software by using renders of a bunch of 3D models as sprites.  With that in mind I popped on my trusty learnin'-hat, fired up <a href="http://www.blender.org">Blender</a> and prepared to dive into the exciting world of <a href="http://theorangeduck.com/page/subdivision-modelling">subdivision modelling</a>.


<div style="width:300px; margin-left:auto; margin-right:auto;">
<img style="display:inline-block; width:300px;" src="https://s3.amazonaws.com/beercave.co.uk/blogpics/hat_300.jpg"/>
<strong style="width:300px; display:inline-block; text-align:center">My trusty learnin' hat.</strong>
</div>

<!--more-->

A spot of googling pointed me in the direction of this <a href="http://www.the-blueprints.com/">excellent resource</a> of reference drawing for hundreds of existing cars (among other things - I can see it being really handy if I do go ahead with the Afterburner clone I was thinking of for a spiritual sequel to this game). Combined with a handy <a href="http://en.wikibooks.org/wiki/Wings_3D/Tutorials/Box_modeling_a_car_with_all_Quad_topography">tutorial based on the wrong software</a> I was in business.


First up, a car for the player. The model for this one is my trusty "Beermobile".

<div style="width:600px; margin-left:auto; margin-right:auto;">
<img style="display:inline-block; width:600px;" src="https://s3.amazonaws.com/beercave.co.uk/blogpics/cougar_threesides_600.jpg"/>
<strong style="width:600px; display:inline-block; text-align:center">Atomic batteries to power, turbines to speed...</strong>
</div>

A few hours of mucking about in Blender and I had this. Still needs a little tidying up but it'll do for now.

<div style="width:600px; margin-left:auto; margin-right:auto;">
<img style="display:inline-block; width:600px;" src="https://s3.amazonaws.com/beercave.co.uk/gameamonth2013/month5/pics/cougar_anim_600.gif"/>
</div>

After that, I started to get the hang of things. I can knock out a fairly reasonable new model in an hour or so, and from there have a set of sprites for use in game in about another 10 minutes. Vehicle-wise, I'm mostly aiming for a mix of sporty little soft tops and big meaty muscle-cars, like these two.


<div style="width:600px; margin-left:auto; margin-right:auto;">
<img style="display:inline-block; width:600px;" src="https://s3.amazonaws.com/beercave.co.uk/gameamonth2013/month5/pics/challenger_anim_600.gif"/>
</div><div style="width:600px; margin-left:auto; margin-right:auto;">
<img style="display:inline-block; width:600px;" src="https://s3.amazonaws.com/beercave.co.uk/gameamonth2013/month5/pics/roadster_anim_600.gif"/>
</div>

I also whipped up some new scenery graphics - since these are just billboards I didn't bother going the full 3D model route, just hacked them together with GIMP.


So, with all that new stuff added in, things currently look like this. There are a few rendering glitches still, mainly because the steering is a bit on/off at the moment and the rotation angles I rendered the cars at don't match the corners very well. Also, I need to write something a bit more sophisticated for scenery generation than just spitting out a random sprite. All that said though, it's starting to look like an actual game :)


<p style="width:600px; margin-left:auto; margin-right:auto">
<iframe width="600" height="400" src="http://www.youtube.com/embed/3dztO6OcdG8" frameborder="0" allowfullscreen></iframe>
<strong style="width:600px; display:inline-block; text-align:center">This might actually turn out to be fun...</strong>

