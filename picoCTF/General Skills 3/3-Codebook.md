## Descripción 

Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/2/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/2/codebook.txt)

## Solución 
```
Jose323-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/2/code.py
--2026-02-16 14:11:29--  https://artifacts.picoctf.net/c/2/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.92, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py'

code.py              100%[===================>]   1.25K  --.-KB/s    in 0s      

2026-02-16 14:11:29 (648 MB/s) - 'code.py' saved [1278/1278]

Jose323-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/2/codebook.txt
--2026-02-16 14:11:38--  https://artifacts.picoctf.net/c/2/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.43, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt         100%[===================>]      27  --.-KB/s    in 0s      

2026-02-16 14:11:38 (20.1 MB/s) - 'codebook.txt' saved [27/27]

Jose323-picoctf@webshell:~$ ls
Addadshashanammu      big-zip-files.zip    enc_flag    flag      salida.txt
Addadshashanammu.zip  big-zip-files.zip.1  enc_flag.1  flag.1    static
README.txt            code.py              files       ltdis.sh  strings
big-zip-files         codebook.txt         files.zip   runme.py  warm
Jose323-picoctf@webshell:~$ python3 code.py
picoCTF{c0d3b00k_455157_7d102d7a}
Jose323-picoctf@webshell:~$ 
```