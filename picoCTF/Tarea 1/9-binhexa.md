#### Description

How well can you perfom basic binary operations?Start searching for the flag here `nc titan.picoctf.net 61226`
## Solucion 
```
Jose323-picoctf@webshell:~$ nc titan.picoctf.net 61226

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 10010101
Binary Number 2: 11111011


Question 1/6:
Operation 1: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 01111101
Correct!

Question 2/6:
Operation 2: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 100100011101001
Incorrect. Try again
Enter the binary result: 11111011
Incorrect. Try again
Enter the binary result: picoCTF{0x12904}

Incorrect input. Provide the right input
Enter the binary result: picoCTF{0x68}

Incorrect input. Provide the right input
Enter the binary result: 1001001000010111
Correct!

Question 3/6:
Operation 3: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 10010001
Correct!

Question 4/6:
Operation 4: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11111111
Correct!

Question 5/6:
Operation 5: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 110010000
Correct!

Question 6/6:
Operation 6: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 100101010
Correct!

Enter the results of the last operation in hexadecimal: 

Incorrect input. Provide the right input!

Enter the results of the last operation in hexadecimal: 12A

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_1367e2c6}
```