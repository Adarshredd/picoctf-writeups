## Description
Figure out how they moved the flag.
## Approach
download Wireshark and open the file
![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/262ec026-ffc4-40e7-9fa8-09cc15c7ae5f)

![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/ff234b83-8d23-4fef-b3f6-595f9a8f659f)

save all the files<br>
open instructions,
use rot 13
![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/bb6867b5-2c41-480d-b2e5-657e9c43f245)

`TFTP DOES NT ENCRYPT OUR TRAFFIC SO WE MUST DISGUISE OUR FLAG TRANSFER. FIGURE OUT AWAY TO HIDE THE FLAG AND I WILL CHECK BACK FOR THE PLAN`

use ROT13 on `plan`
`VHFRQGURCEBTENZNAQUVQVGJVGU-QHRQVYVTRAPR.PURPXBHGGURCUBGBF`=>"IUSEDTHEPROGRAMANDHIDITWITH-DUEDILIGENCE.CHECKOUTTHEPHOTOS"

it says
`I USED THE PROGRAM AND HID IT WITH-DUE DILIGENCE. CHECK OUT THE PHOTOS`

I extracted `program.deb` and went through it to find out that it is "steghide"<br>
use `sudo apt install steghide` to install it <br>
then `steghide extract -sf picture3.bmp `<br>
enter the phrase `DUEDILIGENCE`<br>

```py
wrote extracted data to "flag.txt".
```

![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/6777de50-4609-4317-9076-f66ce4876d62)

flag: `picoCTF{h1dd3n_1n_pLa1n_51GHT_18375919}`
