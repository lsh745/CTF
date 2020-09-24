# [Defend the Web] Crypt 3

![download](https://github.com/lsh745/CTF/blob/master/Defend%20The%20Web/pic/download%20(4).png)

Oh. The hyphens, periods, slashes, and spaces. What will they mean? Not at first glance, but from my little experiences, I recalled that there are morse code, international maritime signal flags, telephone keypads, encodings, etc. in some CTFs. So... maybe this ciphertext can be morse code.

[The morse code](https://en.wikipedia.org/wiki/Morse_code) has two different signal durations, called *dots* and *dashes* or *dits* and *dash* (they will be colon and hyphen). Space will be the divider, and slash means space. I made a morse code translator in python by using a morse code dictionary. But I can find untranslated or mistranslated text.

```
Expected Text       : .... .. --..-- => Hi,
Output from Program : .... .. -..-   => HIX
```

Like this, the problem is the characters that neither alphabets nor numbers. Now I found the problem, and the solution is just adding some special characters in the morse code dictionary. Finally, I fixed some errors and translation is done.

 

***\*SPOILER ALERT. FLAG INCLUDED\****

***\*HI, THANKS TO SAMUEL MORSE THE TRANSMISSION OF TELEGRAPHIC INFORMATION WAS STANDARDIZED. HE USED DOTS AND DASHES TO CREATE A STANDARD WAY OF COMMUNICATION, HE HAS HELPED YOU TODAY TO GET THE PASS: THANKYOUSIR\****