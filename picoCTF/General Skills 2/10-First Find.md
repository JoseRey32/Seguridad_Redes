## Descripción

Unzip this archive and find the file named 'uber-secret.txt'

- [Download zip file](https://artifacts.picoctf.net/c/501/files.zip)
## Solución 
```
Jose323-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/501/files.zip
--2026-02-12 04:02:59--  https://artifacts.picoctf.net/c/501/files.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.33, 3.170.131.72, 3.170.131.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.33|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3995553 (3.8M) [application/octet-stream]
Saving to: 'files.zip'

files.zip            100%[===================>]   3.81M  1.81MB/s    in 2.1s    

2026-02-12 04:03:01 (1.81 MB/s) - 'files.zip' saved [3995553/3995553]

Jose323-picoctf@webshell:~$ ls
Addadshashanammu      big-zip-files.zip    files.zip  salida.txt
Addadshashanammu.zip  big-zip-files.zip.1  flag       static
README.txt            enc_flag             flag.1     strings
big-zip-files         enc_flag.1           ltdis.sh   warm
Jose323-picoctf@webshell:~$ unzip archive.zip
unzip:  cannot find or open archive.zip, archive.zip.zip or archive.zip.ZIP.
Jose323-picoctf@webshell:~$ unzip files.zip
Archive:  files.zip
   creating: files/
   creating: files/satisfactory_books/
   creating: files/satisfactory_books/more_books/
  inflating: files/satisfactory_books/more_books/37121.txt.utf-8  
  inflating: files/satisfactory_books/23765.txt.utf-8  
  inflating: files/satisfactory_books/16021.txt.utf-8  
  inflating: files/13771.txt.utf-8   
   creating: files/adequate_books/
   creating: files/adequate_books/more_books/
   creating: files/adequate_books/more_books/.secret/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/
 extracting: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt  
  inflating: files/adequate_books/more_books/1023.txt.utf-8  
  inflating: files/adequate_books/46804-0.txt  
  inflating: files/adequate_books/44578.txt.utf-8  
   creating: files/acceptable_books/
   creating: files/acceptable_books/more_books/
  inflating: files/acceptable_books/more_books/40723.txt.utf-8  
  inflating: files/acceptable_books/17880.txt.utf-8  
  inflating: files/acceptable_books/17879.txt.utf-8  
  inflating: files/14789.txt.utf-8   
Jose323-picoctf@webshell:~$ cd files
Jose323-picoctf@webshell:~/files$ find . -name "uber-secret.txt"
./adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
Jose323-picoctf@webshell:~/files$ cat ./ruta/que_aparezca/uber-secret.txt
cat: ./ruta/que_aparezca/uber-secret.txt: No such file or directory
Jose323-picoctf@webshell:~/files$ grep -R "picoCTF" .
./adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt:picoCTF{f1nd_15_f457_ab443fd1}
Jose323-picoctf@webshell:~/files$ 
```