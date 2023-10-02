#  First Find
# Objetivos
Unzip this archive and find the file named 'uber-secret.txt'

# Solucion
```bash
james-backster-picoctf@webshell:~$ unzip files.zip
james-backster-picoctf@webshell:~$ ls
files  files.zip
james-backster-picoctf@webshell:~$ cd files/
james-backster-picoctf@webshell:~/files$ find -name uber-secret.txt
./adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
james-backster-picoctf@webshell:~/files$ cd adequate_books/more_books/.secret/deeper_secrets/deepest_secrets
james-backster-picoctf@webshell:~/files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets$ ls
uber-secret.txt
james-backster-picoctf@webshell:~/files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets$ cat uber-secret.txt 
picoCTF{f1nd_15_f457_ab443fd1}
james-backster-picoctf@webshell:~/files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets$ 
```

# Notas adicionales

# Referencias
