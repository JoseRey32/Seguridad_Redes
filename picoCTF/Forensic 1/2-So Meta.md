## Descripción

Find the flag in this [picture](https://challenge-files.picoctf.net/c_fickle_tempest/739119ebf098a2424ccce7d9e08e1af162dab0dc358950a6047750e37ec2bf2b/pico_img.png).
## Solución 
```
┌──(kali㉿kali)-[~]
└─$ cd pico            
cd: no such file or directory: pico
                                                                                                                                                           
┌──(kali㉿kali)-[~]
└─$ cd picoCTF                                                                                                                           
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoCTF]
└─$ cd forensic                                                                                                                          
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoCTF/forensic]
└─$ mkdir someta         
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoCTF/forensic]
└─$ cd someta   
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoCTF/forensic/someta]
└─$ wget https://challenge-files.picoctf.net/c_fickle_tempest/739119ebf098a2424ccce7d9e08e1af162dab0dc358950a6047750e37ec2bf2b/pico_img.png
--2026-03-09 23:42:10--  https://challenge-files.picoctf.net/c_fickle_tempest/739119ebf098a2424ccce7d9e08e1af162dab0dc358950a6047750e37ec2bf2b/pico_img.png
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.161.44.61, 3.161.44.103, 3.161.44.84, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.161.44.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 108795 (106K) [application/octet-stream]
Saving to: ‘pico_img.png’

pico_img.png                           100%[===========================================================================>] 106.25K  --.-KB/s    in 0.1s    

2026-03-09 23:42:11 (884 KB/s) - ‘pico_img.png’ saved [108795/108795]

                                                                                                                                                           
┌──(kali㉿kali)-[~/picoCTF/forensic/someta]
└─$ ls
pico_img.png
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoCTF/forensic/someta]
└─$ exiftool pico_img.png

ExifTool Version Number         : 13.36
File Name                       : pico_img.png
Directory                       : .
File Size                       : 109 kB
File Modification Date/Time     : 2025:11:21 14:11:06-05:00
File Access Date/Time           : 2026:03:09 23:42:11-04:00
File Inode Change Date/Time     : 2026:03:09 23:42:11-04:00
File Permissions                : -rw-rw-r--
File Type                       : PNG
File Type Extension             : png
MIME Type                       : image/png
Image Width                     : 600
Image Height                    : 600
Bit Depth                       : 8
Color Type                      : RGB
Compression                     : Deflate/Inflate
Filter                          : Adaptive
Interlace                       : Noninterlaced
Software                        : Adobe ImageReady
XMP Toolkit                     : Adobe XMP Core 5.3-c011 66.145661, 2012/02/06-14:56:27
Creator Tool                    : Adobe Photoshop CS6 (Windows)
Instance ID                     : xmp.iid:A5566E73B2B811E8BC7F9A4303DF1F9B
Document ID                     : xmp.did:A5566E74B2B811E8BC7F9A4303DF1F9B
Derived From Instance ID        : xmp.iid:A5566E71B2B811E8BC7F9A4303DF1F9B
Derived From Document ID        : xmp.did:A5566E72B2B811E8BC7F9A4303DF1F9B
Artist                          : picoCTF{s0_m3ta_81e30680}
Image Size                      : 600x600
Megapixels                      : 0.360
                                                
```