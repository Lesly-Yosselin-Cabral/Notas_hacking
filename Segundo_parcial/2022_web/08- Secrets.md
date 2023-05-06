# Descripcion
We have several pages hidden. Can you find the one with the flag?The website is running [here](http://saturn.picoctf.net:53932/).

# Pistas
folders folders folders

# Solucion
```
 <div class="imgcontainer">
      <img
        src="[secret/assets/DX1KYM.jpg](view-source:http://saturn.picoctf.net:53932/secret/assets/DX1KYM.jpg)"
        alt="https://www.alamy.com/security-safety-word-cloud-concept-image-image67649784.html"
        class="responsive"
/>

<!DOCTYPE html>
<html>
  <head>
    <title></title>
    <link rel="stylesheet" href="[hidden/file.css](view-source:http://saturn.picoctf.net:53932/secret/hidden/file.css)" />
  </head>

  <body>
    <h1>Finally. You almost found me. you are doing well</h1>
    <img src="[https://media1.tenor.com/images/0a6aff9f825af62c05adfbd75039cc7b/tenor.gif?itemid=4648337](view-source:https://media1.tenor.com/images/0a6aff9f825af62c05adfbd75039cc7b/tenor.gif?itemid=4648337)" alt="Something Like That GIF - Andy Parksandrecreation Wtf GIFs" style="max-width: 833px; background-color: rgb(151, 121, 85);" width="833" height="937.125">
  </body>
</html>

<!DOCTYPE html>
<html>
  <head>
    <title></title>
    <link rel="stylesheet" href="[mycss.css](view-source:http://saturn.picoctf.net:53932/secret/hidden/superhidden/mycss.css)" />
  </head>

  <body>
    <h1>Finally. You found me. But can you see me</h1>
    <h3 class="flag">picoCTF{succ3ss_@h3n1c@10n_51b260fe}</h3>
  </body>
</html>

/>
              <input
                type="password"
                name="password"
                placeholder="Password"
                required
              />
              <input type="hidden" name="db" value="superhidden/xdfgwd.html" />
```

# Bandera
picoCTF{succ3ss_@h3n1c@10n_51b260fe}

# Notas adicionales
Para la solución de este reto se accedió al sitio web que se proporciona en la descripción de el reto.
Una vez dentro de ella, se accede al codigo fuente, navegamos a la suburl "secret", nos lleva a un sitio web, pero tampoco encontramos algo util. Seguimos repitiendo este proceso hasta llegar aun sitio web que contiene una etiqueta con este mensaje "Finally. You found me. But can you see me", nos vamos al archivo css y hacemos una busqueda con cntrl+F de la palabra pico y es así como obtenemos la bandera para la solución de este reto.


# Referencias
view-source:http://saturn.picoctf.net:53932
view-source:http://saturn.picoctf.net:53932/secret/
http://saturn.picoctf.net:53932/secret/hidden/
view-source:http://saturn.picoctf.net:53932/secret/hidden/superhidden/