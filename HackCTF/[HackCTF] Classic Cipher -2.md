# [HackCTF] Classic Cipher -2

![download (5)](https://github.com/lsh745/CTF/blob/master/HackCTF/pic/download%20(5).png)

**Ciphertext** : hreCp1_ev_s117nr_ys17eer132n_5

 

Well, there's a key with ciphertext(suggests this ciphertext needs a key and will be number). its IC is high(0.09167), meaning the cipher will be transposition cipher or a monoalphabetic substitution. but I can find a single capital letter in the given ciphertext. and I can think it is the first letter of the ciphertext. so I can think about some kind of matching ciphers. in this case(of course, I tried a few times), this is **Transposition Cipher**.

 

| **Key**       | **p ** | **y** | **t** | **h** | **o** | **n** |
| ------------- | ------ | ----- | ----- | ----- | ----- | ----- |
| **ASCII**     | 112    | 121   | 116   | 104   | 111   | 110   |
| **Key Index** | 3      | 5     | 4     | 0     | 2     | 1     |

**Key Index** is an important part of this table which can make us decrypt the ciphertext. in Transposition Cipher, slice the ciphertext by the length of the **Index** and apply the values of the **Key** **Index.** for example, the length of the key is 6, starting 6 letters of ciphertext is **hreCp1**, In order of **Key Index : [3, 5, 4, 0, 2, 1]**

 

**Key Index[0] = 3 = Ciphertext[3] = C**

***\*Key Index[1] = 5 = Ciphertext[5] = 1\****

***\**\*Key Index[2] = 4 = Ciphertext[4] = p\*\**\***

***\**\*Key Index[3] = 0 = Ciphertext[0] = h\*\**\***

***\**\*\*\*Key Index[4] = 2 = Ciphertext[2] = e\*\*\*\*\****

**Key Index[5] = 1 = Ciphertext[1] = r**

 

**Result = C1pher**

 

Do the same with rest ciphertext.

 

***\*SPOILER ALERT. FLAG INCLUDED\****

```
inp = "hreCp1_ev_s117nr_ys17eer132n_5"
key = input()

rkey = []
for i in key.upper():
    rkey.append(ord(i) - 65)

seq = []
while len(seq) < len(rkey):
    rmin = rkey.index(min(rkey))
    seq.append(rmin)
    rkey[rmin] = float('inf')
lseq = len(seq)

print(seq)
tmp = 0
for i in range(len(inp) - lseq - 1):
    if i % lseq == 0 and i != 0:
        tmp += lseq
    print(inp[tmp + seq[i % lseq]], end = "")
```

