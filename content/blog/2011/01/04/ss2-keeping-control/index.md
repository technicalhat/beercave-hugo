---
title : "SS2 : Keeping control"
description : ""
tags : []
date: '2011-01-04 22:49:20'
---

I've managed to get the Sheep Snaggers 2 redevelopment off to a good start so far.
So far I've got sprites, movement and a simple camera system up and running, which is enough to get me my ship up and flying over a pretty boring and empty landscape.

It helps that Python massively lends itself to component-based architecture. When I started building DethTank in C# I had to build a whole bunch of functionality myself to be able to attach behaviours to components at runtime. With Python, I just define my behaviours as functions and attach them to the GameObject at runtime. Saves a lot of tedious messing about with interfaces...

I also spent a bit of time this evening abstracting out my input system, which should save me some pain down the line. In the previous games, the input handling code was buried in the player classes and looked something like this:

{{< highlight python >}}
if stick:
    x = stick.get_axis(0)
    y = stick.get_axis(1)
else:
    if keys[K_LEFT]:
        x = -1
    elif keys[K_RIGHT]:
        x = 1
    if keys[K_UP]:
        y = 1
    elif keys[K_DOWN]:
        y = -1
{{< /highlight>}}

Not only was this annoying to keep track of, it basically means there was no chance of adding in user configurable controls.
The equivalent piece of code in the Sheep Snaggers 2 looks like:

{{< highlight python >}}
x = input.GetAxis("HORIZONTAL")
y = input.GetAxis("VERTICAL")
fire = input.GetState("FIRE")
{{< /highlight>}}

The input class (which I'll post once it's done) maps the various available controllers to named controls, with the internal mappings looking like:

{{< highlight python >}}
#key/button states
self.stateMap = {
    'THRUST' : [['keyboard', (K_SPACE,)]],
    'FIRE' : [['keyboard', (K_LCTRL,)]]
}
#axis states
self.axisMap = {
    'VERTICAL' : [
        ['keyaxis', (K_UP, K_DOWN)],
        ['joyaxis', (1,1)]
    ],
    'HORIZONTAL' : [
        ['keyaxis', (K_UP, K_DOWN)],
        ['joyaxis', (1, 2)]
    ]
}
{{< /highlight>}}

<!--more-->
Later on, it should be easy enough to build something into the GUI to make the controls configurable at runtime or support multiple pre-defined control systems without any of the game code knowing anything's changed.

Next job : finish up the input wrapper and see about adding in the sheepies and aliens to make things a bit more interesting visually.
