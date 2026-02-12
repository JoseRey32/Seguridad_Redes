## Descripción

Can you look at the data in this binary? The bash script might help![static](https://challenge-files.picoctf.net/c_wily_courier/b6c2dd492eb053dfbb3fcfa9eb142c8d11f6a00c0691031fc92b045d65b6e56a/static), [ltdis.sh](https://challenge-files.picoctf.net/c_wily_courier/b6c2dd492eb053dfbb3fcfa9eb142c8d11f6a00c0691031fc92b045d65b6e56a/ltdis.sh)
## Solución
```
Jose323-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/b6c2dd492eb053dfbb3fcfa9eb142c8d11f6a00c0691031fc92b045d65b6e56a/static
--2026-02-12 03:14:58--  https://challenge-files.picoctf.net/c_wily_courier/b6c2dd492eb053dfbb3fcfa9eb142c8d11f6a00c0691031fc92b045d65b6e56a/static
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.18, 3.160.5.95, 3.160.5.40, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16776 (16K) [application/octet-stream]
Saving to: 'static'

static               100%[===================>]  16.38K  --.-KB/s    in 0.006s  

2026-02-12 03:14:59 (2.56 MB/s) - 'static' saved [16776/16776]

Jose323-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/b6c2dd492eb053dfbb3fcfa9eb142c8d11f6a00c0691031fc92b045d65b6e56a/ltdis.sh
--2026-02-12 03:14:59--  https://challenge-files.picoctf.net/c_wily_courier/b6c2dd492eb053dfbb3fcfa9eb142c8d11f6a00c0691031fc92b045d65b6e56a/ltdis.sh
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.40, 3.160.5.18, 3.160.5.95, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 785 [application/octet-stream]
Saving to: 'ltdis.sh'

ltdis.sh             100%[===================>]     785  --.-KB/s    in 0s      

2026-02-12 03:14:59 (153 MB/s) - 'ltdis.sh' saved [785/785]

Jose323-picoctf@webshell:~$ chmod +x static ltdis.sh
Jose323-picoctf@webshell:~$ strings static | grep picoCTF
picoCTF{d15a5m_t34s3r_20335e41}
Jose323-picoctf@webshell:~$ 
```