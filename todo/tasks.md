# Tasks

## opengl faults
__(added: 2020-08-11, completed: ...)__
something appears to have gone wrong with all of my opengl programs, only getting a blue screen
could possibly be an issue with stb_image?

[Task progress table.](./task_table.md)

## library installs and versioning
__(added: 2020-08-23, completed: ...)__
The way the library install in makefiles are handle need to be updated.
The `soname` should include the major version of the library, and the bare symlink
should be created with `ln -s`, pointing to the freshly insatlled version.
I should also make sure to create a minimum viable product for the 1.0 release,
and update the version numbers properly.

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

## unit tests and performance analysis
__(added: 2020-07-17, completed: ...)__

Especially for libraries, but also for programs.

## libraries
__(added: 2020-07-17, completed: ...)__  

I have pulled some code out into libraries (fio, xdg, etc.), each repo should
be updated to use these libraries instead of bundling code?  
I might move the opengl code into a library instead of reusing it so often.  

*Making the code in these libraries as concise and efficient as possible should
be a goal.*

## cross platform code
__(added: 2020-07-17, completed: ...)__

I am currently only compiling and testing on Linux. Most of these programs
should compile for Windows (and Mac?) as is, others may require some changes?  

*This would require being able to test programs on these other platforms.*
