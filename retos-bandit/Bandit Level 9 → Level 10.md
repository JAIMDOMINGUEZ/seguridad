# Bandit Level 9 → Level 10
# Objetivos
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.
# Datos de acceso al nivel
```bach
bandit9
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```
# Solucion
```bash
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ strings data.txt | grep ==
4========== the#
========== password
========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
bandit9@bandit:~$

```

# Notas adicionales
|Comando|Descripcion|
|---|---|
|strings |Este comando extraerá todas las secuencias de caracteres  que encuentre en el archivo  
| pipe | Este símbolo se utiliza para redirigir la salida del comando anterior y usarla como entrada para el siguiente comando.|
| grep| Este comando busca las líneas que contienen el patrón proporcionado|
# Referencias