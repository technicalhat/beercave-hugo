---
title : "Welcome to the Fantasy Zone"
description : ""
tags : []
date: '2009-07-30 12:34:44'
---

Little something I've been playing with over the last couple of days. The latest <a href="http://www.retrogamer.net">Retro Gamer</a> had a couple of mentions of Space Harrier, and somewhere along the line my brain went "hey! I could do that!"
So once I got back from Console Combat I thought I'd have a shot at knocking up a quick demo version...

Obviously, the first trick was getting the trademark scrolling hatched field up and running - since the original was all done with sprite scaling, I wanted to keep that fake 3d feel rather than going full-on openGL, so I whipped up something using textured quads as sprites.

{{< youtube OTtgwRqry2k >}}

Not *too* bad - the basic effect is there, although the grass texture looks bloody awful, and performance wasn't brilliant. Swapping the grass out for a flat green seemed to work better visually.
The first obvious point of attack for performance is that I was doing the 3D scaling calculations for each floor tile individually. Since the transform is based on the Z position, creating a FloorStrip object for each row, which then contained multiple Floor tiles meant I could only carry out the main transform once per row, handily knocking a couple of hundred ms off each draw cycle

<!--more-->

<img src="http://i24.photobucket.com/albums/c12/b33rman/gamedev/random/5292_126043093139_549778139_3098792.jpg" border="0" alt="Space Harrier engine test 2">

Then it occurred to me that I don't actually need to draw the individual tiles. If I just draw the horizontal and vertical strips with transparency on I can save a whole lot of mucking about, and only recalculate the scaling factors when the player moves up or down (which moves the horizon). That knocked the render time down even more, so I should have plenty of overhead when it comes to adding an actual game on top of it.

{{< youtube 1xSjRiwNLK8 >}}

The "render fps" value shown is what the fps would be if it wasn't framerate locked to 30fps in the code, based on the time it takes to draw everything.
After making the video above, I realised I only actually need to render every other horizontal strip to get the effect to work, for a current effective FPS of around 680 :D


Next job is to get a player sprite and some enemies in there and see about doing some violence to things with a great big gun!



