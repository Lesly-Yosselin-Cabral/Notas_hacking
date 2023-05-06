# Descripcion
Can you get the flag?Go to this [website](http://saturn.picoctf.net:64710/) and see what you can discover.

# Pistas
How is the password checked on this website?

# Solucion
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="[style.css](view-source:http://saturn.picoctf.net:64710/style.css)">
    <title>Secure Customer Portal</title>
  </head>
  <body>

    <h1>Secure Customer Portal</h1>
    
   <p>Only letters and numbers allowed for username and password.</p>
    
    <form role="form" action="[login.php](view-source:http://saturn.picoctf.net:64710/login.php)" method="post">
      <input type="text" name="username" placeholder="Username" required 
       autofocus></br>
      <input type="password" name="password" placeholder="Password" required>
      <button type="submit" name="login">Login</button>
    </form>
  </body>
</html>

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="[style.css](view-source:http://saturn.picoctf.net:64710/style.css)">
    <title>Login Page</title>
  </head>
  <body>
    <script src="[secure.js](view-source:http://saturn.picoctf.net:64710/secure.js)"></script>
    
    <p id='msg'></p>
    
    <form hidden action="[admin.php](view-source:http://saturn.picoctf.net:64710/admin.php)" method="post" id="hiddenAdminForm">
      <input type="text" name="hash" required id="adminFormHash">
    </form>
    
    <script type="text/javascript">
      function filter(string) {
        filterPassed = true;
        for (let i =0; i < string.length; i++){
          cc = string.charCodeAt(i);
          
          if ( (cc >= 48 && cc <= 57) ||
               (cc >= 65 && cc <= 90) ||
               (cc >= 97 && cc <= 122) )
          {
            filterPassed = true;     
          }
          else
          {
            return false;
          }
        }
        
        return true;
      }
    
      window.username = "";
      window.password = "";
      
      usernameFilterPassed = filter(window.username);
      passwordFilterPassed = filter(window.password);
      
      if ( usernameFilterPassed && passwordFilterPassed ) {
      
        loggedIn = checkPassword(window.username, window.password);
        
        if(loggedIn)
        {
          document.getElementById('msg').innerHTML = "Log In Successful";
          document.getElementById('adminFormHash').value = "2196812e91c29df34f5e217cfd639881";
          document.getElementById('hiddenAdminForm').submit();
        }
        else
        {
          document.getElementById('msg').innerHTML = "Log In Failed";
        }
      }
      else {
        document.getElementById('msg').innerHTML = "Illegal character in username or password."
      }
    </script>
    
  </body>
</html>

function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}

picoCTF{j5_15_7r4n5p4r3n7_b0c2c9cb}
```

# Bandera
picoCTF{j5_15_7r4n5p4r3n7_b0c2c9cb}

# Notas adicionales
Para la solución de este reto se ingresa al sitio web que se proporciona en la descripción del reto 
al ingresar se observa que en el login se requiere de un usuario y contraseña para acceder, por lo cual es necesario hacer la busqueda del password correcto.
Para lo que se accede al codigo fuente y al no observar algo util ahí a la direccion URL  se le agrega "loggin.php" y ya dentro de esta se observa unarchivo con el nombre "secure.js", sea  accede y es ahí donde obtenemos el password para ingresar al login y es así como al ingresar a la página se obtiene la bandera para la solución de este reto. 

# Referencias
http://saturn.picoctf.net:64710
http://saturn.picoctf.net:64710/login.php
view-source:http://saturn.picoctf.net:64710/secure.js
