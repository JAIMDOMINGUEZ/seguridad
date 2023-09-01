# Bandit Level 4 → Level 5
# Objetivos
The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.
# Datos de acceso al nivel
```bach
	bandit4
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
```
# Solucion
```bash
bandit4@bandit:~$ file ./*
./inhere: directory
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: Non-ISO extended-ASCII text, with no line terminators
bandit4@bandit:~/inhere$ cat ./-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
bandit4@bandit:~/inhere$
```

# Notas adicionales
|Comando|Descripcion|
|---|---|
|file|se utiliza para mostrar información sobre los tipos de archivos presentes en el directorio actua|
|
# Referencias