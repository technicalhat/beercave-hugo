---
title : "DETHTANK day 2"
description : ""
tags : []
date: '2010-09-27 21:30:00'
---

Between work, the Dexter season 5 premiere and being struck down with a near terminal case of <a href="http://manflu.org.uk/">man flu</a>, I didn't get a whole lot done today.

I have, however, started work on what I'm calling the Beer Engine. A simple (for now) version of a <a href="http://cowboyprogramming.com/2007/01/05/evolve-your-heirachy/">component engine</a>, which will hopefully prevent me from coding myself into a corner as the game code develops.

The basic concept is that the game engine will consist of several subsystems - graphics, scene management, movement, AI etc. All the game components can have multiple behaviours attached which will register them with the relavant subsystem.

So, for example, a particle object would have the Drawable and Moveable behaviours attached on object creation, which would then register the object with the graphics and movement Managers. The Main game loop would then call the Movement and Graphics Managers in turn which would move and draw the particle as determined by its behaviours.

The design isn't 100% nailed down yet, so I'm almost certainly missing something vital, but hopefully the general structure should help keep my code manageable enough to get the game out by the end of October - ideally I'm aiming to have something playable up and running by the weekend.

<!--more-->