# Masonic Cipher
Each letter is represented by a cell from the following:
```
 A │ B │ C         J │ K │ L
   │   │            .│ . │.
───┼───┼───       ───┼───┼───
 D │ E │ F         M │ N │ O
   │   │            .│ . │.
───┼───┼───       ───┼───┼───
   │   │            .│ . │.
 G │ H │ I         P │ Q │ R


   S          W
  ╲ ╱        ╲.╱
T  ╳  U    X .╳. Y
  ╱ ╲        ╱.╲
   V          Z  
```

A given message can be encoded like this:
```
PLAIN TEXT  : Hello, World!

              ┌─┐┌─┐|  |  ┌──      ┌──┌──|  ──┐
CIPHER TEXT : │ │| ||. |. |.    ╲.╱|. |. |.   |
              │ │└─┘└──└──└──    ╳ └──|  └──  |
```

This cipher does not work well with computer text. Images or hand written cipher
text works best.
