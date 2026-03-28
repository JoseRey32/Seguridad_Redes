#### Description

If you want to hash with the best, beat this test!`nc saturn.picoctf.net 63240`
## Solución
```
Jose323-picoctf@webshell:~$ nc saturn.picoctf.net 63240
Please md5 hash the text between quotes, excluding the quotes: 'cockroaches'
Answer: 
1936d5f0f3d8e13fc00370b7ef69c14c
1936d5f0f3d8e13fc00370b7ef69c14c
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'jelly beans'
Answer: 
cb7d86ece76c57eac5ed18420ca67ea0
cb7d86ece76c57eac5ed18420ca67ea0
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'leaf blowers'
Answer: 
ae8a766493afae57c7332794c2c5f340
ae8a766493afae57c7332794c2c5f340
Correct.
picoCTF{4ppl1c4710n_r3c31v3d_674c1de2}

```
#### Las Respuestas las obtuve de kali 
```
┌──(kali㉿kali)-[~]
└─$ echo -n 'Count Dracula' | md5sum | cut -d' ' -f1        
aff1b17cdcbc3b40afd42d5fe00297da
                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ echo -n 'cockroaches' | md5sum | cut -d' ' -f1
1936d5f0f3d8e13fc00370b7ef69c14c
                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ echo -n 'jelly beans' | md5sum | cut -d' ' -f1
cb7d86ece76c57eac5ed18420ca67ea0
                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ echo -n 'leaf blowers' | md5sum | cut -d' ' -f1
ae8a766493afae57c7332794c2c5f340
                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ 
```