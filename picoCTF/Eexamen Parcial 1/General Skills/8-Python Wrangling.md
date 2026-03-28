## Descripción

Python scripts are invoked kind of like programs in the Terminal...Can you run [ende.py](https://challenge-files.picoctf.net/c_wily_courier/2946b2b767f2d6792cb13dcfc9312c0fd5888dcabaf4196f2d88ae6d46f2a62c/ende.py) using [password.txt](https://challenge-files.picoctf.net/c_wily_courier/2946b2b767f2d6792cb13dcfc9312c0fd5888dcabaf4196f2d88ae6d46f2a62c/password.txt) to get [flag.txt.en](https://challenge-files.picoctf.net/c_wily_courier/2946b2b767f2d6792cb13dcfc9312c0fd5888dcabaf4196f2d88ae6d46f2a62c/flag.txt.en)?}

## Solución 
```
──(kali㉿kali)-[~]
└─$ mkdir PythonWrangling 
                                                                                                                                                           
┌──(kali㉿kali)-[~]
└─$ cd PythonWrangling 
                                                                                                                                                           
┌──(kali㉿kali)-[~/PythonWrangling]
└─$ wget https://challenge-files.picoctf.net/c_wily_courier/2946b2b767f2d6792cb13dcfc9312c0fd5888dcabaf4196f2d88ae6d46f2a62c/ende.py      
--2026-03-26 12:12:43--  https://challenge-files.picoctf.net/c_wily_courier/2946b2b767f2d6792cb13dcfc9312c0fd5888dcabaf4196f2d88ae6d46f2a62c/ende.py
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 54.192.100.111, 54.192.100.5, 54.192.100.76, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|54.192.100.111|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1328 (1.3K) [application/octet-stream]
Saving to: ‘ende.py’

ende.py                                100%[===========================================================================>]   1.30K  --.-KB/s    in 0.002s  

2026-03-26 12:12:45 (581 KB/s) - ‘ende.py’ saved [1328/1328]

                                                                                                                                                           
┌──(kali㉿kali)-[~/PythonWrangling]
└─$ wget https://challenge-files.picoctf.net/c_wily_courier/2946b2b767f2d6792cb13dcfc9312c0fd5888dcabaf4196f2d88ae6d46f2a62c/password.txt
--2026-03-26 12:13:02--  https://challenge-files.picoctf.net/c_wily_courier/2946b2b767f2d6792cb13dcfc9312c0fd5888dcabaf4196f2d88ae6d46f2a62c/password.txt
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 18.154.206.118, 18.154.206.14, 18.154.206.121, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|18.154.206.118|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 33 [application/octet-stream]
Saving to: ‘password.txt’

password.txt                           100%[===========================================================================>]      33  --.-KB/s    in 0s      

2026-03-26 12:13:04 (23.4 MB/s) - ‘password.txt’ saved [33/33]

                                                                                                                                                           
┌──(kali㉿kali)-[~/PythonWrangling]
└─$ wget https://challenge-files.picoctf.net/c_wily_courier/2946b2b767f2d6792cb13dcfc9312c0fd5888dcabaf4196f2d88ae6d46f2a62c/flag.txt.en 
--2026-03-26 12:13:21--  https://challenge-files.picoctf.net/c_wily_courier/2946b2b767f2d6792cb13dcfc9312c0fd5888dcabaf4196f2d88ae6d46f2a62c/flag.txt.en
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 99.84.118.18, 99.84.118.37, 99.84.118.46, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|99.84.118.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 140 [application/octet-stream]
Saving to: ‘flag.txt.en’

flag.txt.en                            100%[===========================================================================>]     140  --.-KB/s    in 0s      

2026-03-26 12:13:22 (103 MB/s) - ‘flag.txt.en’ saved [140/140]

                                                                                                                                                           
┌──(kali㉿kali)-[~/PythonWrangling]
└─$ ls
ende.py  flag.txt.en  password.txt
                                                                                                                                                           
┌──(kali㉿kali)-[~/PythonWrangling]
└─$ chmod +x ende.py  
                                                                                                                                                           
┌──(kali㉿kali)-[~/PythonWrangling]
└─$ ls
ende.py  flag.txt.en  password.txt
                                                                                                                                                           
┌──(kali㉿kali)-[~/PythonWrangling]
└─$ python ende.py 
Usage: ende.py (-e/-d) [file]
                                                                                                                                                           
┌──(kali㉿kali)-[~/PythonWrangling]
└─$ python ende.py -h
Usage: ende.py (-e/-d) [file]
Examples:
  To decrypt a file named 'pole.txt', do: '$ python ende.py -d pole.txt'

                                                                                                                                                           
┌──(kali㉿kali)-[~/PythonWrangling]
└─$ cat pw.txt      
cat: pw.txt: No such file or directory
                                                                                                                                                           
┌──(kali㉿kali)-[~/PythonWrangling]
└─$ ls        
ende.py  flag.txt.en  password.txt
                                                                                                                                                           
┌──(kali㉿kali)-[~/PythonWrangling]
└─$ mkdir pw             
                                                                                                                                                           
┌──(kali㉿kali)-[~/PythonWrangling]
└─$ cat password.txt
720b6ad346f84cd483c60c7464dd95d4
                                                                                                                                                           
┌──(kali㉿kali)-[~/PythonWrangling]
└─$ python ende.py -d flag.txt.en
Please enter the password:720b6ad346f84cd483c60c7464dd95d4
picoCTF{4p0110_1n_7h3_h0us3_9c5f9bcf}

```