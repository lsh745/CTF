# [HackCTF] Classic Cipher -1

![download (4)](https://github.com/lsh745/CTF/blob/master/HackCTF/pic/download%20(4).png)

**Data :** ?y4zl4J_d0ur_b0f_0K zp nhsm

The hint is **[::-1]** which means reverse in Python string. 

 

```
data = "?y4zl4J_d0ur_b0f_0K zp nhsm"
print(data[::-1])
```

 

**Result :** mshn pz K0_f0b_ru0d_J4lz4y?

I got reversed string. and it looks like Caesar Cipher. Mostly, in Caesar Cipher(or other Shift Cipher), only non-alphabetical characters are shifted by the rules. so I can think this is Caesar Cipher.

 

***\*SPOILER ALERT. FLAG INCLUDED\****

![download (5)](https://github.com/lsh745/CTF/blob/master/HackCTF/pic/download%20(5).png)

In value 19(T), I can find "flag is D0_y0u_kn0w_C4es4r?"