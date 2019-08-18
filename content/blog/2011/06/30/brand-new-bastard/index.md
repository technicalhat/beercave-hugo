---
title : "Brand new Bastard"
description : ""
tags : []
date: '2011-06-30 22:17:39'
---

With [SS2](/content/sheep-snaggers-2) finally fixed up and shipped, I've been thinking about [what to work on next](/2011/06/02/now-what). While I'm still pretty keen to make a crack at some of the ideas in there, I can't help but think I should really finish up [Gun Bastard](/content/gun-bastard) first.

With that in mind I took a quick look at the old codebase, went 'uurhg!', and promptly binned the lot and started again ('cos that's just how we roll in indie-land).

What I've got so far looks like this:

<a href="http://s24.photobucket.com/albums/c12/b33rman/gamedev/gun%20bastard/?action=view&amp;current=screen019.jpg" target="_blank"><img src="http://i24.photobucket.com/albums/c12/b33rman/gamedev/gun%20bastard/screen019.jpg" border="0"></a>

Doesn't look like much so far, but the new stuff is a lot easier to work with.

Inspired by <a href="http://gl33k.com/blog/2011/6/27/a-metronome-for-everyone.html">this article</a> I thought it might be cool to have the AI synced to an external timer, so I hacked up a basic events system that I could drive with my metronome class. Right now all it does is make the enemies change direction every beat but I'm planning on making it the core of the game AI and hopefully hooking it up to the audio system so that events happen in time with the soundtrack. If it works out, it should be awesome :D

<!--more-->