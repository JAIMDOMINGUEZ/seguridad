# SQL Direct
# Objetivos
Connect to this PostgreSQL server and find the flag!

Additional details will be available after launching your challenge instance.
# Solucion
```bash
┌──(kali㉿kali)-[~]
└─$ psql -h saturn.picoctf.net -p 49831 -U postgres pico

Password for user postgres: 
psql (15.3 (Debian 15.3-0+deb12u1), server 15.2 (Debian 15.2-1.pgdg110+1))
Type "help" for help.

pico=#  \dt
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico=#  \dt+
                                   List of relations
 Schema | Name  | Type  |  Owner   | Persistence | Access method | Size  | Description 
--------+-------+-------+----------+-------------+---------------+-------+-------------
 public | flags | table | postgres | permanent   | heap          | 16 kB | 
(1 row)

pico=# SELECT * FROM flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_73b0678f}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

pico=# 


```

# Notas adicionales


# Referencias
https://www.postgresql.org/docs/8.3/app-psql.html