---
title : "Gah! part 2"
description : ""
tags : []
date: '2009-01-10 01:00:00'
---

OK, that seems to have fixed it.

Turns out Rabbyt caches textures internally, so just reloading the images for my sprites didn't make any difference.

A little bit of digging around in the source and I managed to work out how to empty the texture cache. Once that was done I just had to refresh the textures for anything already existing and everything was happy again.

Of course, now I've found a new problem. All my sound effects seem to be playing about 0.5 seconds out of sync with the game. Grr...

EDIT : OK, that was easy enough. Just needed to bump up the buffer size a little.

<!--more-->