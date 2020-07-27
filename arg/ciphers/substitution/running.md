# Running Key
A standard caesar shift applies the same shift value to each letter. This can
easily be cracked by simply checking each shift value as it is extremely
unlikely that more than one value will result in a legitimate plain text.

By varying the shift value of each letter by using a key, a basic encryption is
added to the message.

```
IN  : ABCDEFGHIJKLMNOPQRSTUVWXYZ
KEY : RUNNING

PLAIN TEXT  : Hello, World!

```

The shift value is obtained by using the key. The first shift aligns an input
of `A`  to the output of `R`.

```
IN  : ABCDEFGHIJKLMNOPQRSTUVWXYZ
OUT : RSTUVWXYZABCDEFGHIJKLMNOPQ

KEY : RUNNING
      ^

PLAIN TEXT  : Hello, World!
CIPHER TEXT : Y
```

The next shift value is obtained by the next letter in the key

```
IN  : ABCDEFGHIJKLMNOPQRSTUVWXYZ
OUT : UVWXYZABCDEFGHIJKLMNOPQRST

KEY : RUNNING
       ^

PLAIN TEXT  : Hello, World!
CIPHER TEXT : Yy
```

This continues for each letter.

```
IN  : ABCDEFGHIJKLMNOPQRSTUVWXYZ
OUT : GHIJKLMNOPQRSTUVWXYZABCDEF

KEY : RUNNING
            ^

PLAIN TEXT  : Hello, World!
CIPHER TEXT : Yyyyw, Ju
```

When the end of the key is reached, start at the beginning again.

```
IN  : ABCDEFGHIJKLMNOPQRSTUVWXYZ
OUT : RSTUVWXYZABCDEFGHIJKLMNOPQ

KEY : RUNNING
      ^

PLAIN TEXT  : Hello, World!
CIPHER TEXT : Yyyyw, Jui
```



```
IN  : ABCDEFGHIJKLMNOPQRSTUVWXYZ
OUT : NOPQRSTUVWXYZABCDEFGHIJKLM

KEY : RUNNING
        ^

PLAIN TEXT  : Hello, World!
CIPHER TEXT : Yyyyw, Juifq!
```

The cipher text will no longer be a direct one to one mapping, but will allow
multiple input letters to map to a single output letter, and a single input
letter to map to multiple output letters.

## Flaws
- There is a chance that if a word in the plain text is repeated that it may
align with the repitition of the keyword. This can be used to determine
possible lengths of the keyword. From there the cipher can be treated as
multiple caesar shifts interwoven with each other.
