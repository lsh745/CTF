# [Defend the Web] Crypt 1 & Crypt 2

![download](https://github.com/lsh745/CTF/blob/master/Defend%20The%20Web/pic/download.png)

Ciphertext : tpyrcoow :ssap siht retne level siht etelpmoc oT .rewop niarb fo tol a yolpme ot deen lliw uoy ,cigol dna noitpyrced tuoba lla era slevel esehT .sihtkcah no slevel tpyrc eht ot emoclew ,olleH

 

It looks REALLY easy. [::-1] will help us.

 

```
inp = "tpyrcoow :ssap siht retne level siht etelpmoc oT .rewop niarb fo tol a yolpme ot deen lliw uoy ,cigol dna noitpyrced tuoba lla era slevel esehT .sihtkcah no slevel tpyrc eht ot emoclew ,olleH"

print(inp[::-1])
```

Done.

 

***\*SPOILER ALERT. FLAG INCLUDED\****

![download](https://github.com/lsh745/CTF/blob/master/Defend%20The%20Web/pic/download%20(1).png)



![download](https://github.com/lsh745/CTF/blob/master/Defend%20The%20Web/pic/download%20(2).png)

We don't even need to check IC. we know the format from the Crypt 1. 'teww' will be 'pass'. and the part 'ss' in 'pass' is the same character, the 'w'. this makes us guess this is the cipher is Caesar Cipher.

as we know 'teww' is 'pass', let's work with this. 

 

**SPOILER ALERT. FLAG INCLUDED**

![download](https://github.com/lsh745/CTF/blob/master/Defend%20The%20Web/pic/download%20(3).png)

I used my code(ctool)
