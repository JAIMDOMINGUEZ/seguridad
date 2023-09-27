# Obedient Cat
# Objetivos
This file has a flag in plain sight (aka "in-the-clear").

# Solucion
```bash
james-backster-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag
--2023-09-26 20:46:21--  https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: 'flag'

flag                                                       100%[=======================================================================================================================================>]      34  --.-KB/s    in 0s      

2023-09-26 20:46:22 (14.1 MB/s) - 'flag' saved [34/34]

james-backster-picoctf@webshell:~$ cat flag
picoCTF{s4n1ty_v3r1f13d_2aa22101}
james-backster-picoctf@webshell:~$ 
```

# Notas adicionales

# Referencias
