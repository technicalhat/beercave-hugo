---
title : "Beerman's adventures in voxel-land, part 2 : Blowing Chunks"
description : ""
date : 2015-01-20 21:47:00
---

Been a manic weekend - between getting stranded in a pub all afternoon while out buying a new Beermobile (I know. My life, it is filled with troubles...) and general weekend activities, I managed to squeeze in a couple more evenings of coding time on the voxel project. It's starting to come together quite nicely now.

Previous Entries : [Intro](/blog/2015/01/14/beermans-adventures-voxel-land) [Part 1](/blog/2015/01/15/beermans-adventures-voxel-land-part-one-triangles-cubes-blocks-oh-my)

<!--more-->
 
## Day 3 :

Well, that turned out to be a fairly productive evening. First off, I took the working Block rendering code from the end of day two, and broke it out into a separate Chunk class to keep things tidy. With that working, I added a Chunk manager to keep track of multiple chunks. 

Since I'm in full "build one to throw away" mode here (also, very lazy), I'm keeping it restricted to what I need for the current project. That means the current iteration of the Chunk manager is hard coded to work with a scrollable arbitrary length world of 7x7 chunk "slices" - effectively a long tunnel (coincidentally, I was thinking a Star Wars style Trench Run game might make a good candidate for a second game to build on this).

{{< figure src="chunks.png" alt="My voxel world. That's a lot of boxes." >}}

So, at the end of day 3 I've got a functional proof of concept up and running and flying back and forth through a 7x7x100 mesh of voxel Chunks. At 3FPS, performance leaves a little to be desired though - hardly surprising since each individual cube in the world is currently issuing a separate OpenGL drawArrays call for a total of 86240 cubes per frame. 

Fixing that will obviously need to be the focus of day four's efforts, but before that :

{{< figure src="error.png" alt="That's not good" caption="Uh-oh!" >}}

Yeah, I should probably fix that first...

## Day 4 :

Didn't get a chance to work on this over the weekend, because cars, but here's the hour or so's development I managed to squeeze in on Monday night.
First up, I made that annoying memory access error go away - turns out calling win.Close() mid-render isn't very sensible. Moving it to outside the render loop made it start behaving itself.

After that I got down to speeding up the rendering to something slightly more sensible. The main problem was that every single voxel being displayed was making its own OpenGL draw call - hardly efficient, but I'm working on the principle that I'd rather see the naive implementation working right away than spend a couple of hours crafting something optimised and then not know why it's not doing anything.

So, the obvious speed enhancer is to build a mesh per-chunk, as described [here](https://sites.google.com/site/letsmakeavoxelengine/home/display-lists-or-vertex-buffers).

Right now, again for speed of development, it's generating all the meshes on startup, which gives me something like a 9 second delay before anything starts rendering, but once it does it's hitting a solid 60FPS and we're down from 82000 draw calls to 490.
There's just one slight problem...

{{< figure src="wut.png" alt="WAT" caption="I'm not sure what I've done here, but it looks pretty cool" >}}