---
title : "2010 and all that"
description : ""
tags : []
date: '2010-12-31 19:11:29'
---

Well, the year's just about up. S'pose I should do a bit of a review/postmortem and figure out how to make the next one even better.

In general, 2010 was pretty good to me; the only real problem I've had is a terrific lack of motivation. I can probably put at least part of that down to a completely manic year at work, which meant that most nights the last thing I wanted to see when I came home was another goddamn IDE.

The rest I think I can mostly put down to convincing myself I should be a 'real programmer' - if there's one thing that's common to all my aborted/stalled projects it's a stubborn insistence of writing all the engine gubbins from scratch, only to drop it like a rock as soon as I hit performance problems. In contrast to that, I built <a href="/content/dump-and-jump">Dump and Jump</a> in Construct, which takes care of all that for me, and never hit that same point of dreading picking up the project again.

If there's a lesson there, it's that I'm not a damn engine programmer, so why do I keep starting out by trying to write an engine? I don't want to spend my time figuring out how to shave 15 milliseconds off my collision detection loop, I want to make things go 'splodey all over the place!

With that in mind, I'm cutting my losses there and moving my development platform to <a href="http://unity3d.com/">Unity3D</a>. It's cross-platform (including iPhone and XBox360), it speaks C#, which is my main language, and it's component based, which is what I was trying to achieve with the <a href="/category/tags/beer-engine">BeerEngine</a> before I hit the now traditional performance problems and got bored.

My current plan for existing projects is as follows.

<a href="/content/sheep-snaggers-2">Sheep Snaggers 2</a>:

<!--more-->

Needs a big chunk of refactoring, but the codebase can stay in python as there isn't anything major that needs adding, just tweaking the game content to be worthy of a release. Also Paul Drury from <a href="http://www.retrogamer.net/">Retrogamer</a> has been nagging me about it every time I've seen him for the last couple of years so I should really get it done... Most likely this will be my last pygame project for the foreseeable future as I shift development over to Unity.

<a href="/category/tags/dethtank">DethTank</a>:
The DethTank project pretty much died as I lost interest in developing the BeerEngine into a fully fledged framework for game dev. If I convert the graphical assets over to 3D models it should make a pretty good first project for Unity.

<a href="http://www.youtube.com/watch?v=H2MH_cNPBsU">Untitled XNA project</a>:
Not finishing this one bothers me more than the others as it was a collaborative project. Sorry Leo, it'll get done at some point! The prototype was coming along pretty well before I hit the wall, so I should be able to resurrect it fairly quickly, and with the cross-platform-iness of Unity we should still be able to get Xbox *and* Mac builds out.

<a href="/content/gun-bastard">Gun bastard</a>:
This never really progressed beyond a bunch of graphics and some basic sprite movement code so it's a pretty good candidate for shifting to Unity, or possibly Construct - it doesn't need anything too sophisticated under the hood. The main thing holding it back was an unwillingness to write any kind of framework for setting up level content, so handing that part off to something already written should get things moving again.

Overall, I'll be happy if I can get at least a couple of those into a fit state for release during 2011. If I can convince anyone to part with their cash for any of them, so much the better! 

Have an awesome year, all!