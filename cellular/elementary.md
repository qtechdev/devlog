# elementary cellular automata (2020-07-17)
## cell
Each cell consists of four values:
- its state
- red, green, and blue, colour channels

The cell's state is an 8 bit value, allowing for up to 256 unique states.

## rule
A rule consists of an index (representing the cell's ancectors) and a new state
value. The index is a 64 bit value to hold the states up to 8 ancectors.  
For each cell, its ancectors are converted to an index into the rule set and
its state is updated accordingly.

## visualisation
A generation of cells is represented as a single row of pixels in the final
texture, with each generation being stacked below. This gives time represented
as the y axis.

## initial conditions
Four initial conditions are available to choose from via keyboard shortcuts:
- `0`: sets all but the central cell to `1`
- `1`: sets the central cell to `1`
- `r`: randomly generates the first generation
- `a`: alternates between `0` and `1` for each cell

# todo
- clear texture on reset
- allow changing of rule sets at runtime
- allow creation of custom rule sets (via config file?)
- more states (should be trivial, rule set should already support it)
- add option to save images?
