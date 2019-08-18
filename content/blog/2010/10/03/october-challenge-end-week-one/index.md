---
title : "October Challenge : End of week one"
description : ""
tags : []
date: '2010-10-03 20:59:05'
---

One week down on the October Challenge, and what do I have to show for it?

Well, the BeerEngine is coming along nicely. I'm about 90% of the way to feature complete now, with only the collision detection as a significant piece of missing functionality.

Other that that, I've pretty much got the prototype I knocked together last weekend rebuilt using the BeerEngine, and I'm just starting to hit a point where I'm seeing the benefit of having a reasonably well defined platform to build on top of. In the (currently on hiatus) XNA shooter game I was working on I was regularly running into the old <a href="http://en.wikipedia.org/wiki/Diamond_problem">Diamond of Death</a>, particularly when it came to setting up the "Piano Roll" level event system. Swapping inheritance for composition makes life much easier, at the expense of a little more verbosity in the setup code.

What was:

{{< highlight csharp >}}
var ship = new Ship(this)
            {
                position = new Vector2(640, 700)
            };
{{< /highlight>}}

 Currently looks more like:

<!--more-->

{{< highlight csharp >}}
new GameEntity()            
  .AddBehaviour(new MappedSpriteBehaviour(2))
  .AddBehaviour(new CameraBehaviour())
  .AddBehaviour(new TankControllerBehaviour())
  .SetProperty<PositionProperty>(new PositionProperty()
    {
      Position = Vector2.Zero
    }
  )
  .SetProperty<TextureProperty>(new TextureProperty()
    {
       Texture = ContentManager.GetTexture("sprites")
    }
  )
  .SetProperty<PositionProperty>(new PositionProperty(){ 
     Position = new Vector2(500,300)}
  )
  .SetProperty<RotationProperty>(new RotationProperty(){
    Rotation = (float)Math.PI
    }
  )
  .SetProperty<SpriteMapProperty>(new SpriteMapProperty(){
    TileX = 0,
    TileY = 1,
    TileWidth = 63,
    TileHeight = 63,
    OffsetX = 3,
    OffsetY = 3}
  )
  .SetProperty<OriginProperty>(new OriginProperty(){
    Origin = new Vector2(31,31))
  );
{{< /highlight>}}

Wrapping the various types of game object in some sort of Factory class ought to cut down on the noise level a tad.

So, what's the plan for Week 2? Well, I still need to get collisions working, obviously. I'm thinking I'll start with a fairly quick & dirty implementation of the <a href="http://en.wikipedia.org/wiki/Separating_axis_theorem">Separating Axis Theorem</a> once I wrap my head around the requisite maths, then add in additional optimisations as the need arises. Once that's in place, I can move ahead with some more game content. I figure given the time frame I've got to work within I can maybe afford 5 levels - just need to figure out what they should be without drifting <i>too</i> far into the old "ice level", "water level" etc. cliches

28 days remaining! I'm not panicking, I'm not panicking, I'm not panicking...
