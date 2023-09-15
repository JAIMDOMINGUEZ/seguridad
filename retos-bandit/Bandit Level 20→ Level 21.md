# Bandit Level 20→ Level 21

# Objetivos
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

**NOTE:** Try connecting to your own network daemon to see if it works as you think

# Datos de acceso al nivel
```bach
bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
```
# Solución
```bash
bandit20@bandit:~$ nc -lnvp 2020 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
[1] 3771442
bandit20@bandit:~$ Listening on 0.0.0.0 2020
./suconnect 2020
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
bandit20@bandit:~$
```


# Notas adicionales
|Comando|Descripcion|
|---|---|
|nc | Netcat es una utilidad de red que permite la transferencia de datos a través de conexiones de red utilizando el protocolo TCP o UDP. La abreviatura "nc" proviene de "netcat", y es comúnmente utilizada para hacer referencia a esta herramienta en línea de comandos



# Referencias
