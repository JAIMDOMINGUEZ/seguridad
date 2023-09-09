# Bandit Level 13 → Level 14

# Objetivos
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. **Note:** **localhost** is a hostname that refers to the machine you are working on
# Datos de acceso al nivel
```bach
bandit13
wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
```
# Solucion
```bash
bandit13@bandit:~$ ssh -i sshkey.private bandit14@localhost -p 2220
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
bandit14@bandit:~$ ls
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq

```


# Notas adicionales
|Comando|Descripcion|
|---|---|
|-i | Sirve para indicar que se le va proporcionar una llave  

# Referencias
