# Bandit Level 7 → Level 8
# Objetivos
 The password for the next level is stored in the file **data.txt** next to the word **millionth**
# Datos de acceso al nivel
```bach
	bandit7
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```
# Solucion
```bash
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ wc data.txt
  98567  197133 4184396 data.txt
bandit7@bandit:~$ grep millionth data.txt
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$ cat data.txt | grep millionth
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$
```

# Notas adicionales
|Comando|Descripcion|
|---|---|
|grep |Es unaherramienta  que se utiliza para buscar patrones de texto dentro de archivos o en la salida de otros comandos.  

# Referencias