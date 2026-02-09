#### Descripción

What does this bDNhcm5fdGgzX3IwcDM1 mean? I think it has something to do with bases.
## Solución
## Solucion 1 - Consola 
```
Jose323-picoctf@webshell:~$ echo 'bDNhcm5fdGgzX3IwcDM' | base64 -d
l3arn_th3_r0p3base64: invalid input
```
## Solucion 2 Cyberchef
- https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=YkROaGNtNWZkR2d6WDNJd2NETTE