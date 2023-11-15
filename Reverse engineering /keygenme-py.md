open the file keygenme-trial.py

![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/1a63dfc9-3746-4be3-b99a-40b9b79f4bc3)

```py
key_part_static1_trial = "picoCTF{1n_7h3_|<3y_of_"
key_part_dynamic1_trial = "xxxxxxxx"
key_part_static2_trial = "}"
key_full_template_trial = key_part_static1_trial + key_part_dynamic1_trial + key_part_static2_trial
```

half the key is aready given<br>
the other half is of 8 digits<br>
every digit is a random hashed character of the given username_trial<br>
I figured out the order by reading the check_key function
the order is 4,5,3,6,2,7,1,8<br>
now we hash the digits of the username to determine the unknown part of the key

![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/89baf367-c4da-408f-8e6b-d759b2d651d4)


i did this in the check key function itself so i had to run the program and type a random string as license key

upon doing that, the code i injected gives the actual key

![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/d1372a41-6d9e-4b6f-8dfa-11e3cfd052db)

the flag is
`picoCTF{1n_7h3_|<3y_of_01582419}`
