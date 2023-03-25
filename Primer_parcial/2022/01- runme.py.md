# Descripcion
Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell. [Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)

# Pistas
1. If you have Python on your computer, you can download the script normally and run it. Otherwise, use the `wget` command in the webshell.
2. To use `wget` in the webshell, first right click on the download link and select 'Copy Link' or 'Copy Link Address'
3. Type everything after the dollar sign in the webshell: `$ wget` , then paste the link after the space after `wget` and press enter. This will download the script for you in the webshell so you can run it!
4. Finally, to run the script, type everything after the dollar sign and then press enter: `$ python3 runme.py` You should have the flag now!


# Solucion
```
┌──(kali㉿kali)-[~]
└─$ wget https://artifacts.picoctf.net/c/34/runme.py
--2023-03-22 19:37:46--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 99.84.203.44, 99.84.203.40, 99.84.203.115, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|99.84.203.44|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: ‘runme.py’

runme.py                         100%[========================================================>]     270  --.-KB/s    in 0s      

2023-03-22 19:37:46 (252 MB/s) - ‘runme.py’ saved [270/270]

┌──(kali㉿kali)-[~]
└─$ ls               
cookie   Documents  flag         hacking  netcat.py  Pictures  repetitions  Templates
Desktop  Downloads  flagout.txt  Music    otrotoken  Public    runme.py     Videos
                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ chmod +x runme.py
                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ python3 runme.py 
picoCTF{run_s4n1ty_run}
```

# Bandera
picoCTF{run_s4n1ty_run}

# Notas adicionales
Para la solución del reto se hace la descarga del archivo que proporciona, se le asigna permiso de ejecución, eneseguida se eejecuta y este arroja la bandera que contiene la solución de reto.


# Referencias