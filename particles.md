# opengl/particles
A basic 2d particle simulation.

## quadtree collisions (2020-07-16)
With a simulation of 500 particles, checking each particle against every other
particle for collisions results in approximately 15 million checks per second.  
After implementing a quadtree to selectively check collisions this has been
reduced to around 35,000.

*This is much less than the expected count of around 80 thousand. Perhaps this
is mistake in the counting?*

In addition to the reduced number of collision checks, the average frame time
has reduced from approximately 16ms to approximately 14ms.  

## instanced rendering
As each particle only differs by the model matrix, instanced rendering may be
used to significantly reduce the number of draw calls.  
This may result in a noticable speed increase?

## threads?
It may be possible to take advantage of multi-threading or parallelisation to
improve performance in certain areas.  
- calculating the attracition between particles should be possible
- updating the particles position should be possible
- collision may require some tweaks to ensure algorithm is deterministic?
