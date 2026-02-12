#### Description

Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin.Login via `ssh` as `ctf-player` with the password, `8c606eb1` on the host `wily-courier.picoctf.net` and port `64820`.
## Solucion 
```
Jose323-picoctf@webshell:~$ ssh ctf-player@wily-courier.picoctf.net -p 64820
The authenticity of host '[wily-courier.picoctf.net]:64820 ([18.189.99.27]:64820)' can't be established.
ED25519 key fingerprint is SHA256:ErlUUvYlrAxfSW1tIdzfOnGTBSr5OFkZvz0nMN4Vodw.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[wily-courier.picoctf.net]:64820' (ED25519) to the list of known hosts.
ctf-player@wily-courier.picoctf.net's password: 
Welcome to Ubuntu 18.04.6 LTS (GNU/Linux 6.14.0-1012-aws x86_64)

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

ctf-player@pico-chall$ ls
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ cat 1of3.flag.txt
picoCTF{xxsh_
ctf-player@pico-chall$ cat instructions-to-2of3.txt
Next, go to the root of all things, more succinctly `/`
ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ ls
2of3.flag.txt  challenge  home                      lib64  opt   run   sys  var
bin            dev        instructions-to-3of3.txt  media  proc  sbin  tmp
boot           etc        lib                       mnt    root  srv   usr
ctf-player@pico-chall$ find / -name "2of3.flag.txt" 2>/dev/null
/2of3.flag.txt
ctf-player@pico-chall$ cat /ruta/que_aparezca/2of3.flag.txt
cat: /ruta/que_aparezca/2of3.flag.txt: No such file or directory
ctf-player@pico-chall$ cat /2of3.flag.txt
0ut_0f_//4t3r_
ctf-player@pico-chall$ instructions-to-3of3.txt
-bash: instructions-to-3of3.txt: command not found
ctf-player@pico-chall$ cat /instructions-to-3of3.txt
Lastly, ctf-player, go home... more succinctly `~`
ctf-player@pico-chall$ cd ~
ctf-player@pico-chall$ ls
3of3.flag.txt  drop-in
ctf-player@pico-chall$ find ~ -name "3of3.flag.txt"
/home/ctf-player/3of3.flag.txt
ctf-player@pico-chall$ cat ~/3of3.flag.txt
0b24fc4f}ctf-player@pico-chall$ Connection to wily-courier.picoctf.net closed by remote host.
Connection to wily-courier.picoctf.net closed.
Jose323-picoctf@webshell:~$ 
```
picoCTF{xxsh_0ut_0f_//4t3r_0b24fc4f}