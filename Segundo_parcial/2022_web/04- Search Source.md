# Descripcion
The developer of this website mistakenly left an important artifact in the website source, can you find it?The website is [here](http://saturn.picoctf.net:53295/)

# Pistas
How could you mirror the website on your local machine so you could use more powerful tools for searching?

# Solucion
```
<!DOCTYPE html>
<html lang="en">

<head>
    <!-- basic -->
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <!-- mobile metas -->
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="viewport" content="initial-scale=1, maximum-scale=1">
    <!-- site metas -->
    <title>flexed</title>
    <meta name="keywords" content="">
    <meta name="description" content="">
    <meta name="author" content="">
    <!-- bootstrap css -->
    <link rel="stylesheet" href="[css/bootstrap.min.css](view-source:http://saturn.picoctf.net:53295/css/bootstrap.min.css)">
    <!-- owl css -->
    <link rel="stylesheet" href="[css/owl.carousel.min.css](view-source:http://saturn.picoctf.net:53295/css/owl.carousel.min.css)">
    <!-- style css -->
    <link rel="stylesheet" href="[css/style.css](view-source:http://saturn.picoctf.net:53295/css/style.css)">
    <!-- responsive-->
    <link rel="stylesheet" href="[css/responsive.css](view-source:http://saturn.picoctf.net:53295/css/responsive.css)">
    <!-- awesome fontfamily -->
    <link rel="stylesheet" href="[https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css](view-source:https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css)">
    <!--[if lt IE 9]>
      <script src="https://oss.maxcdn.com/html5shiv/3.7.3/html5shiv.min.js"></script>
      <script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script><![endif]-->
</head>
<!-- body -->

/** banner_main picoCTF{1nsp3ti0n_0f_w3bpag3s_8de925a7} **/
 .carousel-indicators li {
     width: 20px;
     height: 20px;
     border-radius: 11px;
     background-color: #070000;
```

# Bandera
picoCTF{1nsp3ti0n_0f_w3bpag3s_8de925a7}

# Notas adicionales
Para la solución de este reto se accedió al sitio web que se proporciona en la descripción de el reto.
Una vez dentro de ella, se accede al codigo fuente, en el se accede a la hoja de estilos y se ahace una busqueda dentro de todo el codigo (con control+F, ya que se observa bastante) de la palabra pico y es así como se encuentra la bandera con la solución de este reto.

# Referencias
http://saturn.picoctf.net:53295/
view-source:http://saturn.picoctf.net:53295/
view-source:http://saturn.picoctf.net:53295/css/style.css