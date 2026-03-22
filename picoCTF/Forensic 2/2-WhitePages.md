## Descripción

I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://challenge-files.picoctf.net/c_fickle_tempest/4de4b105d28cb6df34d9805217f2460b978a37dafc3dfc50edadd8d424dd311a/whitepages.txt) is all blank!
## Solución 

```
┌──(kali㉿kali)-[~/picoCTF/forensic/Whitepages]
└─$ python3 - << 'EOF'
data=open("whitepages.txt","rb").read()

data=data.replace(b'\xe2\x80\x83',b'0')  # em space = 0
data=data.replace(b' ',b'1')             # normal space = 1
data=data.replace(b'\n',b'')

binary=data.decode()

n=int(binary,2)
flag=n.to_bytes((n.bit_length()+7)//8,'big')

print(flag.decode())
EOF

picoCTF

SEE PUBLIC RECORDS & BACKGROUND REPORT
5000 Forbes Ave, Pittsburgh, PA 15213
picoCTF{not_all_spaces_are_created_equal_f5d46aff52c6e17f9fd6317b33d2d783}

                                                                                                                                                           
┌──(kali㉿kali)-[~/picoCTF/forensic/Whitepages]
└─$ 

```