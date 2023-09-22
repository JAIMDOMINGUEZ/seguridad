# Bandit Level 22→ Level 23

# Objetivos
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

# Datos de acceso al nivel
```bach
bandit22
WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff
```
# Solución
```bash
bandit22@bandit:~$ echo I am user $myname
I am user
bandit22@bandit:~$ myname=$(bandit23)
bandit23: command not found
bandit22@bandit:~$ myname=$(whoami)
bandit22@bandit:~$ echo $myname
bandit22
bandit22@bandit:~$ echo I am user $myname
I am user bandit22
bandit22@bandit:~$ echo I am user $myname | md5sum
8169b67bd894ddbb4412f91573b38db3  -
bandit22@bandit:~$ echo I am user $myname | md5sum | cut -d ´ ´ -f 1
cut: the delimiter must be a single character
Try 'cut --help' for more information.
bandit22@bandit:~$ echo I am user $myname | md5sum | cut -d ' ' -f 1
8169b67bd894ddbb4412f91573b38db3
bandit22@bandit:~$ echo I am user $myname | md5sum | cut -d ' ' -f 1
8169b67bd894ddbb4412f91573b38db3
bandit22@bandit:~$ echo I am user $myname | md5sum | cut -d ' ' -f 1
8169b67bd894ddbb4412f91573b38db3
bandit22@bandit:~$ my name=bandit23
my: command not found
bandit22@bandit:~$ myname=bandit23
bandit22@bandit:~$ echo I am user $myname | md5sum | cut -d ' ' -f 1
8ca319486bfbbc3663ea0fbe81326349
bandit22@bandit:~$ cat /tmp/8ca319486bfbbc3663ea0fbe81326349
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
bandit22@bandit:~$
```


# Notas adicionales
|Comando|Descripcion|
|---|---|
|Cron | Es un administrador de tareas en sistemas operativos Unix , incluyendo Linux. Permite a los usuarios programar la ejecución de comandos o scripts en un momento específico o en intervalos regulares.



# Referencias
