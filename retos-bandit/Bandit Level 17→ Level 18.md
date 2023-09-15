# Bandit Level 17→ Level 18

# Objetivos
There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**

**NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19**

# Datos de acceso al nivel
```bach
bandit17  
llave.txt
```
# Solucion
```bash
bandit17@bandit:~$ diff passwords.old passwords.new
42c42
< glZreTEH1V3cGKL6g4conYqZqaEj0mte
---
> hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg

```


# Notas adicionales
|Comando|Descripcion|
|---|---|
|diff | El comando `diff` en Linux se utiliza para comparar el contenido de dos archivos línea por línea y mostrar las diferencias entre ellos.


# Referencias
