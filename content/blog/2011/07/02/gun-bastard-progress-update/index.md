---
title : "Gun Bastard progress update"
description : ""
tags : []
date: '2011-07-02 17:59:31'
---

In a staggering break with tradition, I've been using my weekend to actually get some work done! No, I don't really believe it either...

I started the day off by knocking up a particle system. After hooking it up make the enemies explode when shot it looked a little something like this:

<a href="http://s24.photobucket.com/albums/c12/b33rman/gamedev/gun%20bastard/?action=view&amp;current=screen021.jpg" target="_blank"><img src="http://i24.photobucket.com/albums/c12/b33rman/gamedev/gun%20bastard/screen021.jpg" border="0" alt="Basic particle explosions"></a>

As you might have noticed, it's a bit on the excessive side - I accidentally set the explosions to repeat every beat instead of only firing once. Looks like I'll be able to get plenty of stuff on screen at once though  :)

<!--more-->

Once I was satisfied I could chuck particles around without any problems, I thought I should see about making things a bit prettier. After fixing the particle size and colour to match the game sprites, I added a motion trail effect to my explosion particles and ended up with this:

<a href="http://s24.photobucket.com/albums/c12/b33rman/gamedev/gun%20bastard/?action=view&amp;current=screen032.jpg" target="_blank"><img src="http://i24.photobucket.com/albums/c12/b33rman/gamedev/gun%20bastard/screen032.jpg" border="0" alt="Pretty particle explosions"></a>

Not quite up to OddBob's standards yet, but a definite improvement.

With that done, I spent a bit of time refactoring things to keep the codebase nice and tidy. One thing that was a bit ugly about [Sheep Snaggers 2](/content/sheep-snaggers-2) was the huge chunks of boilerplate code I was using to spawn my game entities and attach the relevant behaviours to them. It works, but as the project gets bigger it's not really sustainable and I ended up with a whole bunch of near-identical 'Spawner' classes for the different entities.

So, to make my life easier in future, I've built myself a generic entity spawner system which takes a folder full of entity definitions (basically a list of behaviours to attach to the game object) and can then generate entities by name.
So instead of having

{{< highlight python>}}

enemy = GameObject(
  x = 0,
  y = 0,
  name="enemy"
)
SpriteBehaviour.Attach(enemy,
  texture="alien1",
  scale=2
)
PhysicsBehaviour.Attach(enemy)
EnemyBehaviour.Attach(enemy)
#etc.

{{< /highlight >}}

The equivalent now looks like:

{{< highlight python>}}
enemy = EntitySpawner.Spawn("enemy")

{{< /highlight >}}

Much nicer! Should help me maintain my sanity once I get a whole bunch of different enemy types in there.