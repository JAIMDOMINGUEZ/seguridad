# Wave a flag
# Objetivos
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm) has extraordinarily helpful information...

# Solucion
```bash
james-backster-picoctf@webshell:~$ ./warm -h                                         
-bash: ./warm: Permission denied
james-backster-picoctf@webshell:~$ chmod +x warm
james-backster-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_30e77291}
```

# Notas adicionales
|Comando|Descripcion|
|---|---|
|-h|Se utiliza para mostrar la ayuda|
# Referencias
