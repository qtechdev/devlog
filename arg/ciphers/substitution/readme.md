# substitution ciphers
These are the most basic method of encoding a message, but they are not
necessarily easy to crack.

## Ceasar Shift
Each letter of the alphabet as shifted by a set number. This can be extended to
include numbers and symbols. The ciphertext is decoded by reversing the shift.

- [caesar shift example](caesar.md)
- [caesar shift code][caesar code]

### Running Key
The caesar shift can be improved by changing the shift value for each letter by
way of a keyword.

[running key example](running.md)

### Auto Key
The caesar shift can be improved by changing the shift value for each letter by
way of a keyword.

[auto key example](auto.md)

### OTP
Further improvements can be made, making the cipher uncrackable without the key.

[one time pad examples](otp.md)

### Enigma Machine
The enigma machine was created to make encoding and decoding messages like this
easier. Each letter was paired with another and by selecting one letter via the
input, the other leter in the pair was displayed on the output. After each
letter, the key pairs were automatically changed.  
By selecting the correct initial conditions, the state of the machine was
advanced with each letter such that a machine with the same initial conditions
would be able to decode the message with the same process.

This was theoretically uncrackable, however, the enigma machine had one fatal
flaw in its encription algorithm.

<!-- [enigma machine info](enigma.md) -->

## Masonic Cipher
The substitutions do not have to be letters, they can be symbols or glyphs as
is the case with the masonic cipher.

[masonic cipher example](masonic.md)


[caesar code]: <https://github.com/qtechdev/qcipher.caesar>
