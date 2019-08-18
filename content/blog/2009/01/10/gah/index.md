---
title : "Gah!"
description : ""
tags : []
date: '2009-01-10 00:00:00'
---

Been adding a few more things in, of which more details later.

Right now, I'm working on being able to switch the game to fullscreen mode.

Switching modes is simple enough, but suddenly all my sprites are rendering as solid white blocks. The only things displaying properly are a couple of things that are dynamically loaded.

Looks like I need to reinitialise all my textures when I switch video mode, which is gonna mean a wee bit of rearchitecture...

Damn!

<!--more-->