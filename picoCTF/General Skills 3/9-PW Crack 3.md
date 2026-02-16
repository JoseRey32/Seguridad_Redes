## Descripción 

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/18/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

## solución 
```
Jose323-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/18/level3.py
--2026-02-16 14:56:58--  https://artifacts.picoctf.net/c/18/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.128, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: 'level3.py'

level3.py            100%[===================>]   1.31K  --.-KB/s    in 0s      

2026-02-16 14:56:58 (805 MB/s) - 'level3.py' saved [1337/1337]

Jose323-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/18/level3.flag.txt.enc
--2026-02-16 14:57:17--  https://artifacts.picoctf.net/c/18/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.128, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level3.flag.txt.enc'

level3.flag.txt.enc  100%[===================>]      31  --.-KB/s    in 0s      

2026-02-16 14:57:17 (12.2 MB/s) - 'level3.flag.txt.enc' saved [31/31]

Jose323-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/18/level3.hash.bin
--2026-02-16 14:57:37--  https://artifacts.picoctf.net/c/18/level3.hash.bin
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.92, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16 [application/octet-stream]
Saving to: 'level3.hash.bin'

level3.hash.bin      100%[===================>]      16  --.-KB/s    in 0s      

2026-02-16 14:57:37 (12.9 MB/s) - 'level3.hash.bin' saved [16/16]

Jose323-picoctf@webshell:~$ ls
Addadshashanammu  files                level1.py            level3.flag.txt.enc
README.txt        fixme2.py            level2.flag.txt.enc  level3.hash.bin
big-zip-files     level1.flag.txt.enc  level2.py            level3.py
Jose323-picoctf@webshell:~$ cat level3.py
import hashlib

### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################

flag_enc = open('level3.flag.txt.enc', 'rb').read()
correct_pw_hash = open('level3.hash.bin', 'rb').read()


def hash_pw(pw_str):
    pw_bytes = bytearray()
    pw_bytes.extend(pw_str.encode())
    m = hashlib.md5()
    m.update(pw_bytes)
    return m.digest()


def level_3_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    user_pw_hash = hash_pw(user_pw)
    
    if( user_pw_hash == correct_pw_hash ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_3_pw_check()


# The strings below are 7 possibilities for the correct password. 
#   (Only 1 is correct)
pos_pw_list = ["8799", "d3ab", "1ea2", "acaf", "2295", "a9de", "6f3d"]

Jose323-picoctf@webshell:~$ 
Jose323-picoctf@webshell:~$ Jose323-picoctf@webshell:~$ 
-bash: Jose323-picoctf@webshell:~$: command not found
Jose323-picoctf@webshell:~$ 
Jose323-picoctf@webshell:~$ Jose323-picoctf@webshell:~$ 8799
-bash: Jose323-picoctf@webshell:~$: command not found
Jose323-picoctf@webshell:~$ d3ab
-bash: d3ab: command not found
Jose323-picoctf@webshell:~$ python3 level3.py
Please enter correct password for flag: 8799
That password is incorrect
Jose323-picoctf@webshell:~$ python3 level3.py
Please enter correct password for flag: d3ab
That password is incorrect
Jose323-picoctf@webshell:~$ python3 - << 'EOF'
> import hashlib
> 
> correct_hash = open('level3.hash.bin','rb').read()
> 
> pos_pw_list = ["8799", "d3ab", "1ea2", "acaf", "2295", "a9de", "6f3d"]
> 
> for pw in pos_pw_list:
>     if hashlib.md5(pw.encode()).digest() == correct_hash:
>         print("Password correcta:", pw)
> EOF
Password correcta: 2295
Jose323-picoctf@webshell:~$ python3 level3.py
Please enter correct password for flag: 2295
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_6f98a49f}
Jose323-picoctf@webshell:~$ 
```