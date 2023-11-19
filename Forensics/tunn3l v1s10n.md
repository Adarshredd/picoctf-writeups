## Description
We found this file. Recover the flag.
## Approach
I tried opening the file<br>
![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/5ade9b4b-8e1c-426c-897f-fd5711711467)

so I tried opening it on websites but it didn't <br>

then I tried the terminal<br>
![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/504e1e24-9b22-4ed2-ae3d-da00e5d470a6)

![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/cc6fa1e3-dd11-40fd-9fae-10cc198ebbf6)

didn't get anything

let's try saving it as a Bitmap file<br>
![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/1af90f5a-00b5-41a8-b486-32707043f757)



so looked to open the file in an hex editor<br>

![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/676f80a5-7e49-4e39-b41d-b4c92f224ef8)

at 0A and 0E the value shows `BAD` instaed of starting address and size of header<br>
![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/65ab8743-502d-4614-80b8-94a31d93c6bc)

![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/329c8ee4-7f9e-4c16-b40e-72b45d1706dc)

lets change 0A to 36 00 from ba d0 as 40+14=54<br>
hex of 54 is 36<br>
and change 0E to 38  (hex of 56)  and save the file to open it<br>

![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/6a1f295f-865f-43d4-a330-ddddd3c9b711)

the text is not flag <br>
looks like the image is not displayed comletely, so may increase the height and width of the image<br>
![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/15c48865-ac72-409b-a82d-06102cf5853c)

increase the values in `16` to increase the height<br>
![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/686c4967-ee6d-4fe6-8a54-a018ca4c1162)

save it and open the image

![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/9791364a-d40c-4974-a401-ddd79a674070)

the flag: picoCTF{qu1t3_a_v13w_2020}
