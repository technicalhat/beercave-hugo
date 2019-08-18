---
title : "Pygame input wrapper"
description : ""
tags : []
date: '2011-06-05 13:58:07'
---

As originally discussed in [Keeping Control](/2011/01/04/ss2-keeping-control), I built a fairly handy wrapper class for handling player input in [Sheep Snaggers 2](/content/sheep-snaggers-2). Now that the game is finished, I'm happy enough with the wrapper code to release it into the wild in the hope that someone else might find it useful.

Basically it abstracts out the various keyboard/mouse/controller functions by mapping them to a set of named controls. Each control can map to more than one input format so the core game logic doesn't have to know what controller you're using, it just asks the input module if e.g. a 'FIRE' event happened this frame.

You can find the source code along with a simple example [here](/content/inputpy), or in the sidebar under 'Other Stuff'. The code is released under the [Beerware license](/content/beerware), so if you like it, why not buy me a pint?

<!--more-->