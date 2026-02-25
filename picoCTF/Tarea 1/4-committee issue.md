#### Description

I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/136/challenge.zip)
## Solucion 
```
commit 8dc51806c760dfdbb34b33a2008926d3d8e8ad49 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:17 2024 +0000

    remove sensitive info

diff --git a/message.txt b/message.txt
index bae247d..d552d1e 100644
--- a/message.txt
+++ b/message.txt
@@ -1 +1 @@
-picoCTF{s@n1t1z3_ea83ff2a}
+TOP SECRET

commit 87b85d7dfb839b077678611280fa023d76e017b8
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:17 2024 +0000

    create flag

diff --git a/message.txt b/message.txt
new file mode 100644
index 0000000..bae247d
--- /dev/null
+++ b/message.txt
@@ -0,0 +1 @@
+
~
~
(END)
```