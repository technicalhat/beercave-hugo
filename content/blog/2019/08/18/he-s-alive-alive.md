+++
date = "2019-08-18T19:36:00+00:00"
description = ""
tags = ["burnout", "ramblings"]
title = "He's alive! ALIVE!"

+++
So it's been...

Holy shit! It's been FOUR. FUCKING. YEARS. Probably worth a bit of a recap then...

[When last we paid visit to Beercave Towers](/blog/2015/07/06/egad-a-post/), I'd just gotten done releasing the voxel games. After that, things went a wee bit haywire. Let's see:

<!--more-->

* Well, Lemmy died for a start - still pretty sure that was the point where we diverged into the darkest timeline.
* ![](uploads/The_darkest_timeline.gif)
* 2016 - just... fucking... 2016...
* I did manage to get a game out among all the chaos though...[ it's not bad](/games/space-bastards/)
* House move
* Car wreck _during_ house move - that was all kinds of fun...
* Burnout
* Wicker man
* ![](uploads/46458636_10156943771863140_3512273638755663872_n.jpg)
* Thunderdome
* ![](uploads/full with beerman.jpg)
* More burnout
* Siege weapons
* ![](uploads/vlcsnap-2018-02-27-19h40m50s853.png)
* Hot tub - didn't exactly _help_ with the burnout but it's a great way to avoid thinking about it
* Ramm-Shrine
* ![](uploads/vlcsnap-2018-02-27-19h40m50s853.png)
* Drinktober!
* ![](uploads/IMG_20181031_190651.jpg)
* Decem-bier
* ![](uploads/WithLighterv2.jpg)
* Rammstein
* ![](uploads/IMG_20190608_214859.jpg)
* More Rammstein
* ![](uploads/IMG_20190706_220345.jpg)

And that about brings us up to date.

So anyway, one of the things that's been putting me off updating (if you don't count the burnout) is the very slight degree of hassle that was involved in posting.

As a Big Damn Nerd who does this stuff for both money and fun I've never met a CMS I didn't hate on first contact - I've dabbled in Drupal, loathe Wordpress, and don't even get me started on Umbraco; static site generators pretty much had me at "hello"

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