# snake

A fairly straight-forward program, primarily for the purpose of learning a bit
about ncurses.
[full code available here](https://github.com/qtechdev/snake).

## ncurses
Four ncurses windows are created;
- a small box containing information
- the border for the bottom portion of the screen
- two windows that sit inside the lower border and can be swapped

The `halfdelay` setting is used to implement a basic game loop. If a set
amount of time has passed then the loop will no longer wait for an input from
the user and enter the loop body.  

## timing issues
There are two isues arise in terms of timing:
- By handling the game loop in this way (using `halfdelay`), the game can be
sped up by pressing any button.
- The snake travels faster in the y-axis than the x-axis due to the non-square
nature of the characters.

The first issue can be solved by simply using a proper game loop, but the
second is more complex.  
One potential solution is to store the snakes head position as a float and
update the body/check for collision only when the head crosses an integer
boundary.
This introduces its own flaws as the snake will now appear to move _slower_
along the y-axis due to the lower visible update rate. This method also depends
on the font size matching the update increments properly to achieve the desired
effect.

The other solution is, of course, to use something other than ncurses.

## program state
The program keeps track of its current status and updates its logical state
accordingly.  
Starting in the `MENU` state, the player is shown a short description of the
rules and controls. Pressing the spacebar will change to the `RUNNING` state.  
The snake body is represented by a `deque`. On every frame, the current head
position is pushed onto the front of the body before being moved. Then the body
length is checked and a body segment is popped from the back end to keep the
snake below the maximum length. This gives the appearence that the snakes body
is moving but without having to update each body segment.  
The game also ensures that a set number of food objects exist at any given time.
If the head of the snake occupies the same grid cell as a piece of food then it
is removed, and the snake maximum length (and score) is increased by 1.
If the head of the snake collides with its body or a wall then the game state is
advanced to `GAME_OVER` and the player is presented with their score, and the
option to start a new game.  
The player also has the option to pause the game at any time. While in the
`PAUSED` state, the game state is not updated and the word `PAUSED` is displayed
using the secondary lower window. upon unpausing the secondary window is cleared
and the game resumes.

## pointer lifetime
Additionally, I have used a class to manage the lifetime of the ncurses window
pointer. This is probably unnecessary, however this knowledge could potentially
be useful in the future.  

For the `window` class, both `copy constructor` and `copy assignment operator`
have been `delete`'d as to avoid multiple ownership of the window pointer.
The `move assignment operator` swaps the window pointers of each object in order
to ensure proper deletion of the pointer, and the `move constructor` uses
copies the pointer over and sets the old window pointer to `nullpte`.  
The `destructor` only operates on a non-`nullptr`, first clearing the window
before calling `delwin`.  

I have also written an member function to enable casting from my class to the
underlying `WINDOW *` for drop-in use in ncurses functions. Again, this is
probably unnecessary and for such a simple data structure I could have probably
managed the pointer manually.

## destruction order
In addition to the `WINDOW *` wrapper, a second class is required to ensure
`endwin` is only called **after** all the `window` destructors have been
executed.  
This works as the destructor for each object is called (as the leave scope) in
the reverse order than that in which they were created. As long as the main
ncurses wrapper is constructed before any of the windows (which is will be as it
is also responsible for calling `initscr`) then it will also be the last to be
destructed.
