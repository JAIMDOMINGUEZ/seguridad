# reverse_cipher
# Objetivos
We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev_this). Can you reverse the flag.
# Solucion
![[Pasted image 20231114220149.png]]
```bash
ifrado = open("rev_this","r").read()
bandera= ""
for i in range(8, len(cifrado)-1):
        if i & 1 ==0:
                bandera+= chr(ord(cifrado[i]) - 5)
        else:
                bandera += chr(ord(cifrado[i]) +2)
print(bandera)
──(kali㉿kali)-[~/Documents/reversing/reverse_cipher]
└─$ python rv.py
r3v3rs312528e05

```

# Notas adicionales

# Referencias
https://www.youtube.com/watch?v=bDKFnIEmyOA