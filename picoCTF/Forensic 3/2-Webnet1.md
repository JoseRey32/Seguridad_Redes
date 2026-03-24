## Descripción

We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/d1e9add4e31989553f239ebf71ba5972f9bed7bd4932f931e14bfba80d75f815/capture.pcap) and [key](https://challenge-files.picoctf.net/c_fickle_tempest/d1e9add4e31989553f239ebf71ba5972f9bed7bd4932f931e14bfba80d75f815/picopico.key). Recover the flag.
## Solución 
```
                                                                                                                                                         
┌──(kali㉿kali)-[~]
└─$ cd picoctf
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf]
└─$ cd forensic
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic]
└─$ cd Webnet1 
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/Webnet1]
└─$ open vulture.jpg   
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/Webnet1]
└─$ strings vulture.jpg -n15
picoCTF{honey.roasted.peanuts}
 )/'%'/9339GDG]]}
 )/'%'/9339GDG]]}
%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz

```
