# Bandit Level 3 → Level 4
# Objetivos
La contraseña para el siguiente nivel se almacena en un archivo oculto en el **aquí** directorio.
# Datos de acceso al nivel
```bach
bandit3
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```
# Solucion
```bash
bandit3@bandit:~$ ls -a
.  ..  .bash_logout  .bashrc  inhere  .profile
bandit3@bandit:~$ ls -l
total 4
drwxr-xr-x 2 root root 4096 Apr 23 18:04 inhere
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -a
.  ..  .hidden
bandit3@bandit:~/inhere$ cat .
cat: .: Is a directory
bandit3@bandit:~/inhere$ ls -a
.  ..  .hidden
bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
bandit3@bandit:~/inhere$
```

# Notas adicionales
|Comando|Descripcion|
|---|---|
|ls -a|lista los archivos ocultos del directorio actual|
|
# Referencias