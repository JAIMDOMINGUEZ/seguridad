# Bandit Level 6 → Level 7
# Objetivos
The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size
# Datos de acceso al nivel
```bach
	bandit6
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```
# Solucion
```bash
bandit6@bandit:~$ ls
bandit6@bandit:~$ ls -a
.  ..  .bash_logout  .bashrc  .profile
bandit6@bandit:~$ ls -la
total 20
drwxr-xr-x  2 root root 4096 Apr 23 18:04 .
drwxr-xr-x 70 root root 4096 Apr 23 18:05 ..
-rw-r--r--  1 root root  220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root root 3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root root  807 Jan  6  2022 .profile
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
bandit6@bandit:~$
```

# Notas adicionales
|Comando|Descripcion|
|---|---|
|find |Este es el comando utilizado para buscar archivos y directorios en un sistema
|/ |Este es el punto de partida para la búsqueda.|
|-user | Este es un filtro que busca archivos propiedad del usuario especificado|
| -group| Es filtro que busca archivos que pertenecen al grupo de un usuario|
|-size |Este es un filtro que busca archivos con un tamaño especificado |
# Referencias