---
title : "Post Mortem : Sheep Snaggers 2"
description : ""
tags : []
date: '2011-05-24 22:56:57'
---

I released [Sheep Snaggers 2](/content/sheep-snaggers-2) on Friday at <a href="http://www.retrovision.org.uk">Retrovision 2011</a>, to what was overall a pretty good reception. All being well, I'm hoping for a fairly positive writeup in the <a href="http://www.retrogamer.net">Retrogamer</a> review of the event.

The high score competition I had running over the weekend was popular, though made somewhat more difficult than anticipated by the fairly low-end laptops available to play it on - I didn't pay a great deal of attention to performance optimisation so when it landed on a machine with 32MB of shared video RAM there were... <em>issues.</em>

Luckily I managed to source an alternative machine which left the game playable with only occasional slowdown, but I'm not entirely happy. At the end of the day it's only a bloody Defender clone; there's really no excuse for it to not run on damn near any hardware you can throw at it, so I'm planning to spend a little time sharpening up the performance before I move on to my next project.

Retrogamer's article on the event should be hitting the stands around the middle of next month, so that seems like a reasonable short term deadline to get a version 1.1 together and iron out some of the speed issues before that hopefully points some more attention this way

<!--more-->

<h3>So, the plan.</h3>

I'll probably need to spend some time profiling to be certain, but I'm pretty sure the biggest problem is that I'm being incredibly lazy with my texture memory usage. I've got limited spritesheet support in there for some of the animations, but for the most part it's one texture per sprite. Worse, for some of the font routines I'm generating one texture per combination of character/font/size.

Since my development system has 96 cores and a gig of video RAM, that's not really something that's been an issue for me, but I should probably look into addressing it. First on the list there should be packing all my graphics into as few textures as possible, which may mean finally venturing into writing my own development tools. Nothing fancy, just something that takes a folder of PNG files and turns them into packed images and a handy code file with all the texture coordinates in - something along the lines of:

{{< highlight python>}}
{
  #use the original filename as a key to the texture dictionary
  #cuts down on the amount changes needed to the existing code
  #and makes it easy to cross reference with the original unpacked sprites
  "alien1.png" : {
    "texture" : "texturemap1.png",
    "tex_shape" : [0,1,1,0], 
    "shape" : [-50,50,50,-50] 
  }
}
{{< /highlight>}}

With that done, it won't need a massive amount of work to update my drawing routines to load sprites from the packed textures rather than individual files.

The next (and possibly much bigger) problem is the fonts. Right now I have a kind of hybrid system that sometimes generates textures for individual characters (e.g. in the high score counter) and sometimes for entire phrases (like the "SHEEPIE SAVE" message). It would probably help if I defined these up-front rather than building them on the fly as the game runs just because I'm lazy. One texture per font and a couple of special cases for the floating messages shouldn't really be all that much work.

Hopefully, by the time I've got those out of the way I should have managed to come up with a few ideas to play with for my next project.
