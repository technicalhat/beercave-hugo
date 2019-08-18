---
title : "New game - GUN BASTARD"
description : ""
tags : []
date: '2009-01-26 00:00:00'
---

With Sheep Snaggers pretty much finished, I've been thinking about how I could have improved the structure of the code. As it stands, it's a pretty horrendous spaghetti mess - I hacked features on pretty much at random, and it shows.

I've come up with a much better design, where the main game loop nice and simple

{{< highlight python >}}
while running:
  think() #handles control input and AI
  update() # move things around
  render() # draws the end result

{{< /highlight >}}

and the different game modules each have their own versions of the 3 functions. When I switch game modes, I swap out the function pointers for the relevant module and everything stays inside the one loop, which makes handling game events much cleaner.

In Sheep Snaggers, the attract mode and high score entry each have their own seperate copy of the game loop, which then has to throw events back to the main loop - hideous I know, but that's what happens when you don't plan ahead...

Anyway, to test the new structure out, I needed a nice simple game concept.

Enter GUN BASTARD.

<!--more-->

Shamelessly stole^W^W<i>Inspired by</i> OddBob's excellent <a href="http://bagfullofwrong.co.uk/bagfullofwords/about/war-twat/">War Twat</a>, it's an arena shooter with mental visuals and ridiculous levels of firepower

<a href="http://s24.photobucket.com/albums/c12/b33rman/gamedev/gun%20bastard/?action=view&amp;current=screen001.jpg" target="_blank"><img src="http://i24.photobucket.com/albums/c12/b33rman/gamedev/gun%20bastard/th_screen001.jpg" border="0" alt="Title Screen with logo" /></a>

The *very* basic title screen, with hastily GIMPed logo.

<a href="http://s24.photobucket.com/albums/c12/b33rman/gamedev/gun%20bastard/?action=view&amp;current=screen008.jpg" target="_blank"><img src="http://i24.photobucket.com/albums/c12/b33rman/gamedev/gun%20bastard/th_screen008.jpg" border="0" alt="The gun bastard in action" /></a>

The Gun Bastard in action. I have *no* idea just how many bullets are on screen right there...

<a href="http://s24.photobucket.com/albums/c12/b33rman/gamedev/gun%20bastard/?action=view&amp;current=screen011.jpg" target="_blank"><img src="http://i24.photobucket.com/albums/c12/b33rman/gamedev/gun%20bastard/th_screen011.jpg" border="0" alt="More gun bastard pyrotechnics" /></a>

But it looks like a lot :D

Next job is to throw in some enemies and see how they like it up 'em!
