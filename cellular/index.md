# cellular automata
Cellular Automatas demonstrate emergent properties from simple rules.  
A well known example is John Conway's game of life; a 2D automata where each
cell is either "dead" or "alive" based on the state of its immediate neighbours.

## elementary
A more fundamental set of automata are elementary cellular automatas.  
These are a set of 256 one dimensional automata referred to by their "Wolfram
code".  
Each generation of a given automata can be stacked on top of each other,
forming a 2D texture where the y-axis represents time.
By altering the initial starting comditions (a single "alive" cell, a random
sequence, etc.) each rule can display variuos sets of behaviours

[more](elementary)

## multiple states
The complexity of a given automata can be increased by giving each cell more
than two states and supplying a rule set that takes that into account.

## Conway's Life
This concept is more well known as John Conway's game of life; a 2D automata
where the rules for each cell are based on population count rather than a
specific configuration.  
Like the Chip8 interpreter, Conway's life has been ported to many different
systems, using many different languages.

## Langton's Ant
An alternative type of rule set can be implemented by focusing on a single cell
via a pointer, usually referred to as a "turmite". Langton's Ant is the most
basic form of these "turmites".

When the turmite enters a cell, the cell is advanced to the next colour in the
chain. The turmite then turns clockwise or anti-clockwise (depending on the
rule set) and moves forward to the next cell.
