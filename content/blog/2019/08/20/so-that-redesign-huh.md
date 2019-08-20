+++
date = "2019-08-20T19:33:00+00:00"
description = ""
tags = ["techie waffling"]
title = "So, that redesign, huh?"

+++
So yeah, here we are again in the Space Year 2019 with a shiny new website update that I'm about to bore you about.

So anyway, one of the things that's been putting me off updating (if you don't count the burnout) is the very slight degree of hassle that was involved in posting.

As a Big Damn Nerd who does this stuff for both money and fun I've never met a CMS I didn't hate on first contact - I've dabbled in Drupal, fear and loathe the horrifying collection of security holes that calls itself Wordpress, and don't even get me started on Umbraco; static site generators pretty much had me at "hello"

<--more-->

But yeah - back in the before-times of 2013 the blistering speed and dirt-cheap hosting of static sites came with the downside of having to do my content editing offline. Write up content at home, run a bunch of build scripts to test the end result, then copy the output back onto the web server. Bit of a faff really, you can kind of see the output drop right around the point I adopted it.

But this is now - in the shiny future of 2019 I can swap out the boring, stable, locally-installed toolchain of the past in favour of a hastily cobbled-together chain of free-as-in-you're-the-product SaaS providers, and that's just what I've done!

So the new tech stack for the site is:

* Shiny new responsive [Bootstrap](https://getbootstrap.com/) layout
* [Hugo](https://gohugo.io/) static site generator
* Content stored as [Markdown](https://en.wikipedia.org/wiki/Markdown) files in a [github](https://github.com/) repo
* [Forestry.io](https://forestry.io/) for content editing, which checks edits back into github
* [CircleCI](https://circleci.com/) continuous integration watches the github repo for changes and runs Hugo on every checkin to produce the static files which get checked back into
* Another github repo which is being served via [github pages](https://pages.github.com/)

I feel extremely devops right now...