# what's a net cat?
# Objetivos
Using netcat (nc) is going to be pretty important. Can you connect to `jupiter.challenges.picoctf.org` at port `41120` to get the flag?

# Solucion
```bash
james-backster-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org -p 41120 
usage: nc [-46CDdFhklNnrStUuvZz] [-I length] [-i interval] [-M ttl]
          [-m minttl] [-O length] [-P proxy_username] [-p source_port]
          [-q seconds] [-s sourceaddr] [-T keyword] [-V rtable] [-W recvlimit]
          [-w timeout] [-X proxy_protocol] [-x proxy_address[:port]]
          [destination] [port]
james-backster-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org:41120 
nc: missing port number
james-backster-picoctf@webshell:~$ nc -v jupiter.challenges.picoctf.org -p 41120 
usage: nc [-46CDdFhklNnrStUuvZz] [-I length] [-i interval] [-M ttl]
          [-m minttl] [-O length] [-P proxy_username] [-p source_port]
          [-q seconds] [-s sourceaddr] [-T keyword] [-V rtable] [-W recvlimit]
          [-w timeout] [-X proxy_protocol] [-x proxy_address[:port]]
          [destination] [port]
james-backster-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 41120 
You're on your way to becoming the net cat master
picoCTF{nEtCat_Mast3ry_3214be47}

```

# Notas adicionales


# Referencias
