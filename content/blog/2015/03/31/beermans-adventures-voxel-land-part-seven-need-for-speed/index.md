---
title : "Beerman's adventures in voxel-land, part 7 : Need for speed"
description : ""
date : 2015-03-31 22:45:00
---

Previous Entries : [Intro](/blog/2015/01/14/beermans-adventures-voxel-land) 
[Part 1](/blog/2015/01/15/beermans-adventures-voxel-land-part-one-triangles-cubes-blocks-oh-my) 
[Part 2](/blog/2015/01/20/beermans-adventures-voxel-land-part-two-blowing-chunks) 
[Part 3](/blog/2015/01/22/beermans-adventures-voxel-land-part-three-it-moves)
[Part 4](/blog/2015/01/25/beermans-adventures-voxel-land-part-four-now-featuring-actual-gameplay)
[Part 5](/blog/2015/03/25/beermans-adventures-voxel-land-part-five-the-hard-parts)
[Part 6](/blog/2015/03/25/beermans-adventures-voxel-land-part-six-the-best-laid-plans)

With the basics of the trench runner working, I wanted to take a look at a performance issue that'd been giving me trouble - the initial version of the engine was pretty much limited to only seeing about 10 chunks ahead if I wanted to keep it at 60fps, which was giving me some pretty visible popup on the far end of the trench. 

The problem was in the mesh generation for my chunks. I had the basic optimisation in place of not adding faces to the mesh that were in between adjacent filled blocks, but that meant that for a completely solid chunk I was still rendering hundreds of little cubes where one would be enough.

<!--more-->
 
A spot of googling helped me find something called a greedy meshing algorithm. Basically, you take 2d slices across each chunk in every direction, then for each slice, the greedy algorithm starts in the top left corner and identifies the largest rectangle it can make consisting only of filled squares. Once that's done, it adds the rectangle to the mesh and continues from the next unprocessed square until all squares in the slice have been processed

<div class="row">
{{< figure src="meshing1.png" alt="Start with top left filled square." wrapperclass="col-md-6">}}
{{< figure src="meshing2.png" alt="Expand right and down until we can't make a bigger rectangle." wrapperclass="col-md-6">}}
{{< figure src="meshing3.png" alt="Add rectangle to mesh and remove squares from slice." wrapperclass="col-md-6">}}
{{< figure src="meshing4.png" alt="Continue with next filled square." wrapperclass="col-md-6">}}
</div>

After a *lot* of swearing, I got a successful implementation up and running, which cut my rendering action from upwards of 10 million triangles a frame to somewhere closer to 300,000, and let me push the render distance out past 100 chunks without affecting the framerate.

<div class="row">
{{< figure src="unoptimised.png" alt="Before meshing" caption="Before meshing" wrapperclass="col-md-6">}}
{{< figure src="optimised.png" alt="After meshing" caption="After meshing" wrapperclass="col-md-6">}}
</div>

And here it is in action

{{< youtube 5cTDfB4jubc >}}

