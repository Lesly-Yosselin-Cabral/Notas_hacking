# Descripcion
Can you get the flag?Go to this [website](http://saturn.picoctf.net:63115/) and see what you can discover

# Pistas
Is there more code than what the inspector initially shows?

# Solucion
```
!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="[style.css](view-source:http://saturn.picoctf.net:63115/style.css)">
    <title>On Includes</title>
  </head>
  <body>
    <script src="[script.js](view-source:http://saturn.picoctf.net:63115/script.js)"></script>
  
    <h1>On Includes</h1>
    <p>Many programming languages and other computer files have a directive, 
       often called include (sometimes copy or import), that causes the 
       contents of a second file to be inserted into the original file. These 
       included files are called copybooks or header files. They are often used
       to define the physical layout of program data, pieces of procedural code
       and/or forward declarations while promoting encapsulation and the reuse
       of code.</p>
    <br>
    <p> Source: Wikipedia on Include directive </p>
    <button type="button" onclick="greetings();">Say hello</button>
  </body>
</html>

body {
  background-color: lightblue;
}

/*  picoCTF{1nclu51v17y_1of2_  */

function greetings()
{
  alert("This code is in a separate file!");
}

//  f7w_2of2_6edef411}
```

# Bandera
picoCTF{1nclu51v17y_1of2_f7w_2of2_6edef411}

# Notas adicionales
Se abre la dirección URL que aparece en la descripción del reto, estando en la pagina a ala re que manda, se insepcciona el codigo fuente, dentro de ahí se abre la hoja de estilos donde se encuentra la primera parte de la bandera y en el archivo script.js se encuentra la segunda  parate y es así como se cumple con la solución de este reto.

# Referencias
view-source:http://saturn.picoctf.net:63115/
view-source:http://saturn.picoctf.net:63115/style.css
view-source:http://saturn.picoctf.net:63115/script.js