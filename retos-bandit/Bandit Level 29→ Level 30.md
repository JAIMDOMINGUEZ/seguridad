# Bandit Level 29→ Level 30

# Objetivos
There is a git repository at `ssh://bandit29-git@localhost/home/bandit29-git/repo` via the port `2220`. The password for the user `bandit29-git` is the same as for the user `bandit29`.

Clone the repository and find the password for the next level.

# Datos de acceso al nivel
```bach
bandit29
tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
```
# Solución
```bash
bandit29@bandit:/tmp/tmp.kAWnrr$ cd repo
bandit29@bandit:/tmp/tmp.kAWnrr/repo$ ls
README.md
bandit29@bandit:/tmp/tmp.kAWnrr/repo$ cat Readme
cat: Readme: No such file or directory
bandit29@bandit:/tmp/tmp.kAWnrr/repo$ cat Readme.md
cat: Readme.md: No such file or directory
bandit29@bandit:/tmp/tmp.kAWnrr/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: <no passwords in production!>

bandit29@bandit:/tmp/tmp.kAWnrr/repo$ GIT LOG
GIT: command not found
bandit29@bandit:/tmp/tmp.kAWnrr/repo$ git log
commit 4bd5389f9f2b9e96ba517aa751ee58d051905761 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Sun Apr 23 18:04:40 2023 +0000

    fix username

commit 1a57cf10158f133c4f40ff82251f605a7618631d
Author: Ben Dover <noone@overthewire.org>
Date:   Sun Apr 23 18:04:40 2023 +0000

    initial commit of README.md
bandit29@bandit:/tmp/tmp.kAWnrr/repo$ git branch
* master
bandit29@bandit:/tmp/tmp.kAWnrr/repo$ git branch -r
  origin/HEAD -> origin/master
  origin/dev
  origin/master
  origin/sploits-dev
bandit29@bandit:/tmp/tmp.kAWnrr/repo$ git log
commit 4bd5389f9f2b9e96ba517aa751ee58d051905761 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Sun Apr 23 18:04:40 2023 +0000

    fix username

commit 1a57cf10158f133c4f40ff82251f605a7618631d
Author: Ben Dover <noone@overthewire.org>
Date:   Sun Apr 23 18:04:40 2023 +0000

    initial commit of README.md
bandit29@bandit:/tmp/tmp.kAWnrr/repo$ git checkout dev
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
Switched to a new branch 'dev'
bandit29@bandit:/tmp/tmp.kAWnrr/repo$ git log
commit 13e735685c73e5e396252074f2dca2e415fbcc98 (HEAD -> dev, origin/dev)
Author: Morla Porla <morla@overthewire.org>
Date:   Sun Apr 23 18:04:40 2023 +0000

    add data needed for development

commit 8caf551dba9f9e39bc8ea4163de7902e6fa85f3a
Author: Ben Dover <noone@overthewire.org>
Date:   Sun Apr 23 18:04:40 2023 +0000

    add gif2ascii

commit 4bd5389f9f2b9e96ba517aa751ee58d051905761 (origin/master, origin/HEAD, master)
Author: Ben Dover <noone@overthewire.org>
Date:   Sun Apr 23 18:04:40 2023 +0000

    fix username

commit 1a57cf10158f133c4f40ff82251f605a7618631d
Author: Ben Dover <noone@overthewire.org>
Date:   Sun Apr 23 18:04:40 2023 +0000

    initial commit of README.md
bandit29@bandit:/tmp/tmp.kAWnrr/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS

bandit29@bandit:/tmp/tmp.kAWnrr/repo$


```


# Notas adicionales
|Comando|Descripcion|
|---|---|
|git log |muestra el registro de commits de Git en el repositorio clonado. Cada entrada en el registro de commits muestra información sobre el autor, la fecha y la descripción del commit..
|cat|muestra el contenido de un archivo|
|git checkout|es un comando fundamental en Git,para cambiar de una rama a otra en tu repositorio Git|

# Referencias
