# strings it
# Objetivos
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings) without running it?

# Solucion
```bash
james-backster-picoctf@webshell:~$ ls
strings
james-backster-picoctf@webshell:~$ strings strings | grep 'pico{'
james-backster-picoctf@webshell:~$ strings strings | grep 'pico'
picoCTF{5tRIng5_1T_7f766a23}
james-backster-picoctf@webshell:~$ 
```

# Notas adicionales


# Referencias
