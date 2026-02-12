##  Descripción 

Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames.[Addadshashanammu.zip](https://challenge-files.picoctf.net/c_wily_courier/730d9106a6ce1d52c6463b90937ec89f5eb661388954fbd15cfa0c8a2eec012f/Addadshashanammu.zip)
## Solución
```
Jose323-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/730d9106a6ce1d52c6463b90937ec89f5eb661388954fbd15cfa0c8a2eec012f/Addadshashanammu.zip
--2026-02-12 03:30:41--  https://challenge-files.picoctf.net/c_wily_courier/730d9106a6ce1d52c6463b90937ec89f5eb661388954fbd15cfa0c8a2eec012f/Addadshashanammu.zip
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.64, 3.160.5.40, 3.160.5.95, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 5166 (5.0K) [application/octet-stream]
Saving to: 'Addadshashanammu.zip'

Addadshashanammu.zip 100%[===================>]   5.04K  --.-KB/s    in 0s      

2026-02-12 03:30:41 (1.54 GB/s) - 'Addadshashanammu.zip' saved [5166/5166]

Jose323-picoctf@webshell:~$ unzip Addadshashanammu.zip
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
 extracting: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet.c  
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
Jose323-picoctf@webshell:~$ cd Addadshashanammu
Jose323-picoctf@webshell:~/Addadshashanammu$ ls
Almurbalarammi
Jose323-picoctf@webshell:~/Addadshashanammu$ cd <TAB>
-bash: syntax error near unexpected token `newline'
Jose323-picoctf@webshell:~/Addadshashanammu$ cd <TAB>
-bash: syntax error near unexpected token `newline'
Jose323-picoctf@webshell:~/Addadshashanammu$ ...
-bash: ...: command not found
Jose323-picoctf@webshell:~/Addadshashanammu$ chmod +x nombre_del_archivo
chmod: cannot access 'nombre_del_archivo': No such file or directory
Jose323-picoctf@webshell:~/Addadshashanammu$ ./nombre_del_archivo
-bash: ./nombre_del_archivo: No such file or directory
Jose323-picoctf@webshell:~/Addadshashanammu$ cd Almurbalarammi
Jose323-picoctf@webshell:~/Addadshashanammu/Almurbalarammi$ cd Ashalmimilkala
Jose323-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala$ cd Assurnabitashpi
Jose323-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurna
bitashpi$ cd Maelkashishi
Jose323-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurna
bitashpi/Maelkashishi$ cd Onnissiralis
Jose323-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurna
bitashpi/Maelkashishi/Onnissiralis$ cd Ularradallaku
Jose323-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurna
bitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls
fang-of-haynekhtnamet  fang-of-haynekhtnamet.c
Jose323-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurna
bitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ chmod +x fang-of-haynekhtnamet
Jose323-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurna
bitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ./fang-of-haynekhtnamet
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}
```