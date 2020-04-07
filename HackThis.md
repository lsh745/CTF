# HackThis

## CRYPTOGRAPHY

### LEVEL 1

<img width="555" alt="Screen Shot 2019-09-25 at 1 03 05 PM" src="https://user-images.githubusercontent.com/16417991/65599337-ee287880-df9d-11e9-8706-5ef055de7481.png">



**CODE**

```python3
#Crypt 1
print("Crypt 1")
inp = "tpyrcoow :ssap siht retne level siht etelpmoc oT .rewop niarb fo tol a yolpme ot deen lliw uoy ,cigol dna noitpyrced tuoba lla era slevel esehT .sihtkcah no slevel tpyrc eht ot emoclew ,olleH"
print(inp[::-1])
```



**RESULT**

<img width="502" alt="Screen Shot 2019-09-25 at 1 05 49 PM" src="https://user-images.githubusercontent.com/16417991/65599339-eec10f00-df9d-11e9-8b19-1595f28a56a2.png">



**COMMENT**

No special thing. Just reverse



-----

### LEVEL 2

<img width="554" alt="Screen Shot 2019-09-25 at 1 06 36 PM" src="https://user-images.githubusercontent.com/16417991/65599340-eec10f00-df9d-11e9-8403-c209a29d5b33.png">



**CODE**

```python3
# Crypt 2
def caesar(inp):
    mlist = []
    for o in range(22, 26):
    # for o in range(26):
        result = "%2s : " % o
        for i in inp:
            if i >= 'A' and i <= 'Z':
                result += chr((ord(i) - 65 + o) % 26 + 65)

            elif i >= 'a' and i <= 'z':
                result += chr((ord(i) - 97 + o) % 26 + 97)

            else:
                result += i
                
        mlist.append(result)

    return mlist

print("Crypt 2")
inp = "Aipgsqi fego, xlmw pizip mw rsx ew iewc ew xli pewx fyx wxmpp rsx xss gleppirkmrk. Ws ks elieh erh irxiv xlmw teww: wlmjxxlexpixxiv"
for i in caesar(inp):
    print(i)
```



**RESULT**

<img width="498" alt="Screen Shot 2019-09-25 at 1 09 05 PM" src="https://user-images.githubusercontent.com/16417991/65599341-ef59a580-df9d-11e9-97d0-40b52f5fb86a.png">



**COMMENT**

Simple Caesar Cipher. Result is on shift 22.



-----

### LEVEL 3

<img width="555" alt="Screen Shot 2019-09-25 at 1 10 06 PM" src="https://user-images.githubusercontent.com/16417991/65599342-ef59a580-df9d-11e9-86a0-6a6a776655f2.png">



**CODE**

```python3
# Crypt 3
MORSE_CODE_DICT = { 'A':'.-', 'B':'-...', 
                    'C':'-.-.', 'D':'-..', 'E':'.', 
                    'F':'..-.', 'G':'--.', 'H':'....', 
                    'I':'..', 'J':'.---', 'K':'-.-', 
                    'L':'.-..', 'M':'--', 'N':'-.', 
                    'O':'---', 'P':'.--.', 'Q':'--.-', 
                    'R':'.-.', 'S':'...', 'T':'-', 
                    'U':'..-', 'V':'...-', 'W':'.--', 
                    'X':'-..-', 'Y':'-.--', 'Z':'--..', 
                    '1':'.----', '2':'..---', '3':'...--', 
                    '4':'....-', '5':'.....', '6':'-....', 
                    '7':'--...', '8':'---..', '9':'----.', 
                    '0':'-----', ', ':'--..--', '.':'.-.-.-', 
                    '?':'..--..', '/':'-..-.', '-':'-....-', 
                    '(':'-.--.', ')':'-.--.-', ':':'---...',
                    "'":'.----.', '"':'.-..-.', '@':'.--.-.' } 

def morseDecrypt(message): 
    message += ' '
  
    decipher = '' 
    citext = '' 
    for letter in message: 
        if (letter != ' '): 
  
            i = 0
  
            citext += letter 
  
        else: 
            i += 1
  
            if i == 2 : 
                decipher += ' '
            
            else: 
                decipher += list(MORSE_CODE_DICT.keys())[list(MORSE_CODE_DICT.values()).index(citext)] 
                citext = '' 
  
    return decipher 

inp = ".... .. --..-- / - .... .- -. -.- ... / - --- / ... .- -- ..- . .-.. / -- --- .-. ... . / - .... . / - .-. .- -. ... -- .. ... ... .. --- -. / --- ..-. / - . .-.. . --. .-. .- .--. .... .. -.-. / .. -. ..-. --- .-. -- .- - .. --- -. / .-- .- ... / ... - .- -. -.. .- .-. -.. .. --.. . -.. .-.-.- / .... . / ..- ... . -.. / -.. --- - ... / .- -. -.. / -.. .- ... .... . ... / - --- / -.-. .-. . .- - . / .- / ... - .- -. -.. .- .-. -.. / .-- .- -.-- / --- ..-. / -.-. --- -- -- ..- -. .. -.-. .- - .. --- -. --..-- / .... . / .... .- ... / .... . .-.. .--. . -.. / -.-- --- ..- / - --- -.. .- -.-- / - --- / --. . - / - .... . / .--. .- ... ... ---... / - .... .- -. -.- -.-- --- ..- ... .. .-.".split(' / ')

for i in inp:
    print(morseDecrypt(i), end = " ")
```



**RESULT**

<img width="502" alt="Screen Shot 2019-09-25 at 1 26 26 PM" src="https://user-images.githubusercontent.com/16417991/65599343-ef59a580-df9d-11e9-9347-9c6a7bf1b93c.png">



**COMMENT**

This is Morse Code separated with '/'



-----

### LEVEL 4

<img width="554" alt="Screen Shot 2019-09-25 at 1 26 54 PM" src="https://user-images.githubusercontent.com/16417991/65599345-ef59a580-df9d-11e9-8997-32bfd894d9b5.png">



**CODE**

```python3
# Crypt 4
# https://quipqiup.com/
```



**RESULT**

<img width="722" alt="Screen Shot 2019-09-25 at 1 59 20 PM" src="https://user-images.githubusercontent.com/16417991/65599346-eff23c00-df9d-11e9-97c7-da7995694cdf.png">



<img width="616" alt="Screen Shot 2019-09-25 at 1 59 31 PM" src="https://user-images.githubusercontent.com/16417991/65599347-eff23c00-df9d-11e9-8486-12ee6527484e.png">



**COMMENT**

Pattern 'pass: something' is known. So we know clues:  J=P, h=a, l=s



-----

### LEVEL 5

<img width="555" alt="Screen Shot 2019-09-25 at 2 01 01 PM" src="https://user-images.githubusercontent.com/16417991/65600429-62641b80-dfa0-11e9-85a2-538b29036d20.png">



**CODE**

```python3
# Crypt 5
inp = "qoymlNlpY :ccdf lpy yzJ .qoh ln lxigqoh qlxlm eeiw zot ydpy gmipylnoC ,zot gmiyqdncyzo ho ydpy ci lniqk tN .lsie sooe tlpy ydpw yom ,smipy amd tdc tlpy ydpw tj lefolf gmigazb ho ydpy ci lniqk tN .tyicoiqzk ho ydpy ci lniqk tN .edminiqk d nd i clT"[::-1]
print(inp)
# https://quipqiup.com/
```



**RESULT**

<img width="490" alt="Screen Shot 2019-09-25 at 2 01 43 PM" src="https://user-images.githubusercontent.com/16417991/65600430-62641b80-dfa0-11e9-9c39-e8dd9c947ab6.png">

Reverse because you can see capital letters are in the end of words 
Put this result to quipquip.



<img width="646" alt="Screen Shot 2019-09-25 at 2 02 27 PM" src="https://user-images.githubusercontent.com/16417991/65600431-62fcb200-dfa0-11e9-880e-774a034d91b2.png">



<img width="563" alt="Screen Shot 2019-09-25 at 2 04 09 PM" src="https://user-images.githubusercontent.com/16417991/65600432-62fcb200-dfa0-11e9-9c19-c4ca0421c066.png">



**COMMENT**

Priority Number is 1 not 0. Be careful.
