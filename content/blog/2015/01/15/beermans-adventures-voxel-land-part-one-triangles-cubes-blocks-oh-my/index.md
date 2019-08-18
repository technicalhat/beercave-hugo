---
title : "Beerman's adventures in voxel-land, part 1 : Triangles and cubes and blocks, oh my!"
description : ""
date : 2015-01-15 22:42:00
---

As [previously mentioned](/blog/2015/01/14/beermans-adventures-voxel-land), I'm having a crack at building my own voxel engine, because that's the sort of thing we do for entertainment around these parts. 

Here's how it's looking after a couple of evenings of development.

<!--more-->
 
## Day 1 : Pain, then triangle!

Ah, new projects, starting from scratch - always such *fun*... 

So yeah, most of the first day's development time was spent swearing at my computer in a vain attempt to get it to do _anything._ About typical for starting a fresh project with new tools, really.

I've pretty much had it with java development, but that's a rant for another day. As a .Net web-monkey by day, I'm switching to a platform I actually like working with and giving [SFML.Net](http://www.sfml-dev.org/index.php) a try. So, most of day 1 was spent in standard open source project user fashion - figuring out the inconsistencies between the documentation, the samples, and the current release. Joy!

Eventually, after much annoyance I managed to get this _amazing_ triangle to appear on my screen. Well worth 3 hours of effort, I'm sure you'll agree.

{{< figure src="triangle_color.png" alt="A triangle" caption="Yep, that's a triangle. It sure is... triangular." >}}

## Day 2 : A wild Block appears!

With my new triangle rendering skills, day 2 went a lot smoother. It didn't take a huge amount of modification to turn my single triangle into a perfectly rendered cube.

{{< figure src="cube.png" alt="A cube, yesterday" caption="A cube, yesterday" >}}

And with cubes working, it wasn't a huge step to a 16x16x16 array of cubes, or Blocks.

{{< figure src="box.png" alt="A voxel box - a boxel?" caption="A voxel box - a boxel?" >}}

{{< figure src="overlap.png" alt="Coloured Voxels" caption="Yeah, we're really pushing the envelope now" >}}

The eagle eyed might notice that there's a bit of a problem with the rendering order - the blocks on the top right are overlapping blocks they're supposed to be behind. I'd fix it, but I'll be rewriting the block rendering to work as a single mesh anyway rather than a bunch of individual cube meshes so there's not much point.
