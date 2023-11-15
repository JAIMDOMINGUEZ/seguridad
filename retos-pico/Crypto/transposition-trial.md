# transposition-trial
# Objetivos
Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message.Download the corrupted message [here](https://artifacts.picoctf.net/c/192/message.txt).
# Solucion
```bash
  GNU nano 7.2                              rv.py                                        
texto = "heTfl g as iicpCTo{7F4NRP051N51635P3X51N3_V091B0AE}2"
salida = ""
for i in range(2, len(texto), 3):
    salida += texto[i] + texto[i-2] + texto [i-1]
print(salida)

┌──(kali㉿kali)-[~/Documents/crypto/trasnposition-trial]
└─$ python rv.py
The flag is picoCTF{7R4N5P051N31635P1X5_N39V001B}AE

```

# Notas adicionales

# Referencias
