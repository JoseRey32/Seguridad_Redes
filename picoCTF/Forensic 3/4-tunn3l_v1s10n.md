## Descripción

We found this file. Recover the flag.[tunn3l_v1s10n](https://challenge-files.picoctf.net/c_wily_courier/626df9feed926c1e1280804f5d87fde5576e266ff250a819a5528b0471b0f3f7/tunn3l_v1s10n)
## Solucion 
```
┌──(kali㉿kali)-[~]
└─$ cd picoctf                                                                                                                            
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf]
└─$ cd forensic                                                                                                                           
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic]
└─$ cd tunn3l_v1s10n                                                                                                                      
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/tunn3l_v1s10n]
└─$ open tunn3l_v1s10n.bnp

                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/tunn3l_v1s10n]
└─$ exiftool tunn3l_v1s10n.bmp
ExifTool Version Number         : 13.36
File Name                       : tunn3l_v1s10n.bmp
Directory                       : .
File Size                       : 2.9 MB
File Modification Date/Time     : 2026:03:22 17:20:44-04:00
File Access Date/Time           : 2026:03:22 17:20:50-04:00
File Inode Change Date/Time     : 2026:03:22 17:20:44-04:00
File Permissions                : -rw-rw-r--
File Type                       : BMP
File Type Extension             : bmp
MIME Type                       : image/bmp
BMP Version                     : Windows V3
Image Width                     : 1134
Image Height                    : 306
Planes                          : 1
Bit Depth                       : 24
Compression                     : None
Image Length                    : 2893400
Pixels Per Meter X              : 5669
Pixels Per Meter Y              : 5669
Num Colors                      : Use BitDepth
Num Important Colors            : All
Image Size                      : 1134x306
Megapixels                      : 0.347
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/tunn3l_v1s10n]
└─$ exiftool tunn3l_v1s10n.bmp
ExifTool Version Number         : 13.36
File Name                       : tunn3l_v1s10n.bmp
Directory                       : .
File Size                       : 2.9 MB
File Modification Date/Time     : 2026:03:22 17:20:44-04:00
File Access Date/Time           : 2026:03:22 17:20:50-04:00
File Inode Change Date/Time     : 2026:03:22 17:20:44-04:00
File Permissions                : -rw-rw-r--
File Type                       : BMP
File Type Extension             : bmp
MIME Type                       : image/bmp
BMP Version                     : Windows V3
Image Width                     : 1134
Image Height                    : 306
Planes                          : 1
Bit Depth                       : 24
Compression                     : None
Image Length                    : 2893400
Pixels Per Meter X              : 5669
Pixels Per Meter Y              : 5669
Num Colors                      : Use BitDepth
Num Important Colors            : All
Image Size                      : 1134x306
Megapixels                      : 0.347
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/tunn3l_v1s10n]
└─$ hexeditor tunn3l_v1s10n.bmp
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/tunn3l_v1s10n]
└─$ open tunn3l_v1s10n.bnp    

                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/tunn3l_v1s10n]
└─$ exiftool tunn3l_v1s10n.bmp 
ExifTool Version Number         : 13.36
File Name                       : tunn3l_v1s10n.bmp
Directory                       : .
File Size                       : 2.9 MB
File Modification Date/Time     : 2026:03:22 17:28:06-04:00
File Access Date/Time           : 2026:03:22 17:28:06-04:00
File Inode Change Date/Time     : 2026:03:22 17:28:06-04:00
File Permissions                : -rw-rw-r--
File Type                       : BMP
File Type Extension             : bmp
MIME Type                       : image/bmp
BMP Version                     : Windows V3
Image Width                     : 1134
Image Height                    : 320
Planes                          : 1
Bit Depth                       : 24
Compression                     : None
Image Length                    : 2893400
Pixels Per Meter X              : 5669
Pixels Per Meter Y              : 5669
Num Colors                      : Use BitDepth
Num Important Colors            : All
Image Size                      : 1134x320
Megapixels                      : 0.363
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/tunn3l_v1s10n]
└─$ hexeditor tunn3l_v1s10n.bmp
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/tunn3l_v1s10n]
└─$ exiftool tunn3l_v1s10n.bmp 
ExifTool Version Number         : 13.36
File Name                       : tunn3l_v1s10n.bmp
Directory                       : .
File Size                       : 2.9 MB
File Modification Date/Time     : 2026:03:22 17:30:11-04:00
File Access Date/Time           : 2026:03:22 17:28:06-04:00
File Inode Change Date/Time     : 2026:03:22 17:30:11-04:00
File Permissions                : -rw-rw-r--
File Type                       : BMP
File Type Extension             : bmp
MIME Type                       : image/bmp
BMP Version                     : Windows V3
Image Width                     : 1134
Image Height                    : 1088
Planes                          : 1
Bit Depth                       : 24
Compression                     : None
Image Length                    : 2893400
Pixels Per Meter X              : 5669
Pixels Per Meter Y              : 5669
Num Colors                      : Use BitDepth
Num Important Colors            : All
Image Size                      : 1134x1088
Megapixels                      : 1.2
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/tunn3l_v1s10n]
└─$ open tunn3l_v1s10n.bnp    

```
![[Pasted image 20260322153557.png]]
picoCTF{qu1t3_a_v13w_2020}