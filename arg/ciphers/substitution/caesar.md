# Caesar Shift
Given a shift of 3, the message can be encoded as such:

```
Encoding (shift 3)
------------------

IN  : ABCDEFGHIJKLMNOPQRSTUVWXYZ
OUT : DEFGHIJKLMNOPQRSTUVWXYZABC

PLAIN TEXT  : Hello, World!
CIPHER TEXT : Khoor, Zruog!
```

To decode the message, simple reverse the shift direction:

```
Decoding (unshift 3)
--------------------

IN  : ABCDEFGHIJKLMNOPQRSTUVWXYZ
OUT : XYZABCDEFGHIJKLMNOPQRSTUVW

CIPHER TEXT : Khoor, Zruog!
PLAIN TEXT  : Hello, World!

```

## ROT13
A shift value of 13 will result in the encode/decode functions being the same.
This is also known as ROT13.

```
Encode/Decode (shift 13)
------------------------

IN  : ABCDEFGHIJKLMNOPQRSTUVWXYZ
OUT : NOPQRSTUVWXYZABCDEFGHIJKLM

PLAIN TEXT  : Hello, World!
CIPHER TEXT : Uryyb, Jbeyq!
```

## extending the cipher
The cipher can be extended to include numbers or symbols:
```
Encoding (shift 3)
------------------

IN  : ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789
OUT : DEFGHIJKLMNOPQRSTUVWXYZ0123456789ABC

PLAIN TEXT  : Hello, World! 69420
CIHPER TEXT : Khoor, Zroug! 9C753

```

Each character set could have a seperate shift:

```
Encoding (shift 3, 5)
------------------

IN  : ABCDEFGHIJKLMNOPQRSTUVWXYZ 1234567890
OUT : DEFGHIJKLMNOPQRSTUVWXYZABC 6789012345

PLAIN TEXT  : Hello, World! 69420
CIPHER TEXT : Khoor, Zruog! 14975
```

## Flaws
- Trivial to brute force; It is extremely unlikely that more than one shift value
will result in a legitimate plain text.
