# submodules

`git submodule` allows for a nested git repository.

A reference to the module repo ([module_greeter][module]) is placed inside the
main repo ([testing_modules][testing]) at a given path (`modules/greeter`).

Cloning the repo via `git clone` will not clone the submodule also. The
`--recursive` flag must also be specified. Submodules can be cloned mannually
via `git submodule init` and `git submodule update`.

A submodule is included at a specific commit. Submodules can be updated with
`git submodule update` or via `git pull --recurse-submodules`, however their
`HEAD` will remain on the same commit.  
To change the commit pointed to, the user must:
- update each submodule repository
- call `git submodule sync` from the main repo
- add the new files and commit the changes

## pros
- easy and convenient to source dependencies
- specific commits are referenced, allowing easier version compatability control

## cons
- changing the submodule version requires a commit in the main project
- each project using the submodule will have its own instance, requiring
network resources and disk space (arguably insignificant)

## final word
I don't think submodules are the best approach at the moment, but I may
reconsider in the future.

[testing]: <https://github.com/qtechdev/testing_modules>
[module]: <https://github.com/qtechdev/module_greeter>
