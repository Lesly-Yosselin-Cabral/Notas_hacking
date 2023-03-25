# Descripcion
Fix the syntax error in the Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/5/fixme2.py)

# Pistas
1. Are equality and assignment the same symbol?
2. To view the file in the webshell, do: `$ nano fixme2.py`
3. To exit `nano`, press Ctrl and x and follow the on-screen prompts.
4. The `str_xor` function does not need to be reverse engineered for this challenge.

# Solucion
```
┌──(kali㉿kali)-[~]
└─$ wget https://artifacts.picoctf.net/c/5/fixme2.py 
--2023-03-22 22:52:41--  https://artifacts.picoctf.net/c/5/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 99.84.203.44, 99.84.203.115, 99.84.203.9, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|99.84.203.44|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: ‘fixme2.py’

fixme2.py                        100%[========================================================>]   1.00K  --.-KB/s    in 0s      

2023-03-22 22:52:42 (10.3 MB/s) - ‘fixme2.py’ saved [1029/1029]

                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ ls
codebook.txt  convertme.py  Desktop    Downloads  fixme2.py  flagout.txt  Music      otrotoken  Public       runme.py   Videos
code.py       cookie        Documents  fixme1.py  flag       hacking      netcat.py  Pictures   repetitions  Templates
                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ python3 fixme2.py
  File "/home/kali/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ sudo nano fixme2.py                             
                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ python3 fixme2.py  
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}

```

# Bandera
picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}

# Notas adicionales
Para la solucion de este reto se hizo la descarga del programa hecho en python que proporciona el reto, al querer ejecutarlo nos  da un mensaje donde dice que hay un error en la linea donde se encuentra un if, se le da solución, se guarda y se vuele a ejecutar el programa y es asi como se obtiene la bandera con la solución de este reto.

# Referencias