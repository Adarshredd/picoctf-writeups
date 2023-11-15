download the flag and program<br>
open the program, change the directory to Desktop(where flag is  located)<br>
now run the program
```py
Please enter correct password for flag:
```
 to get the password<br>
 ```py
import sys
a = "!\"#$%&'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ"+ \
            "[\\]^_`abcdefghijklmnopqrstuvwxyz{|}~ "
def arg133(arg432):
  if arg432 == a[71]+a[64]+a[79]+a[79]+a[88]+a[66]+a[71]+a[64]+a[77]+a[66]+a[68]:
    return True
  else:
```
if we type a random paswword the program compares it with the actual password in an order<br>
we know that 
```py
a = "!\"#$%&'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ"+ \
            "[\\]^_`abcdefghijklmnopqrstuvwxyz{|}~ "
```
and the order is given in the program itself<br> 
so let's just print it<br>
```py
print(a[71]+a[64]+a[79]+a[79]+a[88]+a[66]+a[71]+a[64]+a[77]+a[66]+a[68])
```
run the program then it'll print the password
```py
PS C:\Users\Adarsh\Desktop> python -u "c:\Users\Adarsh\Desktop\bloat.flag.py"
happychance
Please enter correct password for flag:
```
now just type the password to  get the flag

![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/dda8dc69-29db-4cee-9747-69f9b1200a9f)

`picoCTF{d30bfu5c4710n_f7w_b8062eec}`
