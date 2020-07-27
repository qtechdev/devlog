# Autokey Cipher
An extension of the running key cipher which appends the plain text message to
the keyword.

This removes the weakness that a repeating keyword introduces, but adds in its
own flaw.

## Flaws
- Since the keyword contains the plain text, it will likely contain commonly
used words. This can be used to partially decode the cipher text. By selecting
the most promising results, more of the keyword can be deduced. This can result
in cracking the cipher.
