# Bandit Level 1 → Level 2

# Objetivos
The password for the next level is stored in a file called **-** located in the home directory
# Datos de acceso al nivel
```bach
bandit1
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```
# Solucion
```bash
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$
```

# Notas adicionales
|Comando|Descripcion|
|---|---|
|ls|lista los archivos del directorio actual|
|whoami|saber el usuario actual|
|cat ./|cuando un archivo inicia con - podemos utilizar el comando para acceder ael|
# Referencias