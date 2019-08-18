---
title : "Lagertron update"
description : ""
tags : ["lagertron"]
date : 2012-09-12 22:20:30
---

I've managed to get a fair bit of work done on Lagertron (now Lagertron : 1664) since the last post. First off, I hacked together some simple touch controls and got it up and running on the Android tablet. The controls are far from perfect at this point but I wanted to make sure I had a decent performance benchmark that I could check in with so I don't get carried away working on the desktop version.

Once that was working, the next thing to do was to improve the enemy AI - so of course I was bitten by the shiny bug and started tarting up the title screen instead.

<p style="width:600px; margin-left:auto; margin-right:auto">
<img width="600" src="https://s3.amazonaws.com/beercave.co.uk/Lagertron/lagertron2.png"/>
<strong style="width:600px; display:inline-block; text-align:center">Ah, glow. The indie-dev's best friend.</strong>


<!--more-->

With that done, I quit mucking about and got stuck into adding some enemy behaviours - here's the result:

{{< youtube ZEoQiamEQgk >}}


<h2>The cast</h2>

<h3>The Mighty Beerman</h3>
<img style="float:left" height="64px" src="https://s3.amazonaws.com/beercave.co.uk/Lagertron/player.png">

Earth's Drunkest Hero. Only he can save mankind from the evil aliens of planet Lagertron and their diabolical scheme to steal all Earth's beer. Before chucking-out time.


<h3 style="clear:both;">Wunda Woman</h3>

<img style="float:left;height:64px" src="https://s3.amazonaws.com/beercave.co.uk/Lagertron/wonderwoman.png"/>
<em>Totally</em> non trademark-infringing and original character, this is the basic grunt enemy. Relentlessly chases down the player.


<h3 style="clear:both;">Doctor Terrible</h3>

<img style="float:left;height:64px" src="https://s3.amazonaws.com/beercave.co.uk/Lagertron/doctorh.png"/>
With his freeze ray he will stop the world. Luckily, he forgot to bring it today. This twisted medical maniac seeks out the beers which are the source of your power and transforms them into <em>alcohol-free beer.</em> Does evil know no bounds?


<h3 style="clear:both;">Ming the Markieless</h3>

<img style="float:left;height:64px" src="https://s3.amazonaws.com/beercave.co.uk/Lagertron/markie.png"/>
They say it's not easy being green. Maybe that's why he turned to evil. Either way, this viridian villain is quite a handful. Likes to hide away in corners where he spawns hordes of lethal pink fearies to battle our hero.


<h3 style="clear:both;">The Pink Fearie</h3>

<div style="float:left;width:64px;height:64px"><img style="margin-left:16px;height:32px" src="https://s3.amazonaws.com/beercave.co.uk/Lagertron/fairy.png"/>
</div>
Specialist subject : stabbing. Beware her lethal sparkle shots.


<h3 style="clear:both;">Mixed Grill Man</h3>

<img style="float:left;height:128px" src="https://s3.amazonaws.com/beercave.co.uk/Lagertron/mixedgrillman.png"/>
The <em>BANE</em> of your existence. Made invulnerable by his exclusive diet of mixed grills, this caledonian colossus is invulnerable to even the mighty Beerman's lasers. Avoid at all costs.


<h3 style="clear:both;">And the deadliest enemy of them all...</h3>
<p style="width:600px; margin-left:auto; margin-right:auto">
<img style="display:block;width:64px; margin-left:auto; margin-right:auto" src="https://s3.amazonaws.com/beercave.co.uk/Lagertron/yourmum.png"/>
<strong style="width:600px; display:inline-block; text-align:center">That's your mum, that is.</strong>

