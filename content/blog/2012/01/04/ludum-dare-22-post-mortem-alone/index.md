---
title : "Ludum Dare 22 post mortem : Alone"
description : ""
tags : ["ludumm dare"]
date : 2012-01-04 22:32:05
---

In my <a href="/2012/01/01/post-mortem-2011">last update</a>, I mentioned that I should probably get around to writing up how I got on with <a href="http://www.ludumdare.com/compo/ludum-dare-22">Ludum Dare 22</a>. After <em>just about</em> completing something that could be called a game for LD21 back in August (<a href="/category/tags/ludum-dare-21">full story here</a>), I thought it'd be fun to have another go now that I've been playing with Unity for a while.

If you just want to play the game, go <a href="/content/lonely-robots-kitten-quest">here</a>, otherwise read on...

<!--more-->

I was planning to blog the development as I went along, like last time, but I just ended up sticking updates on twitter instead as it was less hassle. Will have to see if I can get around to installing a decent drupal plugin for uploading images and stuff before the next one.

So anyway - Ludum Dare 22. The theme this time was <em>Alone</em>. Yeah, I wasn't too keen on that one. One of those "it's not good unless it's depressing" "art game" kind of themes. Making stuff go kaboom is more my style. Still, after wasting <em>way</em> too much time whining about how it was rubbish I was eventually reminded up Spectrum/C64 classic <a href="http://en.wikipedia.org/wiki/Ant_Attack">Ant Attack</a>, which felt like something I could more-or-less hammer into shape to fit the theme.

One of my least favourite things about <a href="/content/get-choppah">GET TO THE CHOPPAH!!!</a> was the map. I basically just chucked a bunch of "buildings" on a poorly drawn terrain and called it a day, and it was far too easy to win just by walking around the edges of the map. To avoid that, and add a bit of variety, I decided to dabble with some simple procedural generation, and by the Saturday evening I had a fairly acceptable Antescher-esque city generator, complete with a hastily modelled robot character to float around it (bit sneaky there. I used a robot so I could plausibly have him float around with, I dunno, anti-gravity or something, and not need a walk animation)

<p style="width:600px; margin-left:auto; margin-right:auto">
<a href="http://s24.photobucket.com/albums/c12/b33rman/beercave/?action=view&amp;current=Generator2.jpg" target="_blank"><img src="http://i24.photobucket.com/albums/c12/b33rman/beercave/Generator2.jpg" border="0" alt="Photobucket" width="600"></a>
<strong style="width:600px; display:inline-block; text-align:center">Randomly generated robot city.</strong>


Unfortunately, development was somewhat interrupted at that point when I was dragged roughly to the pub by miscreants and quite literally forced to drink pint after pint of <a href="http://www.wychwood.co.uk/">fine ruby ale.</a> Understandably, this meant nothing more was getting done on Saturday night, and also put paid to most of Sunday morning...

Still, I had the bare bones of a game in place, and drawing from the unofficial LD22 theme of <a href="http://www.ludumdare.com/compo/2011/12/16/kitten-challenge/">kittens!</a> I had a plot! You, the robot, had to rescue your pet kitten who was lost in the city of evil robots and <em>all alone!</em> (See, there's your theme right there!) I quickly hacked up a couple of enemy robot models and a kitten (with *two* whole models for sitting and standing - amazing levels of content this game has!), added some fairly basic patrol/chase AI and some poorly drawn intro/ending screens and I had a game ready for submission <em>in advance of the deadline</em>

<p style="width:600px; margin-left:auto; margin-right:auto">
<a href="http://s24.photobucket.com/albums/c12/b33rman/beercave/?action=view&amp;current=Game.png" target="_blank"><img src="http://i24.photobucket.com/albums/c12/b33rman/beercave/Game.png" border="0" alt="Photobucket"></a>
<strong style="width:600px; display:inline-block; text-align:center">Defeated by enemy droids, Lonely Robot lies down for a nap</strong>



So, what'd I learn this time around then?

<strong>Good stuff</strong>
<ul>
<li>I definitely know what I'm doing a bit more with Unity now. Managed to get things up and running fairly easily with a lot less time frenziedly checking forums and documentation.</li>
<li>Similarly, giving myself a quick refresher course in using blender and reaper before the compo started was definitely a good idea. I'm not exactly the world's greatest artist or musician but I can at least knock out "programmer art" without spending too much time on it now.</li>
<li>The movement for the kitten worked out pretty well. It was basically a hack to get around my nonexistent animating skills, but having the little guy bounce along makes it quite fun.</li>
</ul>
<strong>Less good stuff</strong>
<ul>
<li>Note to self : don't go out on the piss halfway through a Ludum Dare. Nuff said.</li>
<li>The AI for the enemy robots isn't all that great. Bit of a tendency to get stuck on the buildings. Could have been fixed with a bit more time for testing.</li>
<li>As a couple of reviewers pointed out, the sparse colour scheme made it a little difficult to judge where things were in relation to each other at times. Maybe a grid pattern on the floor or something would help.</li>
<li>No HUD. I'd meant to have a health meter and maybe some sort of radar to point you towards the kitten, but kept putting it off to do later and then suddenly it was submission time and "oh fuck, I forgot about the HUD". Still works as a game without it but would have been nice to get that in there.</li>
</ul>

<strong>Future plans</strong>
<ul>
<li>Procedural content is definitely the way to go. I managed to get a reasonable level generator hacked together from scratch pretty quickly, with a bit more time to spend on more varied buildings and better placement rules it could be quite good. Been reading some very interesting stuff about <a href="http://www.valvesoftware.com/publications/2009/ai_systems_of_l4d_mike_booth.pdf">Left 4 Dead's AI Director</a>. Think there might be more than a few ideas in there I could borrow for future projects.</li>
<li>AI is still a bit of a weak spot. At least my enemies weren't total zombies this time, but they were still a bit dim. Random walk, pace between two points and chase was pretty much the limit of the AI routines, and even then they were a bit buggy. I'd really like to get some smarter enemies in the next game.</li>
<li>I mentioned this last time, but I really do need to blog more. Apart from anything else, having a record of what I've done really helps keep track when I have one of those "what the hell was I thinking when I wrote this?" moments. Might write up how I did the city generator, that could be good.</li>
</ul>