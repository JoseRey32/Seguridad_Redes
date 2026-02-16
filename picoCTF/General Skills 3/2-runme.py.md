## Descripción 

Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell.[Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)

## Solución 
```
Jose323-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/34/runme.py
--2026-02-16 14:07:19--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.92, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: 'runme.py'

runme.py             100%[===================>]     270  --.-KB/s    in 0s      

2026-02-16 14:07:19 (10.8 MB/s) - 'runme.py' saved [270/270]

Jose323-picoctf@webshell:~$ ls
Addadshashanammu      big-zip-files.zip    files      ltdis.sh    strings
Addadshashanammu.zip  big-zip-files.zip.1  files.zip  runme.py    warm
README.txt            enc_flag             flag       salida.txt
big-zip-files         enc_flag.1           flag.1     static
Jose323-picoctf@webshell:~$ python3 runme.py
picoCTF{run_s4n1ty_run}
Jose323-picoctf@webshell:~$ 


```