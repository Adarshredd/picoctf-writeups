download and open the file

```p
bezos_cc_secret = "A:4@r%uL`M-^M0c0AbcM-MFE02fh3e4a5N"

# Reference alphabet
alphabet = "!\"#$%&'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ"+ \
            "[\\]^_`abcdefghijklmnopqrstuvwxyz{|}~"



def decode_secret(secret):
    """ROT47 decode

    NOTE: encode and decode are the same operation in the ROT cipher family.
    """
```

`bezos_cc_secret` is not called any where, so let's try

```p
decode_secret(bezos_cc_secret)
```

![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/16df2499-82c8-4aec-8891-8dbd671c3d5f)

and we get the flag

`picoCTF{1|\/|_4_p34|\|ut_a79b6c2d}`
