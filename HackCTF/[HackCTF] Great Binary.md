# [HackCTF] Great Binary

https://github.com/lsh745/CTF/blob/master/HackCTF/pic/download.png

I found the data from the attached zip file.

 

**Data :** 01001000 01100001 01100011 01101011 01000011 01010100 01000110 01111011 01100011 01110010 01111001 01110000 

01110100 01101111 01011111 01110110 00110010 01110010 01111001 01011111 01100101 01100001 01110011 01111001 01011111 

01110000 01110010 00110000 01100010 00110001 01100101 01101101 01111101

 

It seems to be binary values of ASCII data. so I wrote code.

```
[print(chr(int(i, 2)), end = "") for i in input().split()]
```

 

and this is the result.

**SPOILER ALERT. FLAG INCLUDED**



https://github.com/lsh745/CTF/blob/master/HackCTF/pic/download(1).png
