---
title : "Beerman's adventures in voxel-land, part 3 : It moves!"
description : ""
tags: ["voxel engine"]
date : 2015-01-22 21:47:00
---

{{< youtube 9L8ty8SaMcY >}}

Busy evening!! 

Previous Entries : [Intro](/blog/2015/01/14/beermans-adventures-voxel-land) [Part 1](/blog/2015/01/15/beermans-adventures-voxel-land-part-one-triangles-cubes-blocks-oh-my) [Part 2](/blog/2015/01/20/beermans-adventures-voxel-land-part-two-blowing-chunks)

<!--more--> 

## Day 5

First up, I fixed the rendering problem. Turns out the mesh builder was just creating the triangles for my cubes all wrong.
That's what I get for copy and pasting the vertex list from the internets. To fix it, I shrunk the world down to a single chunk and zoomed right in on it to see what was being drawn. 

{{< figure src="fixingcube.png" alt="Close up on the cube" caption="Part way through, got a couple of faces drawing correctly now." >}}

Once I could see what I was doing, I had the test grid back up and running in no time.

{{< figure src="fixedcubes.png" alt="The grid" caption="Hooray, we're almost back to where we were on day 3!" >}}

Next thing was to update the mesh builder to add colour back in.

{{< figure src="colourcubes.png" alt="The grid, once more in colour" caption="Now we're back to where we were on day 3!" >}}

For once, I actually had a bit of time to play around after fixing the previous night's bugs, so I updated my setup code to generate 
a fairly basic height-mapped landscape, which came out looking quite nice and videogamey.

{{< figure src="landscapes.png" alt="Heightmapped landscapes" caption="Yeah, this is pretty much what I'm looking for." >}}

Suppose I should start thinking about turning it into a game now, then...
 
