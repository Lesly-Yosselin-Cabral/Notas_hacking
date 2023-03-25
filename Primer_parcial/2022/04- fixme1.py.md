# Descripcion
Fix the syntax error in this Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/26/fixme1.py)

# Pistas
1. Indentation is very meaningful in Python
2. To view the file in the webshell, do: `$ nano fixme1.py`
3. To exit `nano`, press Ctrl and x and follow the on-screen prompts.
4. The `str_xor` function does not need to be reverse engineered for this challenge.

# Solucion
```
┌──(kali㉿kali)-[~]
└─$ wget https://artifacts.picoctf.net/c/26/fixme1.py
--2023-03-22 22:42:43--  https://artifacts.picoctf.net/c/26/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 99.84.203.115, 99.84.203.44, 99.84.203.40, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|99.84.203.115|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: ‘fixme1.py’

fixme1.py                        100%[========================================================>]     837  --.-KB/s    in 0.001s  

2023-03-22 22:42:43 (1.50 MB/s) - ‘fixme1.py’ saved [837/837]

                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ ls
codebook.txt  convertme.py  Desktop    Downloads  flag         hacking  netcat.py  Pictures  repetitions  Templates
code.py       cookie        Documents  fixme1.py  flagout.txt  Music    otrotoken  Public    runme.py     Videos
                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ python3 fixme1.py 
  File "/home/kali/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ sudo nano fixme1.py     
[sudo] password for kali: 
                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ python3 fixme1.py  
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_09ee727a}

```

# Bandera
picoCTF{1nd3nt1ty_cr1515_09ee727a}

# Notas adicionales
Para la solucion de este reto se hizo la descarga del programa hecho en python que proporciona el reto, al querer ejecutarlo nos  da un mensaje donde dice que la linea que imprime la bandera esta mal identada, se le hace la identación correcta, se guarda, se vuele ejecutar el programa y es así como se obtiene la bandera de la solución de este reto.

# Referencias
