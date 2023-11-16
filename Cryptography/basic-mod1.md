open the message.txt file
```c
165 248 94 346 299 73 198 221 313 137 205 87 336 110 186 69 223 213 216 216 177 138
```
we have to mod37 all the numbers individually and map it with<br>
`A B C D E F G H I J K L M N O P Q R S T U V W X Y Z 0 1 2 3 4 5 6 7 8 9 _`
first I did %37 to all the numbers seperately and got the values<br>

```p
165 248 94 346 299 73 198 221 313 137 205 87 336 110 186 69 223 213 216 216 177 138 
17  26  20 13  3   36  13 36  17  26  20  13  3  36  1   32  1  28  31  31  29  27
```
then mapped them<br>

but this meathod is not efficient so i decided to write a code for it<br>
```py
file = open("message.txt","r")
numbers = file.read().split(" ")
characters = "ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789_"
output = "picoCTF{"
for number in numbers:
    i=int(number)%37
    output = output+characters[i]
output=output+"}"
print(output)
```
now run the code in the same directory as the `message.txt` file

```
PS C:\Users\Adarsh> cd Desktop
PS C:\Users\Adarsh\Desktop> python -u "c:\Users\Adarsh\Desktop\MOD1 DECODE .py"
picoCTF{R0UND_N_R0UND_B6B25531}
PS C:\Users\Adarsh\Desktop> 
```

the flag is `picoCTF{R0UND_N_R0UND_B6B25531}`
