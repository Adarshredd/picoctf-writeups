in this challenge we have to find the inverse mod for %41 of all the numbers in `message.txt`file<br>

so let's write a code for that instead of doing the calculations manually
```py
def invmod(num,mod):
    ans=0
    b=0
    while (ans!=1):
         b+=1
         ans = (num*b)%mod

    return b

file = open("message.txt","r") 
numbers = file.read().split(" ")
characters = " ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789_"
output = "picoCTF{"
for number in numbers:
    if number=="":
        continue
    i=invmod(int(number)%41,41)
    output = output+characters[i]
output=output+"}"
print(output)
````
run the program in the same directory as the `message.txt`file
```py
PS C:\Users\Adarsh\Desktop> python -u "c:\Users\Adarsh\Desktop\MOD1 DECODE .py"
picoCTF{1NV3R53LY_H4RD_8A05D939}
PS C:\Users\Adarsh\Desktop>
```
the flag is `picoCTF{1NV3R53LY_H4RD_8A05D939}`
