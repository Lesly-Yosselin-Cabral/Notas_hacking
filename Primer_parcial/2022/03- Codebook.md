# Descripcion
Run the Python script `code.py` in the same directory as `codebook.txt`.

-   [Download code.py](https://artifacts.picoctf.net/c/1/code.py)
-   [Download codebook.txt](https://artifacts.picoctf.net/c/1/codebook.txt)

# Pistas
1. On the webshell, use `ls` to see if both files are in the directory you are in.
2. The `str_xor` function does not need to be reverse engineered for this challenge.


# Solucion
```
┌──(kali㉿kali)-[~]
└─$ wget https://artifacts.picoctf.net/c/1/code.py      
--2023-03-22 20:09:00--  https://artifacts.picoctf.net/c/1/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 99.84.203.115, 99.84.203.44, 99.84.203.9, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|99.84.203.115|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: ‘code.py’

code.py                          100%[========================================================>]   1.25K  --.-KB/s    in 0s      

2023-03-22 20:09:00 (7.54 MB/s) - ‘code.py’ saved [1278/1278]

                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ wget https://artifacts.picoctf.net/c/1/codebook.txt
--2023-03-22 20:09:30--  https://artifacts.picoctf.net/c/1/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 99.84.203.40, 99.84.203.115, 99.84.203.44, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|99.84.203.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: ‘codebook.txt’

codebook.txt                     100%[========================================================>]      27  --.-KB/s    in 0s      

2023-03-22 20:09:34 (15.8 MB/s) - ‘codebook.txt’ saved [27/27]

                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ ls
codebook.txt  convertme.py  Desktop    Downloads  flagout.txt  Music      otrotoken  Public       runme.py   Videos
code.py       cookie        Documents  flag       hacking      netcat.py  Pictures   repetitions  Templates
                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ python3 code.py     
picoCTF{c0d3b00k_455157_d9aa2df2}

```

# Bandera
picoCTF{c0d3b00k_455157_d9aa2df2}

# Notas adicionales
Para la solución de este reto se hizo la descarga de los archivos que proporciona, al ser .py se mandan llamar y ejecutar con python y es asi como se obtiene la bandera de este reto.


# Referencias