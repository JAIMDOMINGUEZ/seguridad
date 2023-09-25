# Bandit Level 31→ Level 32

# Objetivos
Hay un repositorio git en `ssh://bandit31-git@localhost/home/bandit31-git/repo` a través del puerto `2220`. La contraseña para el usuario `bandit31-git` es lo mismo que para el usuario `bandit31`.

Clone el repositorio y busque la contraseña para el siguiente nivel.
# Datos de acceso al nivel
```bach
bandit31
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
```
# Solución
```bash
bandit31@bandit:/tmp/tmp.PiNxz$ cd repo
bandit31@bandit:/tmp/tmp.PiNxz/repo$ ls -la
total 20
drwxrwxr-x 3 bandit31 bandit31 4096 Sep 25 03:32 .
drwx------ 3 bandit31 bandit31 4096 Sep 25 03:32 ..
drwxrwxr-x 8 bandit31 bandit31 4096 Sep 25 03:32 .git
-rw-rw-r-- 1 bandit31 bandit31    6 Sep 25 03:32 .gitignore
-rw-rw-r-- 1 bandit31 bandit31  147 Sep 25 03:32 README.md
bandit31@bandit:/tmp/tmp.PiNxz/repo$ cat README.md
This time your task is to push a file to the remote repository.

Details:
    File name: key.txt
    Content: 'May I come in?'
    Branch: master

bandit31@bandit:/tmp/tmp.PiNxz/repo$ rm .gitignore
bandit31@bandit:/tmp/tmp.PiNxz/repo$ echo 'May I come in?' > key.txt
bandit31@bandit:/tmp/tmp.PiNxz/repo$ cta key.txt
Command 'cta' not found, did you mean:
  command 'cat' from deb coreutils (8.32-4.1ubuntu1)
  command 'ctr' from deb containerd (1.6.12-0ubuntu1~22.04.1)
  command 'cba' from deb cba (0.3.6-5build1)
  command 'sta' from deb opensta (0~20191111gitc018cb2+dfsg-1build1)
  command 'eta' from deb eta (1.0.1-1)
Try: apt install <deb name>
bandit31@bandit:/tmp/tmp.PiNxz/repo$ cat key.txt
May I come in?
bandit31@bandit:/tmp/tmp.PiNxz/repo$ git add key.txt
bandit31@bandit:/tmp/tmp.PiNxz/repo$ git commit -m "pa arriba"
[master c71bfa0] pa arriba
 1 file changed, 1 insertion(+)
 create mode 100644 key.txt
bandit31@bandit:/tmp/tmp.PiNxz/repo$ git push
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit31-git@localhost's password:
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 320 bytes | 320.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: ### Attempting to validate files... ####
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
remote: Well done! Here is the password for the next level:
remote: rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
To ssh://localhost:2220/home/bandit31-git/repo
 ! [remote rejected] master -> master (pre-receive hook declined)
error: failed to push some refs to 'ssh://localhost:2220/home/bandit31-git/repo'

```


# Notas adicionales
|Comando|Descripcion|
|---|---|
|git log |muestra el registro de commits de Git en el repositorio clonado. Cada entrada en el registro de commits muestra información sobre el autor, la fecha y la descripción del commit..
|cat|muestra el contenido de un archivo|
|git show|Es un comando utilizado en Git, para mostrar información detallada sobre un commit específico. 
|git tag|Es un comando utilizado en Git para administrar etiquetas (tags). Las etiquetas son referencias estáticas a puntos específicos en la historia de un repositorio Git

# Referencias

