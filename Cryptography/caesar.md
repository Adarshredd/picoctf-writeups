download and open the ciphertext<br>

`picoCTF{ynkooejcpdanqxeykjrbdofgkq}`

the encrypted message is `ynkooejcpdanqxeykjrbdofgkq`

let's try decrypt it with cyberchef<br>
first I'll try rearranging the order of the data using `ROT`

![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/4e39e666-55e4-437e-997e-9b8728fc43f5)

I started with `ROT 13` and kept increasing the no. of rotations till I got some meaning full<br>

at ROT30 
![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/caa123ec-e3fd-43e6-baae-c9628d899e26)
the out put is`crossingtherubiconvfhsjkou`

let's wrap it as a flag
and...

`picoCTF{crossingtherubiconvfhsjkou}`
