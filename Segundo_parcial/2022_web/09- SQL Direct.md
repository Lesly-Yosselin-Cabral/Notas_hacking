# Descripcion
Connect to this PostgreSQL server and find the flag!

Additional details will be available after launching your challenge instance.

# Pistas
(None)

# Solucion
```
┌──(kali㉿kali)-[~/picoctf/2doparcial/web2022/sqldirect]
└─$ psql -h saturn.picoctf.net -p 62124 -U postgres pico
Password for user postgres: 
psql (13.5 (Debian 13.5-0+deb11u1), server 14.2 (Debian 14.2-1.pgdg110+1))
WARNING: psql major version 13, server major version 14.
         Some psql features might not work.
Type "help" for help.

pico=#
pico=# \dt
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)
pico=#
pico=#
pico=# select * from flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)
picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
```

# Bandera
picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}

# Notas adicionales


# Referencias
[SQL Direct | picoCTF 2022 - YouTube](https://www.youtube.com/watch?v=g5q64M6ZqHw)
