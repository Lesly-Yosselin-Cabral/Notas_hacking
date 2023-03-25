# Descripcion
Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.

# Pistas
1. Does that encoding look familiar?
2. The `str_xor` function does not need to be reverse engineered for this challenge.

# Solucion
```
┌──(kali㉿kali)-[~]
└─$ wget https://artifacts.picoctf.net/c/13/level2.py
--2023-03-23 15:50:39--  https://artifacts.picoctf.net/c/13/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 99.84.203.115, 99.84.203.40, 99.84.203.44, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|99.84.203.115|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: ‘level2.py’

level2.py                        100%[========================================================>]     914  --.-KB/s    in 0s      

2023-03-23 15:50:39 (3.08 MB/s) - ‘level2.py’ saved [914/914]

                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ wget https://artifacts.picoctf.net/c/13/level2.flag.txt.enc
--2023-03-23 15:51:07--  https://artifacts.picoctf.net/c/13/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 99.84.203.9, 99.84.203.115, 99.84.203.40, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|99.84.203.9|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: ‘level2.flag.txt.enc’

level2.flag.txt.enc              100%[========================================================>]      31  --.-KB/s    in 0s      

2023-03-23 15:51:08 (45.4 MB/s) - ‘level2.flag.txt.enc’ saved [31/31]

                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ ls
codebook.txt  cookie     Downloads  flag         level1.flag.txt.enc  level2.py  otrotoken  Public       Templates
code.py       Desktop    fixme1.py  flagout.txt  level1.py            Music      picoctf    repetitions  Videos
convertme.py  Documents  fixme2.py  hacking      level2.flag.txt.enc  netcat.py  Pictures   runme.py

┌──(kali㉿kali)-[~]
└─$ python3 level2.py
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}
```

# Bandera
picoCTF{tr45h_51ng1ng_489dea9a}

# Notas adicionales
Para la solución de este reto se hizo la descarga de los dos archivos proporcionados en el reto, enseguida se mandan abrir mandando llamar a python, pues al hacer la descarga se observa que es un programa echo es python.
Como salida nos pide una contraseña, es así como con ayuda de un editor de texto (VisualStudioCode) se abre el programa, se corre, se extrae la linea que contiene la contraseña, al obtener la salida, nuevamnete en consola se corre el archivo se pega la salida del programa  y es así como se obtiene la bandera de este reto.


# Referencias