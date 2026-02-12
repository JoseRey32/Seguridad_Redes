## Descripción 

Can you find the flag in [file](https://challenge-files.picoctf.net/c_fickle_tempest/285538e2710605958a055500d6573657fcafea6308545cecfabb34462199cfd5/strings) without running it?
## solución 
```
Jose323-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_fickle_tempest/285538e2710605958a055500d6573657fcafea6308545cecfabb34462199cfd5/strings
--2026-02-12 02:59:52--  https://challenge-files.picoctf.net/c_fickle_tempest/285538e2710605958a055500d6573657fcafea6308545cecfabb34462199cfd5/strings
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.40, 3.160.5.18, 3.160.5.95, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 784424 (766K) [application/octet-stream]
Saving to: 'strings'

strings              100%[===================>] 766.04K  1.86MB/s    in 0.4s    

2026-02-12 02:59:53 (1.86 MB/s) - 'strings' saved [784424/784424]

Jose323-picoctf@webshell:~$ ls
README.txt  flag  flag.1  salida.txt  strings
Jose323-picoctf@webshell:~$ file warm
warm: cannot open `warm' (No such file or directory)
Jose323-picoctf@webshell:~$ file strings
strings: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=f4f3c992bb3f870f5b303cb391db44c8f665d4a9, for GNU/Linux 3.2.0, not stripped
Jose323-picoctf@webshell:~$ strings strings | grep pico
picoCTF{5tRIng5_1T_1067EC4c}
Jose323-picoctf@webshell:~$ 
```