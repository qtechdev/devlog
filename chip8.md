# chip8
Chip8 is an programming language that is interpreted by a virtual machine.
Originally written for a home computer in the '70s, there have been many ports
to a variety of different systems.

The virtual machine that I have written (`qch_vm`) is based on the instruction
set at [wikipedia](https://en.wikipedia.org/wiki/CHIP-8).

## virtual machine (qch_vm)
The virtual machine consists of several registers and memory blocks.
For each clock cycle an instruction is pulled from the relevant memory location
and then converted into a function pointer via a lookup table.

## libraries (qch_vm)
All of the common functions and data are bundled into a seperate header that
can be referenced without including the entire virtual machine implementation.

## finite state machines (qch_asm)
The assembly files are parsed into tokens via several finite stame machines.

## software rendering (qchip)
The graphics data is taken from the virtual machine and converted into an
opengl texture that is displayed full size.
