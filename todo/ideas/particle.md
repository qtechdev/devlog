# Particle Generator

A generator will spawn particles at the given rate until either the diration
has elapsed or the spawn count has been met.

generator properties
- spawn rate
- do_burst_spawn
- duration/count
- \*particle properties ranges

could add physics to generator, e.g. for smoke grenade?

Each particle will be spawned with properties that are randomly selected within
the generators specified ranges.

particle properties:
- velocity
- direction
- size
- opacity
- colour/texture
- lifetime (can be infinite)
- die_on_collision

additional (optional) particle properties:
- use_physics (must have mass set)
- mass (should be non zero unless the physics engine can handle zero-mass particles)
- shrink rate
- fade rate
- colour/texture transformation?
