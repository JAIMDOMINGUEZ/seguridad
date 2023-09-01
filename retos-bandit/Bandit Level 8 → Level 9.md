# Bandit Level 8 → Level 9
# Objetivos
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once
# Datos de acceso al nivel
```bach
bandit8
TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```
# Solucion
```bash

bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
bandit8@bandit:~$
```

# Notas adicionales
|Comando|Descripcion|
|---|---|
|grep |Es unaherramienta  que se utiliza para buscar patrones de texto dentro de archivos o en la salida de otros comandos.  
| sort | Este comando toma la salida del comando anterior y lo ordena alfabéticamente o numéricamente|
| uniq -u| Se utiliza para eliminar líneas duplicadas adyacentes en su entrada. Con la opción "-u", se le indica a "uniq" que solo muestre las líneas que aparecen una sola vez en la entrada.|
# Referencias