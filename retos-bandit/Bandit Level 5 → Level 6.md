# Bandit Level 5 → Level 6
# Objetivos
The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.
# Datos de acceso al nivel
```bach
	bandit5
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```
# Solucion
```bash
./maybehere05: directory
./maybehere06: directory
./maybehere07: directory
./maybehere08: directory
./maybehere09: directory
./maybehere10: directory
./maybehere11: directory
./maybehere12: directory
./maybehere13: directory
./maybehere14: directory
./maybehere15: directory
./maybehere16: directory
./maybehere17: directory
./maybehere18: directory
./maybehere19: directory
bandit5@bandit:~/inhere$ find . -redeable -type f -size 1033c
find: unknown predicate `-redeable'
bandit5@bandit:~/inhere$ find . -redable -type f -size 1033c
find: unknown predicate `-redable'
bandit5@bandit:~/inhere$ find . -readable -type f -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```

# Notas adicionales
|Comando|Descripcion|
|---|---|
|find . -readable -type f -size 1033c |El comando busca archivos que sean legibles, tengan un tipo de archivo de "archivo regular" y tengan un tamaño de exactamente 1033 bytes. El indicador `-readable` asegura que solo se consideren archivos con permisos de lectura.|
|
# Referencias