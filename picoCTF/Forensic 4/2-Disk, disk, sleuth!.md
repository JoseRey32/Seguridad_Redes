## Descripción

Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image.[dds1-alpine.flag.img.gz](https://challenge-files.picoctf.net/c_wily_courier/a118330a1c5e12f3b59fc45a75b8838700482f89c8ea71a28aa1bd66c7ba3968/dds1-alpine.flag.img.gz)

## Solución 
```
┌──(kali㉿kali)-[~]
└─$ cd picoctf                    
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf]
└─$ cd forensic
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic]
└─$ mkdir disk                                                                                                                                       
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic]
└─$ cd disk     
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/disk]
└─$ wget https://challenge-files.picoctf.net/c_wily_courier/a118330a1c5e12f3b59fc45a75b8838700482f89c8ea71a28aa1bd66c7ba3968/dds1-alpine.flag.img.gz
--2026-03-24 22:59:06--  https://challenge-files.picoctf.net/c_wily_courier/a118330a1c5e12f3b59fc45a75b8838700482f89c8ea71a28aa1bd66c7ba3968/dds1-alpine.flag.img.gz
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.161.44.22, 3.161.44.103, 3.161.44.84, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.161.44.22|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29768911 (28M) [application/octet-stream]
Saving to: ‘dds1-alpine.flag.img.gz’

dds1-alpine.flag.img.gz                100%[===========================================================================>]  28.39M  8.63MB/s    in 3.4s    

2026-03-24 22:59:10 (8.26 MB/s) - ‘dds1-alpine.flag.img.gz’ saved [29768911/29768911]

                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/disk]
└─$ ls                  
dds1-alpine.flag.img.gz
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/disk]
└─$ gzip -d dds1-alpine.flag.img.gz

                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/disk]
└─$ srch_strings dds1-alpine.flag.img.gz | grep "pico"

'dds1-alpine.flag.img.gz': No such file
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/disk]
└─$ srch_strings dds1-alpine.flag.img. | grep "pico" 

'dds1-alpine.flag.img.': No such file
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/disk]
└─$ srch_strings dds1-alpine.flag.img | grep "pico" 

ffffffff81399ccf t pirq_pico_get
ffffffff81399cee t pirq_pico_set
ffffffff820adb46 t pico_router_probe
  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_5e56e786}

```