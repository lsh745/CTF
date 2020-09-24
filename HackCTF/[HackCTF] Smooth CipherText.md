# [HackCTF] Smooth CipherText

![download (2)](/Users/lsh/Desktop/download (2).png)

It seems to be Vigenere Cipher. Because its IC is 0.04372. Which means it will be a polyalphabetic cipher. but I don't know the key. However, I know this CTFs flag format. it means LymoADJ in the given data is HackCTF. as this ciphertext is encrypted by Vigener Cipher, I'd better think these alphabets to numbers. Like A = 0, B = 1, C = 2,... Y = 24, Z = 25.

When does so, 

| **L** | **y** | **m** | **o** | **A** | **D** | **J** |
| ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| 11    | 24    | 12    | 14    | 00    | 03    | 09    |
| **H** | **a** | **c** | **k** | **C** | **T** | **F** |
| 07    | 00    | 02    | 10    | 02    | 19    | 05    |

 

This is what I have and what I want. Now I should subtract the values in the same column.

 

**11 - 07 = 4**

**24 - 00 = 24**

**12 - 02 = 10**

**14 - 10 = 4**

**00 - 02 = -2 = 24 \**(-2 % 26)\****

**03 - 19 = -16 = 10 \**(-16 % 26)\****

**09 - 05 = 4**

 

I found 4, 24, 10 is repeating continuously. and 4, 24, 10 is E, Y, K. Key should be the combination of E, Y, K. but at the first glance, I can think this is K, E, Y.

One step advanced to the decryption. Now I'll use this key to the ciphertext. 

| **R** | **i** | **j** | **v** | **s** | **m** | **y** | **s** | **m** | **y** |
| ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| 17    | 08    | 09    | 21    | 18    | 12    | 24    | 18    | 12    | 24    |
| **K** | **E** | **Y** | **K** | **E** | **Y** | **K** | **E** | **Y** | **K** |
| 10    | 4     | 24    | 10    | 4     | 24    | 10    | 4     | 24    | 10    |

 

**SPOILER ALERT. FLAG INCLUDED**

![download (3)](/Users/lsh/Desktop/download (3).png)