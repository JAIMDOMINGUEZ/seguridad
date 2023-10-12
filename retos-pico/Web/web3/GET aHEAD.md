# GET aHEAD
# Objetivos
Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:53554/](http://mercury.picoctf.net:53554/)

# Solucion
```bash
(kali㉿kali)-[~]
└─$ curl -I  http://mercury.picoctf.net:53554/index.php | grep "pico"
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0       0     0    0     0    0     0      0      0 --:--:--  0:00:22 --:--:--     0
flag: picoCTF{r3j3ct_th3_du4l1ty_2e5ba39f}

```

# Notas adicionales
|Comando|Descripcion|
|---|---|
|-I|es la nueva version de -X HEAD utilizando curl|

# Referencias
