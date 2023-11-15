open chall.s in terminal
 func|main
:-------------------------------------------------------------------------------------------------------------:|:--------------:
![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/8d229efa-671d-40b7-b398-864485abd5d4) | ![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/d2a858ad-2604-49ec-b3dd-a0fa539ca3ee) |

func 1 

stores the 1st parameter 12 from bottom stack and stores 2nd parameter 8 from bottom stack and loads them back in to compare them 

if w1 < or = w0  then we go to .L2 and we load sp-8

if w1 >   then we ld sp-12

so probably we want the bigger one 

and the bigger value gets to the main program
 -which says printf with result string 

 so maybe we are just printing the bigger value of
 4112417903 and 1169092511

so let's try 4112417903 

![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/0ec8c75d-8333-4b6c-9cbd-86bea86354da)

 so the flag should be 
"picoCTF{f51e846f}"
