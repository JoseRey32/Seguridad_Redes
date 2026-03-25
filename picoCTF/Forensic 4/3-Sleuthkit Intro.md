#### Description

Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.[Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)Access checker program: `nc saturn.picoctf.net 62529`

## Solución
```
                                                                                                                                                          
┌──(kali㉿kali)-[~/picoctf/forensic/disk]
└─$ ..
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic]
└─$ mkdir SleuthkitIntro 
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic]
└─$ cd SleuthkitIntro 
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/SleuthkitIntro]
└─$ wget https://artifacts.picoctf.net/c/164/disk.img.gz
--2026-03-24 23:09:01--  https://artifacts.picoctf.net/c/164/disk.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.32.179.119, 13.32.179.34, 13.32.179.63, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.32.179.119|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29714372 (28M) [application/octet-stream]
Saving to: ‘disk.img.gz’

disk.img.gz                            100%[===========================================================================>]  28.34M  8.04MB/s    in 3.7s    

2026-03-24 23:09:05 (7.68 MB/s) - ‘disk.img.gz’ saved [29714372/29714372]

                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/SleuthkitIntro]
└─$ file disk.img.gz 
disk.img.gz: gzip compressed data, was "disk.img", last modified: Tue Sep 21 19:34:53 2021, from Unix, original size modulo 2^32 104857600
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/SleuthkitIntro]
└─$ gzip -d disk.img.gz            
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/SleuthkitIntro]
└─$ ls -la              
total 102408
drwxrwxr-x  2 kali kali      4096 Mar 24 23:12 .
drwxrwxr-x 11 kali kali      4096 Mar 24 23:08 ..
-rw-rw-r--  1 kali kali 104857600 Aug  4  2023 disk.img
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/SleuthkitIntro]
└─$ mmls -v             
Missing image name
usage: mmls [-i imgtype] [-b dev_sector_size] [-o imgoffset] [-BrvV] [-aAmM] [-t vstype] image [images]
        -t vstype: The type of volume system (use '-t list' for list of supported types)
        -i imgtype: The format of the image file (use '-i list' for list supported types)
        -b dev_sector_size: The size (in bytes) of the device sectors
        -o imgoffset: Offset to the start of the volume that contains the partition system (in sectors)
        -B: print the rounded length in bytes
        -r: recurse and look for other partition tables in partitions (DOS Only)
        -v: verbose output
        -V: print the version
Unless any of these are specified, all volume types are shown
        -a: Show allocated volumes
        -A: Show unallocated volumes
        -m: Show metadata volumes
        -M: Hide metadata volumes
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/SleuthkitIntro]
└─$ mmls disk.img    
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/SleuthkitIntro]
└─$  nc saturn.picoctf.net 62529
What is the size of the Linux partition in the given disk image?
Length in sectors: 202752
202752
Great work!
picoCTF{mm15_f7w!}
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/SleuthkitIntro]
└─$ 

```