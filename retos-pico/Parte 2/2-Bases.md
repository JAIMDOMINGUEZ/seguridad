#  Bases
# Objetivos
What does this `bDNhcm5fdGgzX3IwcDM1` mean? I think it has something to do with bases.

# Solucion
```bash
james-backster-picoctf@webshell:~$ python
Python 3.10.6 (main, Aug 10 2022, 11:40:04) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print(int(4, 2))
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: int() can't convert non-string with explicit base
>>> print(int("4", 2))
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: invalid literal for int() with base 2: '4'
>>> print(format(42,'b'))
101010
>>> 
KeyboardInterrupt
>>> 
```

# Notas adicionales
La codificación Base64 es un método comúnmente utilizado para representar datos binarios o cualquier tipo de datos en un formato de texto legible. Se utiliza para asegurarse de que los datos sean transportables a través de protocolos de texto, como el correo electrónico, o almacenados en sistemas que pueden no admitir datos binarios.

# Referencias
