#  HashingJobApp
# Objetivos
If you want to hash with the best, beat this test!`nc saturn.picoctf.net 53638`

# Solucion
```bash
james-backster-picoctf@webshell:~$ nc saturn.picoctf.net 53638
Please md5 hash the text between quotes, excluding the quotes: 'bull fight'
Answer: 
Time's up. Press Ctrl-C to disconnect. Feel free to reconnect and try again.
^C
james-backster-picoctf@webshell:~$ nc saturn.picoctf.net 53638
Please md5 hash the text between quotes, excluding the quotes: 'Al Pacino'
Answer: 
1c9909508d984c65fb3a2f3b28d27faf
1c9909508d984c65fb3a2f3b28d27faf
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'Joan of Arc'
Answer: 
19ba425a542946fcf13228d9ddd53139
19ba425a542946fcf13228d9ddd53139
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'cold pizza'
Answer: 
da910b97223f1dc73b65038d744b5e3c
da910b97223f1dc73b65038d744b5e3c
Correct.
picoCTF{4ppl1c4710n_r3c31v3d_bf2ceb02}
```

# Notas adicionales
El cálculo del valor hash es una técnica comúnmente utilizada en informática para convertir datos, como cadenas de texto, en un valor numérico fijo de longitud fija.
# Referencias
https://www.topster.es/texto/hash_wert.html