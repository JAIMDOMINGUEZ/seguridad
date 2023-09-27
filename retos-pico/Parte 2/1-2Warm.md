# 2Warm
# Objetivos
Can you convert the number 42 (base 10) to binary (base 2)?

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


# Referencias
