# Bandit Level 14 → Level 15

# Objetivos
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.
# Datos de acceso al nivel
```bach
bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
```
# Solucion
```bash
andit14@bandit:~$ nc -v localhost -p 30000
usage: nc [-46CDdFhklNnrStUuvZz] [-I length] [-i interval] [-M ttl]
          [-m minttl] [-O length] [-P proxy_username] [-p source_port]
          [-q seconds] [-s sourceaddr] [-T keyword] [-V rtable] [-W recvlimit]
          [-w timeout] [-X proxy_protocol] [-x proxy_address[:port]]
          [destination] [port]
bandit14@bandit:~$ nc -v localhost  30000
Connection to localhost (127.0.0.1) 30000 port [tcp/*] succeeded!
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt


```


# Notas adicionales
|Comando|Descripcion|
|---|---|
|nc | Netcat es una utilidad de red que permite la transferencia de datos a través de conexiones de red utilizando el protocolo TCP o UDP. La abreviatura "nc" proviene de "netcat", y es comúnmente utilizada para hacer referencia a esta herramienta en línea de comandos
. 

# Referencias
