# fixme2.py
# Objetivos
Solucione el error de sintaxis en el script de Python para imprimir el indicador.

# Solucion
```bash
james-backster-picoctf@webshell:~$ python fixme2.py 
  File "/home/james-backster-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
james-backster-picoctf@webshell:~$ nano fixme2.py 
james-backster-picoctf@webshell:~$ python fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}
james-backster-picoctf@webshell:~$ 

```

# Notas adicionales


# Referencias
