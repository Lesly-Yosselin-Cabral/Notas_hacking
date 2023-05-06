# Descripcion
The flag is somewhere on this web application not necessarily on the website. Find it.Check [this](http://saturn.picoctf.net:55771/) out.

# Pistas
(None)

# Solucion
```
User-agent *
Disallow: /cgi-bin/
Think you have seen your flag or want to keep looking.

ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg
Disallow: /wp-admin/

picoCTF{Who_D03sN7_L1k5_90B0T5_22ce1f22}
```

# Bandera
picoCTF{Who_D03sN7_L1k5_90B0T5_22ce1f22}

# Notas adicionales
Para la solución de este reto se accedió al sitio web que se proporciona en la descripción de el reto.
Una vez dentro de ella, se accede al codigo fuente, al no observar nada que nos lleve a la solución, a la URL del sitio web se le agrega robots.txt para acceder a ese archivo en la pagina. Encontramos unas cadenas de texto codificadas en base64.
Así que llevamos la segunda línea del archivo a Cyberchef para decodificarla, una vez echo este nos arroja el nombre de un nuevo archivo con el nombre de js/myfile.txt, lo susitituiomos por el re robots.txt, recargamos y es así como se obtiene la bandera con la solución de este reto.


# Referencias
http://saturn.picoctf.net:55771/
http://saturn.picoctf.net:55771/robots.txt
https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=YW5NdmJYbG1hV3hsTG5SNGRBPT0
http://saturn.picoctf.net:55771/js/myfile.txt
