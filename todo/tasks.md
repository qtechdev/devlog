# Tasks
## readmes
__(added: 2020-07-17, completed: ...)__

I should add readmes with a unified format:
- program name
- short description
- basic example
- dependencies

Progress
- ~qtechdev.github.io~
- cellular
- testing_modules
- module_greeter
- opengl
- qch_meta
- qchip
- qch_vm
- qch_asm
- qch_dis
- bmi
- qsi
- qfio
- qxdg
- weights

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
