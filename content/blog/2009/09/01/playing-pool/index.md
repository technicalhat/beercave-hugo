---
title : "Playing pool"
description : ""
tags : []
date: '2009-09-01 22:06:16'
---

I've noticed the frame rate on Gun Bastard has a tendency to plummet when things get a bit splodey, so I should probably start looking at optimising the code a little before I go any further.
Since the explosions are the most obvious source of slowdown, at least some of the problem is likely down to object creation overhead on the various particles I'm chucking about the screen.

In order to minimise the overhead, I thought I should investigate <a href="http://sourcemaking.com/design_patterns/object_pool">object pooling</a>.

Seemed like a good idea to run some tests first and get a handle on what kind of performance improvement I could expect from it, so I hacked together a quick particle pool class to try it out:

{{< highlight python>}}
class ParticlePool():
    def __init__(self):
        self.pool = []

#gets a particle from the pool if any are available, and creates a new one if not.
def getParticle(self, list):
    pool = self.pool
    if len(pool) > 0:
        obj = pool.pop()
        obj.init(list)
    else:
        obj = Particle(list)
        obj.pool = self
    return obj

#releases a particle back to the pool.
def release(self, particle):
    self.pool.append(particle)

#empty the pool
def clean(self):
    self.pool = self.pool[:]
{{< /highlight >}}

and a basic test harness to check on how it performs:

{{< highlight python>}}
#function to kill particles, for use in the map function later
def kill(p):
    p.die()

particles = []

#pool is empty. get some new particles
for i in range(0,count):
    pool.getParticle(particles)

#return all particles to the pool
for p in particles[:]:
    p.die()

#get some particles again, now that the pool is filled
for i in range(0,count):
    pool.getParticle(particles)

#return the particles to the pool again
    map(kill, particles[:])

#remove all particles from the pool
    pool.clean()
{{< /highlight >}}

<!--more-->

Note that the second time I release the particles I'm using map() and the kill function. Thought I might as well check how well that outperforms using a regular python loop.

Results testing with 100, 1000 and 10,000 objects are as follows:

* Got 100 unpooled particles in <strong>0.013000s</strong>
* Unpooled fps equivalent : 76.923077
* Returned 100 particles to pool in 0.002000s
* Got 100 pooled particles in <strong>0.001000s</strong>
* Pooled fps equivalent : 1000.000000
* Returned 100 particles to pool in 0.001000s
* Advantage factor of pooling = <strong>13.000000</strong>

=======================================

* Got 1000 unpooled particles in <strong>0.165000s</strong>
* Unpooled fps equivalent : 6.060606
* Returned 1000 particles to pool in 0.016000s
* Got 1000 pooled particles in <strong>0.012000s</strong>
* Pooled fps equivalent : 83.333333
* Returned 1000 particles to pool in 0.009000s
* Advantage factor of pooling = <strong>13.750000</strong>

=======================================

* Got 10000 unpooled particles in <strong>1.838000s</strong>
* Unpooled fps equivalent : 0.544070
* Returned 10000 particles to pool in 0.226000s
* Got 10000 pooled particles in <strong>0.126000s</strong>
* Pooled fps equivalent : 7.936508
* Returned 10000 particles to pool in 0.131000s
* Advantage factor of pooling = <strong>14.587302</strong>

=======================================

Looks like I can reasonably expect an order of magnitude of improvement in my object creation code using object pools. Groovy.
Using map() for the cleanup is also running approximately twice as fast as a normal python loop, so that's something else I should probably be doing.