# Bandit Level 12 → Level 13

# Objetivos
La contraseña para el siguiente nivel se almacena en el archivo **data.txt**, que es un hexdump de un archivo que se ha comprimido repetidamente. Para este nivel puede ser útil crear un directorio bajo / tmp en que puedes trabajar usando mkdir. Por ejemplo: mkdir / tmp / myname123. Luego copie el archivo de datos usando cp y cambie el nombre usando mv ( lea el manpages! )
# Datos de acceso al nivel
```bach
bandit12
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
```
# Solucion
```bash
bandit12@bandit:~$ sudo apt install 7z
sudo: /usr/bin/sudo must be owned by uid 0 and have the setuid bit set
bandit12@bandit:~$ xxd -r data.txt | file -
xxd -r data.txt | zcat | bzcat |file -
xxd -r data.txt | zcat | bzcat | zcat |file -
xxd -r data.txt | zcat | bzcat | zcat | tar xO | file -
xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | file -
xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat |file -
xxd -r data.txt | zcat | bzcat | zcat/dev/stdin: gzip compressed data, was "data2.bin", last modified: Sun Apr 23 18:04:23 2023, max compression, from Unix
 | tar xO | tar xO | bzcat | tbandit12@bandit:~$ xxd -r data.txt | zcat |file -
ar xO | file -
xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat | file -
xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat/dev/stdin: bzip2 compressed data, block size = 900k
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat |file -
/dev/stdin: gzip compressed data, was "data4.bin", last modified: Sun Apr 23 18:04:23 2023, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat |file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | file -
/dev/stdin: bzip2 compressed data, block size = 900k
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat |file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | file -
/dev/stdin: gzip compressed data, was "data9.bin", last modified: Sun Apr 23 18:04:23 2023, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat | file -
/dev/stdin: ASCII text
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
bandit12@bandit:~$

```


# Notas adicionales
|Comando|Descripcion|
|---|---|
|tar |El comando `tar`, que significa "tape archive", se utiliza en sistemas Unix y Linux para crear y manipular archivos de archivo. Puede comprimir varios archivos y directorios en un solo archivo de archivo o extraer archivos de un archivo de archivo existente.  
| gzip | El comando `gzip` se utiliza para comprimir archivos en sistemas Unix y Linux. Puede comprimir un solo archivo y reemplazarlo con una versión comprimida o crear un archivo comprimido nuevo.|
| bzcat | El comando `bzcat` se utiliza para mostrar el contenido de archivos comprimidos en formato Bzip|
| xxd | El comando `xxd` se utiliza para crear una representación hexadecimal (y textual) de un archivo binario.|
| zcat | El comando `zcat` se utiliza para mostrar el contenido de archivos comprimidos en formato gzip sin tener que descomprimirlos manualmente.|


# Referencias
