---
title : "Reasons to love Python"
description : ""
tags : []
date: '2009-07-22 20:07:07'
---

It lets you do twisted things like this:

{{< highlight python>}}
waves = [[Clown, Clown, Clown],
    [Clown, Tank, Bunny, Clown],
    [Clown, Tank, Tank, Clown],
    [Clown, Tank, Tank, Bunny],
    [Tank, Tank, Tank, Clown],
...
]
{{< /highlight >}}

where Clown, Tank and Bunny are the _Types_ of the various enemies

and later...

{{< highlight python>}}
for enemy in waves[wave]:
    enemy(xpos, ypos, 0, 0, self.target)
{{< /highlight>}}

and it just figures it out and calls the constructor for the relevant type.

<!--more-->