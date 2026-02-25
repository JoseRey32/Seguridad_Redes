## Descripción

Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/159/challenge.zip)
## Solución 
```
Jose323-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c_titan/138/challenge.zip
--2026-02-25 02:50:55--  https://artifacts.picoctf.net/c_titan/138/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.33, 3.170.131.18, 3.170.131.72, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.33|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 19199 (19K) [application/octet-stream]
Saving to: 'challenge.zip.1'

challenge.zip.1      100%[===================>]  18.75K  --.-KB/s    in 0.002s  

2026-02-25 02:50:55 (11.6 MB/s) - 'challenge.zip.1' saved [19199/19199]

Jose323-picoctf@webshell:~$ unzip challenge.zip -d reto138
Archive:  challenge.zip
   creating: reto138/drop-in/
   creating: reto138/drop-in/.git/
   creating: reto138/drop-in/.git/branches/
  inflating: reto138/drop-in/.git/description  
   creating: reto138/drop-in/.git/hooks/
  inflating: reto138/drop-in/.git/hooks/applypatch-msg.sample  
  inflating: reto138/drop-in/.git/hooks/commit-msg.sample  
  inflating: reto138/drop-in/.git/hooks/fsmonitor-watchman.sample  
  inflating: reto138/drop-in/.git/hooks/post-update.sample  
  inflating: reto138/drop-in/.git/hooks/pre-applypatch.sample  
  inflating: reto138/drop-in/.git/hooks/pre-commit.sample  
  inflating: reto138/drop-in/.git/hooks/pre-merge-commit.sample  
  inflating: reto138/drop-in/.git/hooks/pre-push.sample  
  inflating: reto138/drop-in/.git/hooks/pre-rebase.sample  
  inflating: reto138/drop-in/.git/hooks/pre-receive.sample  
  inflating: reto138/drop-in/.git/hooks/prepare-commit-msg.sample  
  inflating: reto138/drop-in/.git/hooks/update.sample  
   creating: reto138/drop-in/.git/info/
  inflating: reto138/drop-in/.git/info/exclude  
   creating: reto138/drop-in/.git/refs/
   creating: reto138/drop-in/.git/refs/heads/
 extracting: reto138/drop-in/.git/refs/heads/master  
   creating: reto138/drop-in/.git/refs/tags/
 extracting: reto138/drop-in/.git/HEAD  
  inflating: reto138/drop-in/.git/config  
   creating: reto138/drop-in/.git/objects/
   creating: reto138/drop-in/.git/objects/pack/
   creating: reto138/drop-in/.git/objects/info/
   creating: reto138/drop-in/.git/objects/fc/
 extracting: reto138/drop-in/.git/objects/fc/a28bbf8dde2f49246166ae6512a1046fc4cbc3  
   creating: reto138/drop-in/.git/objects/61/
 extracting: reto138/drop-in/.git/objects/61/db7d05a8b7657aedc1e13320ca53623a364fe7  
   creating: reto138/drop-in/.git/objects/ea/
 extracting: reto138/drop-in/.git/objects/ea/859bf3b5d94ee74ce5ee1afa3edd7d4d6b35f0  
   creating: reto138/drop-in/.git/objects/d5/
 extracting: reto138/drop-in/.git/objects/d5/52d1ecd2d83fa2e65b6724d1ff73b45a7d59b7  
   creating: reto138/drop-in/.git/objects/0c/
 extracting: reto138/drop-in/.git/objects/0c/1ab266b7a3a1cd099bb509f82b7a2d03aecd03  
   creating: reto138/drop-in/.git/objects/ef/
 extracting: reto138/drop-in/.git/objects/ef/0b7cc6b98367fa168573c931e0f7098ef59182  
  inflating: reto138/drop-in/.git/index  
 extracting: reto138/drop-in/.git/COMMIT_EDITMSG  
   creating: reto138/drop-in/.git/logs/
  inflating: reto138/drop-in/.git/logs/HEAD  
   creating: reto138/drop-in/.git/logs/refs/
   creating: reto138/drop-in/.git/logs/refs/heads/
  inflating: reto138/drop-in/.git/logs/refs/heads/master  
 extracting: reto138/drop-in/message.txt  
Jose323-picoctf@webshell:~$ ls
Addadshashanammu  drop-in              level2.flag.txt.enc  reto137
README.txt        files                level2.py            reto138
big-zip-files     fixme2.py            level3.flag.txt.enc  serpentine.py
challenge.zip     level1.flag.txt.enc  level3.hash.bin
challenge.zip.1   level1.py            level3.py
Jose323-picoctf@webshell:~$ cd drop-in
Jose323-picoctf@webshell:~/drop-in$ git log
Jose323-picoctf@webshell:~/drop-in$ git log --pretty=format:"%an"
Jose323-picoctf@webshell:~/drop-in$ git log --pretty=format:"%ae"
Jose323-picoctf@webshell:~/drop-in$ picoCTF{ops@picoctf.com}
-bash: picoCTF{ops@picoctf.com}: command not found
Jose323-picoctf@webshell:~/drop-in$ picoCTF{ops}
-bash: picoCTF{ops}: command not found
Jose323-picoctf@webshell:~/drop-in$ git log
Jose323-picoctf@webshell:~/drop-in$ git log --pretty=format:"%H %an %ae"
Jose323-picoctf@webshell:~/drop-in$ git log --pretty=format:"%an"
Jose323-picoctf@webshell:~/drop-in$ 
Jose323-picoctf@webshell:~/drop-in$ cat message.
cat: message.: No such file or directory
Jose323-picoctf@webshell:~/drop-in$ git long
git: 'long' is not a git command. See 'git --help'.

The most similar commands are
        clone
        log
Jose323-picoctf@webshell:~/drop-in$ git long message.py
git: 'long' is not a git command. See 'git --help'.

The most similar commands are
        clone
        log
Jose323-picoctf@webshell:~/drop-in$ cd reto137/drop-in
-bash: cd: reto137/drop-in: No such file or directory
Jose323-picoctf@webshell:~/drop-in$ ls -a
.  ..  .git  message.txt
Jose323-picoctf@webshell:~/drop-in$ git --git-dir=.git log
Jose323-picoctf@webshell:~/drop-in$ git show 87b85d7dfb839b077678611280fa023d76e017b8:message.txt
Jose323-picoctf@webshell:~/drop-in$ git show 87b85d7dfb839b077678611280fa023d76e017b8:message.txt
Jose323-picoctf@webshell:~/drop-in$ rm -rf reto
Jose323-picoctf@webshell:~/drop-in$ unzip challenge.zip -d reto
unzip:  cannot find or open challenge.zip, challenge.zip.zip or challenge.zip.ZIP.
Jose323-picoctf@webshell:~/drop-in$ cd reto/drop-in
-bash: cd: reto/drop-in: No such file or directory
Jose323-picoctf@webshell:~/drop-in$ git show 87b85d7dfb839b077678611280fa023d76e017b8:message.txt
Jose323-picoctf@webshell:~/drop-in$ git show 87b85d7dfb839b077678611280fa023d76e017b8:message.txt | cat
picoCTF{s@n1t1z3_ea83ff2a}
Jose323-picoctf@webshell:~/drop-in$ 
```