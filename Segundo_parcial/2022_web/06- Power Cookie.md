# Descripcion
Can you get the flag?Go to this [website](http://saturn.picoctf.net:57329/) and see what you can discover.

# Pistas
Do you know how to modify cookies?

# Solucion
```
We apologize, but we have no guest services at the moment.
isAdmin:"0"
isAdmin:"1"
picoCTF{gr4d3_A_c00k13_65fd1e1a}
```

# Bandera
picoCTF{gr4d3_A_c00k13_65fd1e1a}

# Notas adicionales
Para la solución de este reto se accedió al sitio web que se proporciona en la descripción de el reto.
Una vez dentro de ella, luego se abren las herramientas de desarrollador, después nos vamos a la pestaña storage y podemos ver una cookie con nombre isAdmin y de valor 0,  se edita el valor de la cookie para que sea 1, recargamos la página y podemos ver la bandera para la solución de este reto.

# Referencias
http://saturn.picoctf.net:57329/
http://saturn.picoctf.net:57329/check.php