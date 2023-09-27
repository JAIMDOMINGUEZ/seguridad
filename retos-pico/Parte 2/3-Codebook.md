# Codebook
# Objetivos
Run the Python script `code.py` in the same directory as `codebook.txt`.

# Solucion
```bash
james-backster-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/3/code.py
--2023-09-27 04:14:45--  https://artifacts.picoctf.net/c/3/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.42, 3.160.5.93, 3.160.5.71, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.42|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py'

code.py                                    100%[======================================================================================>]   1.25K  --.-KB/s    in 0s      

2023-09-27 04:14:45 (523 MB/s) - 'code.py' saved [1278/1278]

james-backster-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/3/codebook.txt
--2023-09-27 04:15:47--  https://artifacts.picoctf.net/c/3/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.93, 3.160.5.71, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt                               100%[======================================================================================>]      27  --.-KB/s    in 0s      

2023-09-27 04:15:47 (7.90 MB/s) - 'codebook.txt' saved [27/27]

james-backster-picoctf@webshell:~$ ls
README.txt  code.py  codebook.txt  flag  warm
james-backster-picoctf@webshell:~$ python code.py 
picoCTF{c0d3b00k_455157_197a982c}
james-backster-picoctf@webshell:~$ 

```

# Notas adicionales


# Referencias
