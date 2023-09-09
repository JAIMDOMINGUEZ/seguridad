# Bandit Level 11 → Level 12

# Objetivos
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data
# Datos de acceso al nivel
```bach
bandit11
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```
# Solucion
```bash
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt | tr [d-zabc] [a-z] | tr [D-ZABC] [A-Z]
Dro zkccgybn sc TFXLLPCwJgUUYZ0HlPHYyG8mrNj5iFBf
bandit11@bandit:~$ cat data.txt | tr [a-zA-Z] [n-za-mN-ZA-M]
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
bandit11@bandit:~$

```

# Notas adicionales
|Comando|Descripcion|
|---|---|
|tr | Con el comando **tr** realizamos una sustitución carácter a carácter.|

# Referencias
