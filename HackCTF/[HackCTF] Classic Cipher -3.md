# [HackCTF] Classic Cipher -3

![download (7)](https://github.com/lsh745/CTF/blob/master/HackCTF/pic/download%20(7).png)

**Ciphertext** : FqyeYBX{Yv4kk1y_Y1lfgt_1k_jgti_g4ki_1x91cqx14x}

**IC** : 0.06667

 

As its IC is high, I can think it is a transposition cipher like Caesar Cipher. in this case, YBX should be CTF. but if this is Caesar, the order in Alphabet will be C, d, e, F, and the ciphertext is YBX(Y, X). The order is not the same. Now I can think this is not a Caesar Cipher, and I

can also think the cipher will be Vigenere or Affine. 

In the next result, I can't find any key-like words. now I can remove Vigenere from my mind.

```
ctxt		ptxt		ctn		ptn		c-p		mod(alp)
F		H		 05		 07		-02		24(Y)
q		a		 16		 00		 16		16(Q)
y		c		 24		 02		 22		22(W)
e		k		 04		 10		-06		20(U)
Y		C		 24		 02		 22		22(W)
B		T		 01		 19		-18		08(I)
X		F		 23		 05		 18		18(S)
```

Now Affine, this cipher is Poly-Alphabetic Cipher. IC is high enough to think the cipher is a transposition cipher. but this isn't. 

[Affine Cipher](https://www.dcode.fr/affine-cipher) is Encryption uses a classic alphabet, and two integers, called coefficients or keys A and B, these are the parameters of the affine function Ax+B.

Cipher can be solved by brute-forcing. so I made a tool.

 

***\*SPOILER ALERT. FLAG INCLUDED\****

![download (8)](https://github.com/lsh745/CTF/blob/master/HackCTF/pic/download%20(8).png)