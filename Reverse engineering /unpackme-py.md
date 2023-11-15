```py
import base64
from cryptography.fernet import Fernet



payload = b'gAAAAABkzWGO_8MlYpNM0n0o718LL-w9m3rzXvCMRFghMRl6CSZwRD5DJOvN_jc8TFHmHmfiI8HWSu49MyoYKvb5mOGm_Jn4kkhC5fuRiGgmwEpxjh0z72dpi6TaPO2TorksAd2bNLemfTaYPf9qiTn_z9mvCQYV9cFKK9m1SqCSr4qDwHXgkQpm7IJAmtEJqyVUfteFLszyxv5-KXJin5BWf9aDPIskp4AztjsBH1_q9e5FIwIq48H7AaHmR8bdvjcW_ZrvhAIOInm1oM-8DjamKvhh7u3-lA=='

key_str = 'correctstaplecorrectstaplecorrec'
key_base64 = base64.b64encode(key_str.encode())
f = Fernet(key_base64)
plain = f.decrypt(payload)
exec(plain.decode())
```

replace the `exec` function with `print` to know what's in the string

![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/18e7ff7f-0809-4dc1-85a0-4ecdfc7f901c)

when u run 
```py
print(plain.decode())
```
u get the flag in output

![image](https://github.com/Adarshredd/picoctf-writeups/assets/145366498/ce861b2e-0c78-4d48-9024-28177fe3c970)


`print('picoCTF{175_chr157m45_5274ff21}')`
