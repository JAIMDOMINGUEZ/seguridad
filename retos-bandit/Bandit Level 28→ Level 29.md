# Bandit Level 28→ Level 29

# Objetivos
There is a git repository at `ssh://bandit28-git@localhost/home/bandit28-git/repo` via the port `2220`. The password for the user `bandit28-git` is the same as for the user `bandit28`.

Clone the repository and find the password for the next level.

# Datos de acceso al nivel
```bach
bandit28
AVanL161y9rsbcJIsFHuw35rjaOM19nR
```
# Solución
```
bandit28@bandit:~$ cd /tmp/tmp.Ndnskc
bandit28@bandit:/tmp/tmp.Ndnskc$ git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit28/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit28/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit28-git@localhost's password:
remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 9 (delta 2), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (9/9), done.
Resolving deltas: 100% (2/2), done.
bandit28@bandit:/tmp/tmp.Ndnskc$ ls
repo
bandit28@bandit:/tmp/tmp.Ndnskc$ cd repo
bandit28@bandit:/tmp/tmp.Ndnskc/repo$ ls repo
ls: cannot access 'repo': No such file or directory
bandit28@bandit:/tmp/tmp.Ndnskc/repo$ ls -la
total 16
drwxrwxr-x 3 bandit28 bandit28 4096 Sep 24 21:00 .
drwx------ 3 bandit28 bandit28 4096 Sep 24 20:59 ..
drwxrwxr-x 8 bandit28 bandit28 4096 Sep 24 21:00 .git
-rw-rw-r-- 1 bandit28 bandit28  111 Sep 24 21:00 README.md
bandit28@bandit:/tmp/tmp.Ndnskc/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: xxxxxxxxxx

bandit28@bandit:/tmp/tmp.Ndnskc/repo$ git brnach -a
git: 'brnach' is not a git command. See 'git --help'.

The most similar command is
        branch
bandit28@bandit:/tmp/tmp.Ndnskc/repo$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
bandit28@bandit:/tmp/tmp.Ndnskc/repo$ git log
commit 899ba88df296331cc01f30d022c006775d467f28 (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Sun Apr 23 18:04:39 2023 +0000

    fix info leak

commit abcff758fa6343a0d002a1c0add1ad8c71b88534
Author: Morla Porla <morla@overthewire.org>
Date:   Sun Apr 23 18:04:39 2023 +0000

    add missing data

commit c0a8c3cf093fba65f4ee0e1fe2a530b799508c78
Author: Ben Dover <noone@overthewire.org>
Date:   Sun Apr 23 18:04:39 2023 +0000

    initial commit of README.md
bandit28@bandit:/tmp/tmp.Ndnskc/repo$ git diff 899ba88df296331cc01f30d022c006775d467f28 abcff758fa6343a0d002a1c0add1ad8c71b88534 c0a8c3cf093fba65f4ee0e1fe2a530b799508c78
diff --cc README.md
index b302105,7ba2d2f..5c6457b
--- a/README.md
+++ b/README.md
@@@ -4,5 -4,5 +4,5 @@@ Some notes for level29 of bandit
  ## credentials

  - username: bandit29
- - password: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
 -- password: <TBD>
++- password: xxxxxxxxxx

bandit28@bandit:/tmp/tmp.Ndnskc/repo$

```


# Notas adicionales
|Comando|Descripcion|
|---|---|
|git log |muestra el registro de commits de Git en el repositorio clonado. Cada entrada en el registro de commits muestra información sobre el autor, la fecha y la descripción del commit..
|cat|muestra el contenido de un archivo|


# Referencias
