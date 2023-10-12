# Irish-Name-Repo 3
# Objetivos
¡Consulta el scratchpad de administrador! `https://jupiter.challenges.picoctf.org/problem/61864/` o http://jupiter.challenges.picoctf.org:61864

# Solucion
```bash
(kali㉿kali)-[~]
└─$ sudo gzip -d /usr/share/wordlists/rockyou.txt.gz 
[sudo] password for kali: 
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ head /usr/share/wordlists/rockyou.txt.gz
head: cannot open '/usr/share/wordlists/rockyou.txt.gz' for reading: No such file or directory
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ head /usr/share/wordlists/rockyou.txt   
123456
12345
123456789
password
iloveyou
princess
1234567
rockyou
12345678
abc123

(kali㉿kali)-[~]
└─$ john hash -w:/usr/share/wordlists/rockyou.txt

Using default input encoding: UTF-8
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 256/256 AVX2 8x])
Will run 2 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
ilovepico        (?)     
1g 0:00:00:02 DONE (2023-10-12 00:49) 0.3676g/s 2719Kp/s 2719Kc/s 2719KC/s iloverob4live345..ilovemymother@
Use the "--show" option to display all of the cracked passwords reliably
Session completed. 

```
![[Pasted image 20231011230107.png]]
# Notas adicionales
## ¿Qué es JSON Web Token?

JSON Web Token (JWT) es un estándar abierto ([RFC 7519](https://tools.ietf.org/html/rfc7519)) que define una forma compacta y autónoma para transmitir información de forma segura entre partes como un objeto JSON. Esta información se puede verificar y confiar porque está firmada digitalmente.

# Referencias
https://jwt.io/introduction