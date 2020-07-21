# classyfing images of cellular automata
As the cellular automata is intended to extend infinitely in each direction,
there is a problem when creating a simulation in finite space.  
A simple approach to this is to consider any cell outside of the simulation to
be a fixed value (in the case of my simulation, a `0`).

For most simulations this is adequate, however some rules will introduce
features from outside of the grid. In order to ensure that these additional
features do not interfere witht the main feature, I have set a suitable width.  
I did consider cropping the sides of these images to focus on the central and
main feature, but some of them are interesting.

---

## basic observations
- All even rules (and 0) show a single feature on an empty background.
- Odd rules up to (and including) 127 have a striped background.
- Odd rules above 127 show their feature as empty cells on a filled background.
- Odd rules may have additional features, but even rules do not.

## mirrors and complements
Each rule has a mirror and a complement.  
A mirrored rule is one that is flipped across the y axis.  
The complemet of a rule is one that is inverted, i.e. `live` cells become `dead`
and `dead` cells become `live`.

## `single_1` evolutions
All rules with a single live cell as the initial state. [here](single_1)
