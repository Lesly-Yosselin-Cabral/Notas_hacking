# Descripcion
Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/17/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin) in the same directory too. There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

# Pistas
1. To view the level3.hash.bin file in the webshell, do: `$ bvi level3.hash.bin`
2. To exit `bvi` type `:q` and press enter.
3. The `str_xor` function does not need to be reverse engineered for this challenge.

# Solucion
```
──(kali㉿kali)-[~]
└─$ cd picoctf 
                                                                                                                                  
┌──(kali㉿kali)-[~/picoctf]
└─$ mkdir pwcrack3
                                                                                                                                  
┌──(kali㉿kali)-[~/picoctf]
└─$ cd pwcrack3 
                                                                                                                                  
┌──(kali㉿kali)-[~/picoctf/pwcrack3]
└─$ ls
                                                                                                                                  
┌──(kali㉿kali)-[~/picoctf/pwcrack3]
└─$ wget https://artifacts.picoctf.net/c/17/level3.py          
--2023-03-23 15:59:48--  https://artifacts.picoctf.net/c/17/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 99.84.203.9, 99.84.203.44, 99.84.203.40, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|99.84.203.9|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: ‘level3.py’

level3.py                        100%[========================================================>]   1.31K  --.-KB/s    in 0s      

2023-03-23 15:59:49 (29.6 MB/s) - ‘level3.py’ saved [1337/1337]

                                                                                                                                  
┌──(kali㉿kali)-[~/picoctf/pwcrack3]
└─$ wget https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
--2023-03-23 16:00:03--  https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 99.84.203.40, 99.84.203.115, 99.84.203.9, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|99.84.203.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: ‘level3.flag.txt.enc’

level3.flag.txt.enc              100%[========================================================>]      31  --.-KB/s    in 0s      

2023-03-23 16:00:04 (21.4 MB/s) - ‘level3.flag.txt.enc’ saved [31/31]

                                                                                                                                  
┌──(kali㉿kali)-[~/picoctf/pwcrack3]
└─$ wget https://artifacts.picoctf.net/c/17/level3.hash.bin    
--2023-03-23 16:00:14--  https://artifacts.picoctf.net/c/17/level3.hash.bin
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 99.84.203.40, 99.84.203.115, 99.84.203.9, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|99.84.203.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16 [application/octet-stream]
Saving to: ‘level3.hash.bin’

level3.hash.bin                  100%[========================================================>]      16  --.-KB/s    in 0s      

2023-03-23 16:00:15 (249 KB/s) - ‘level3.hash.bin’ saved [16/16]

                                                                                                                                  
┌──(kali㉿kali)-[~/picoctf/pwcrack3]
└─$ ls
level3.flag.txt.enc  level3.hash.bin  level3.py
                                                                                                                                  
┌──(kali㉿kali)-[~/picoctf/pwcrack3]
└─$ python3 level3.py
Please enter correct password for flag: 
That password is incorrect

┌──(kali㉿kali)-[~/picoctf/pwcrack3]
└─$ bvi level3.hash.bin

zsh: suspended  bvi level3.hash.bin
                                                                                                                                  
┌──(kali㉿kali)-[~/picoctf/pwcrack3]
└─$ python3 level3.py  
Please enter correct password for flag: 87ab
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}

```

# Bandera
picoCTF{m45h_fl1ng1ng_cd6ed2eb}

# Notas adicionales
Para la solución de este reto se hizo la descarga de los dos archivos proporcionados en el reto, enseguida se mandan abrir mandando llamar a python, pues al hacer la descarga se observa que es un programa echo es python.
Como salida nos pide una contraseña, es así como con ayuda de una de las pistas que proporciona el reto se utiliza el comando que da y se  abre el programa, se corre, se extrae la linea que contiene la contraseña, se lleva a un editor que sirve para desifrar la contraaseña hash,mal obtener la salida, nuevamnete en consola se corre el archivo se pega la salida del editor  y es así como se obtiene la bandera de este reto.


# Referencias
https://crackstation.net/