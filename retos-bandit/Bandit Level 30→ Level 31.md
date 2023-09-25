# Bandit Level 30→ Level 31

# Objetivos
There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo` via the port `2220`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

Clone the repository and find the password for the next level.

# Datos de acceso al nivel
```bach
bandit30
xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS
```
# Solución
```bash
bandit30@bandit:/tmp/tmp.KEzGi/repo$ cat README.md
just an epmty file... muahaha
bandit30@bandit:/tmp/tmp.KEzGi/repo$ ls -la
total 16
drwxrwxr-x 3 bandit30 bandit30 4096 Sep 25 03:22 .
drwx------ 3 bandit30 bandit30 4096 Sep 25 03:22 ..
drwxrwxr-x 8 bandit30 bandit30 4096 Sep 25 03:22 .git
-rw-rw-r-- 1 bandit30 bandit30   30 Sep 25 03:22 README.md
bandit30@bandit:/tmp/tmp.KEzGi/repo$ git log
commit 59530d30d299ff2e3e9719c096ebf46a65cc1424 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Sun Apr 23 18:04:42 2023 +0000

    initial commit of README.md
bandit30@bandit:/tmp/tmp.KEzGi/repo$ git checkout 59530d30d299ff2e3e9719c096ebf46a65cc1424
Note: switching to '59530d30d299ff2e3e9719c096ebf46a65cc1424'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 59530d3 initial commit of README.md
bandit30@bandit:/tmp/tmp.KEzGi/repo$ git branch
* (HEAD detached at 59530d3)
  master
bandit30@bandit:/tmp/tmp.KEzGi/repo$ git branch master
fatal: A branch named 'master' already exists.
bandit30@bandit:/tmp/tmp.KEzGi/repo$ git log
commit 59530d30d299ff2e3e9719c096ebf46a65cc1424 (HEAD, origin/master, origin/HEAD, master)
Author: Ben Dover <noone@overthewire.org>
Date:   Sun Apr 23 18:04:42 2023 +0000

    initial commit of README.md
bandit30@bandit:/tmp/tmp.KEzGi/repo$ cat README.md
just an epmty file... muahaha
bandit30@bandit:/tmp/tmp.KEzGi/repo$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
bandit30@bandit:/tmp/tmp.KEzGi/repo$ git tag
secret
bandit30@bandit:/tmp/tmp.KEzGi/repo$ git show secret
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
bandit30@bandit:/tmp/tmp.KEzGi/repo$

```


# Notas adicionales
|Comando|Descripcion|
|---|---|
|git log |muestra el registro de commits de Git en el repositorio clonado. Cada entrada en el registro de commits muestra información sobre el autor, la fecha y la descripción del commit..
|cat|muestra el contenido de un archivo|
|git show|Es un comando utilizado en Git, para mostrar información detallada sobre un commit específico. 
|git tag|Es un comando utilizado en Git para administrar etiquetas (tags). Las etiquetas son referencias estáticas a puntos específicos en la historia de un repositorio Git

# Referencias

