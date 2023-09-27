# Glitch Cat
# Objetivos
¡Nuestro servicio de impresión de banderas ha comenzado a fallar!`$ nc saturn.picoctf.net 52682`

# Solucion
```bash
james-backster-picoctf@webshell:~$ nc saturn.picoctf.net 52682            
'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'

james-backster-picoctf@webshell:~$ python -c "print('picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + "}")"
  File "<string>", line 1
    print('picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + })
                                                                                                                                     ^
SyntaxError: closing parenthesis '}' does not match opening parenthesis '('
james-backster-picoctf@webshell:~$ python -c "print('picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}')"
picoCTF{gl17ch_m3_n07_bda68f75}
james-backster-picoctf@webshell:~$ 
```

# Notas adicionales


# Referencias
