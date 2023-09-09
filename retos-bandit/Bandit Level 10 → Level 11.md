# Bandit Level 10 → Level 11

# Objetivos
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data
# Datos de acceso al nivel
```bach
bandit10
G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```
# Solucion
```bash
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ echo data.txt | base64 decode
base64: decode: No such file or directory
bandit10@bandit:~$ echo data.txt | base64 -decode
base64: invalid option -- 'e'
Try 'base64 --help' for more information.
bandit10@bandit:~$ cat data.txt | base64 -decode
base64: invalid option -- 'e'
Try 'base64 --help' for more information.
bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

```

# Notas adicionales
|Comando|Descripcion|
|---|---|
|base64 |Para codificar o decodificar entrada / salida estándar o cualquier contenido de archivo, Linux utiliza el sistema de codificación y decodificación base64  
| -d or –decode | Esta opción se usa para decodificar cualquier dato codificado de entrada estándar o de cualquier archivo.|

# Referencias
https://linuxhint.com/bash_base64_encode_decode/