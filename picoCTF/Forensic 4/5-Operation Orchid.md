## Descripción

Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/213/disk.flag.img.gz)
## Solución 
```
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/OperationOrchid]
└─$ icat disk.flag.img -o 411648 1875       
touch flag.txt
nano flag.txt 
apk get nano
apk --help
apk add nano
nano flag.txt 
openssl
openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
shred -u flag.txt
ls -al
halt
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/OperationOrchid]
└─$ openssl -h            
help:

Standard commands
asn1parse         ca                ciphers           cmp               
cms               crl               crl2pkcs7         dgst              
dhparam           dsa               dsaparam          ec                
ecparam           enc               engine            errstr            
fipsinstall       gendsa            genpkey           genrsa            
help              info              kdf               list              
mac               nseq              ocsp              passwd            
pkcs12            pkcs7             pkcs8             pkey              
pkeyparam         pkeyutl           prime             rand              
rehash            req               rsa               rsautl            
s_client          s_server          s_time            sess_id           
skeyutl           smime             speed             spkac             
srp               storeutl          ts                verify            
version           x509              

Message Digest commands (see the `dgst' command for more details)
blake2b512        blake2s256        md4               md5               
rmd160            sha1              sha224            sha256            
sha3-224          sha3-256          sha3-384          sha3-512          
sha384            sha512            sha512-224        sha512-256        
shake128          shake256          sm3               

Cipher commands (see the `enc' command for more details)
aes-128-cbc       aes-128-ecb       aes-192-cbc       aes-192-ecb       
aes-256-cbc       aes-256-ecb       aria-128-cbc      aria-128-cfb      
aria-128-cfb1     aria-128-cfb8     aria-128-ctr      aria-128-ecb      
aria-128-ofb      aria-192-cbc      aria-192-cfb      aria-192-cfb1     
aria-192-cfb8     aria-192-ctr      aria-192-ecb      aria-192-ofb      
aria-256-cbc      aria-256-cfb      aria-256-cfb1     aria-256-cfb8     
aria-256-ctr      aria-256-ecb      aria-256-ofb      base64            
bf                bf-cbc            bf-cfb            bf-ecb            
bf-ofb            camellia-128-cbc  camellia-128-ecb  camellia-192-cbc  
camellia-192-ecb  camellia-256-cbc  camellia-256-ecb  cast              
cast-cbc          cast5-cbc         cast5-cfb         cast5-ecb         
cast5-ofb         des               des-cbc           des-cfb           
des-ecb           des-ede           des-ede-cbc       des-ede-cfb       
des-ede-ofb       des-ede3          des-ede3-cbc      des-ede3-cfb      
des-ede3-ofb      des-ofb           des3              desx              
rc2               rc2-40-cbc        rc2-64-cbc        rc2-cbc           
rc2-cfb           rc2-ecb           rc2-ofb           rc4               
rc4-40            seed              seed-cbc          seed-cfb          
seed-ecb          seed-ofb          sm4-cbc           sm4-cfb           
sm4-ctr           sm4-ecb           sm4-ofb           zlib              
zstd              

                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/OperationOrchid]
└─$ openssl aes256 help
aes256: Extra option: "help"
aes256: Use -help for summary.
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/OperationOrchid]
└─$                    
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/OperationOrchid]
└─$ openssl aes256 -salt -out  flag.txt -in flag.txt.enc -k unbreakablepassword1234567 -d

Can't open "flag.txt.enc" for reading, No such file or directory
404767E3777F0000:error:80000002:system library:BIO_new_file:No such file or directory:../crypto/bio/bss_file.c:67:calling fopen(flag.txt.enc, rb)
404767E3777F0000:error:10000080:BIO routines:BIO_new_file:no such file:../crypto/bio/bss_file.c:75:
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/OperationOrchid]
└─$ ls
disk.flag.img
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/OperationOrchid]
└─$ icat disk.flag.img -o 411648 1782 > flag.txt.enc                                     
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/OperationOrchid]
└─$ openssl aes256 -salt -out  flag.txt -in flag.txt.enc -k unbreakablepassword1234567 -d

*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
bad decrypt
40172A1EAC7F0000:error:1C800064:Provider routines:ossl_cipher_unpadblock:bad decrypt:../providers/implementations/ciphers/ciphercommon_block.c:107:
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/OperationOrchid]
└─$ ls
disk.flag.img  flag.txt  flag.txt.enc
                                                                                                                                                           
┌──(kali㉿kali)-[~/picoctf/forensic/OperationOrchid]
└─$ cat flag.txt
picoCTF{h4un71ng_p457_5113beab} 
```