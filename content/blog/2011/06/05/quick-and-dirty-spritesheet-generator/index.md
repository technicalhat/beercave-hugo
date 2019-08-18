---
title : "Quick and dirty spritesheet generator"
description : ""
tags : []
date: '2011-06-05 19:15:25'
---

2 posts in a day - man, I'm on fire!

Before I get started on my next game project, I thought I should address my woeful lack of tool support, since it tends to lead to a certain amount of corner-cutting and inefficiency. First up, spritesheets!

[Sheep Snaggers 2](/content/sheep-snaggers-2)'s engine code had pretty decent support for rendering from single texture spritesheets, but since packing all my sprites together and working out the co-ordinates by hand was frankly a <em>massive pain in the arse</em> it only really got used for a couple of animations. I ended up actively resisting the idea of adding new animations because I couldn't be bothered with the donkey-work.

Since automating the donkey-work is pretty much what computers are <em>for</em> I thought I should address that by writing something to build the spritesheets for me - so this afternoon I finally pulled my finger out and the result was [Spritepacker.py](/content/spritepackerpy)

A brief google suggested that if I wanted it to be really efficient I'd be dealing with a variation on a classic <a href="http://en.wikipedia.org/wiki/Bin_packing_problem">NP Hard problem</a>, which is a bit more than I want to tackle on a lazy Sunday afternoon. A bit more googling found this example for <a href="http://www.blackpawn.com/texts/lightmaps/default.html">packing lightmaps</a> which looks like a nice simple interpretation of the First Fit Descending algorithm listed on Wikipedia. I tried it out with the Sheep Snaggers sprites and it seemed to do a pretty good job, anyway.
<a href="http://s24.photobucket.com/albums/c12/b33rman/gamedev/?action=view&amp;current=texture.png" target="_blank"><img src="http://i24.photobucket.com/albums/c12/b33rman/gamedev/texture.png" border="0" alt="SpritePacker output"></a>

<!--more-->