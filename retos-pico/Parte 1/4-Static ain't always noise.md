#  Static ain't always noise
# Objetivos
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/7495259e963bd5b67d0fb8b616652618/static)? This [BASH script](https://mercury.picoctf.net/static/7495259e963bd5b67d0fb8b616652618/ltdis.sh) might help!

# Solucion
```bash
james-backster-picoctf@webshell:~$ ls -la
total 80
drwxr-xr-x 2 james-backster-picoctf james-backster-picoctf  4096 Sep 25 17:14 .
drwxr-xr-x 3 root                   root                      36 Sep 25 16:29 ..
-rw-r--r-- 1 james-backster-picoctf james-backster-picoctf   220 Sep 25 16:29 .bash_logout
-rw-r--r-- 1 james-backster-picoctf james-backster-picoctf  3771 Sep 25 16:29 .bashrc
-rw-r--r-- 1 james-backster-picoctf james-backster-picoctf   807 Sep 25 16:29 .profile
-rw------- 1 james-backster-picoctf james-backster-picoctf     7 Sep 25 16:54 .python_history
-rw-rw-r-- 1 james-backster-picoctf james-backster-picoctf   167 Sep 25 16:34 .wget-hsts
-rw-r--r-- 1 root                   root                    4443 Sep 25 16:29 README.txt
-rw-rw-r-- 1 james-backster-picoctf james-backster-picoctf  1328 Mar 16  2021 ende.py
-rw-rw-r-- 1 james-backster-picoctf james-backster-picoctf    34 Mar 16  2021 flag
-rw-rw-r-- 1 james-backster-picoctf james-backster-picoctf    34 Mar 16  2021 flag.1
-rw-rw-r-- 1 james-backster-picoctf james-backster-picoctf   140 Mar 16  2021 flag.txt.en
-rw-rw-r-- 1 james-backster-picoctf james-backster-picoctf   785 Mar 16  2021 ltdis.sh
-rw-rw-r-- 1 james-backster-picoctf james-backster-picoctf    33 Mar 16  2021 pw.txt
-rw-rw-r-- 1 james-backster-picoctf james-backster-picoctf  8376 Mar 16  2021 static
-rw-rw-r-- 1 james-backster-picoctf james-backster-picoctf 10936 Mar 16  2021 warm
james-backster-picoctf@webshell:~$ chmod +x static
james-backster-picoctf@webshell:~$  strings static | greep pico
-bash: greep: command not found
james-backster-picoctf@webshell:~$ Strings static | greep pico
-bash: Strings: command not found
-bash: greep: command not found
james-backster-picoctf@webshell:~$ Strings static | Greep pico
-bash: Strings: command not found
-bash: Greep: command not found
james-backster-picoctf@webshell:~$ Strings static | grep pico
-bash: Strings: command not found
james-backster-picoctf@webshell:~$ strings static | grep pico
picoCTF{d15a5m_t34s3r_f6c48608}
james-backster-picoctf@webshell:~$ ^C
james-backster-picoctf@webshell:~$ 

```

# Notas adicionales

# Referencias
https://onlinetools.com/ascii/convert-decimal-to-ascii