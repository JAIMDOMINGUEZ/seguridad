#  plumbing
# Objetivos
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 4427`.

# Solucion
```bash
james-backster-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 4427 >> bandera.txt

james-backster-picoctf@webshell:~$ ls
README.txt  bandera.txt
james-backster-picoctf@webshell:~$ cat bandera.txt  
...
james-backster-picoctf@webshell:~$ grep pico bandera.txt 
picoCTF{digital_plumb3r_5ea1fbd7}
 
```

# Notas adicionales

# Referencias
