## Descripción 

Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/24/convertme.py)

## Solución 
```
Jose323-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/24/convertme.py
--2026-02-16 14:21:31--  https://artifacts.picoctf.net/c/24/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.43, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py.2'

convertme.py.2       100%[===================>]   1.16K  --.-KB/s    in 0s      

2026-02-16 14:21:31 (314 MB/s) - 'convertme.py.2' saved [1189/1189]

Jose323-picoctf@webshell:~$ ls
Addadshashanammu      big-zip-files.zip.1  convertme.py.2  flag        static
Addadshashanammu.zip  code.py              enc_flag        flag.1      strings
README.txt            codebook.txt         enc_flag.1      ltdis.sh    warm
big-zip-files         convertme.py         files           runme.py
big-zip-files.zip     convertme.py.1       files.zip       salida.txt
Jose323-picoctf@webshell:~$ python3 convertme.py
If 61 is in decimal base, what is it in binary base?
Answer: 111101
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_722f6b39}
Jose323-picoctf@webshell:~$ 

```