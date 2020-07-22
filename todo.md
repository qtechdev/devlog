# todo list
## readmes
__(added: 2020-07-17, completed: ...)__

I should add readmes with a unified format:
- program name
- short description
- basic example
- dependencies

## changelogs
__(added: 2020-07-17, completed: ...)__

It could be helpful to keep track of changes?
I would need a version/release system?

## documentation
__(added: 2020-07-17, completed: ...)__

Documentation could be helpful

## trello
__(added: 2020-07-22, completed; ...)__

Investigate trello?
https://trello.com/home
https://blog.trello.com/github-and-trello-integrate-your-commits

## totalistic cellular automata
__(added: 2020-07-19, completed: ...)__

https://mathworld.wolfram.com/TotalisticCellularAutomaton.html

## libraries
__(added: 2020-07-17, completed: ...)__  

I have pulled some code out into libraries (fio, xdg, etc.), each repo should
be updated to use these libraries instead of bundling code?  
I might move the opengl code into a library instead of reusing it so often.  

*Making the code in these libraries as concise and efficient as possible should
be a goal.*

## lua scripting
__(added: 2020-07-22, completed: ...)__

Look at integrating lua scripting.
Demonstrate capabilities via a basic OS where each program is a lua script?

## particle generators
__(added: 2020-07-22, completed: ...)__

Particles (and particle generators) are often used for graphical effects.

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

## nes/gameboy graphics
__(added: 2020-07-22, completed: ...)__

https://www.youtube.com/watch?v=57ibhDU2SAI
Create a rendering pipeline in the style of nes/gameboy.
- tiles/sprites
- colour palettes
- layers

I would like to write a full emulator at some point.

## unit tests and performance analysis
__(added: 2020-07-17, completed: ...)__

Especially for libraries, but also for programs.

## pkgbuild and aur
__(added: 2020-07-19, completed: ...)__

https://wiki.archlinux.org/index.php/Creating_packages

## cross platform code
__(added: 2020-07-17, completed: ...)__

I am currently only compiling and testing on Linux. Most of these programs
should compile for Windows (and Mac?) as is, others may require some changes?

## ~submodules~
__(added: 2020-07-18, completed: 2020-07-19)__

https://git-scm.com/book/en/v2/Git-Tools-Submodules  
https://git-scm.com/docs/gitmodules  
