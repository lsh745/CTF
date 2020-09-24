# [Defend the Web] Crypt 4

![download](https://github.com/lsh745/CTF/blob/master/Defend%20The%20Web/pic/download%20(5).png)

IC : 0.08170

This looks like transposition cipher again. So I tried Caesar and Vigenere Cipher. But not them. Because I don't know how it was encrypted, I just replaced letters that I know.

For the reason of convenience, the unchanged letters are indicated as upper case, and changed will be lower case.

 

```
J -> p
h -> a
l -> s

Result : DC, GDCs Cs a sCRCSaN CKQa GZ SQWQS GUZ. GDCs GCRQ QaYD SQGGQN Cs assCOMQK a spQYCACQK NQSaGCZMsDCp UCGD aMZGDQN SQGGQN. pass: CDaWQANCQMKs
```

 

As I can see **Cs** twice in the result,  I'll treat C as i. 

```
C -> i

Result : Di, GDis is a siRiSaN iKQa GZ SQWQS GUZ. GDis GiRQ QaYD SQGGQN is assiOMQK a spQYiAiQK NQSaGiZMsDip UiGD aMZGDQN SQGGQN. pass: iDaWQANiQMKs
```

 

Maybe **Di** is Hi. Therefore **GDis** will be **Ghis**, and **Ghis** looks like **this**.

```
D -> h
G -> t

Result : hi, this is a siRiSaN iKQa tZ SQWQS tUZ. this tiRQ QaYh SQttQN is assiOMQK a spQYiAiQK NQSatiZMship Uith aMZthQN SQttQN. pass: ihaWQANiQMKs
```

 

I think it works! After a few more like this, there is an answer.

***\*SPOILER ALERT. FLAG INCLUDED\****

![download](https://github.com/lsh745/CTF/blob/master/Defend%20The%20Web/pic/download%20(6).png)

**tiRQ** will be **time**, **tZ** will be **to, Uith** will be **with**, etc. 

hi, this is a similar idea to level two. this time each letter is assigned a specified relationship with another letter. pass: ihavefriends