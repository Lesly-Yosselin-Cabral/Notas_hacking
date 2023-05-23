# Descripcion
I just recently learnt about the SRA public key cryptosystem... or wait, was it supposed to be RSA? Hmmm, I should probably check...Connect to the program on our server: `nc saturn.picoctf.net 52774`Download the program: [chal.py](https://artifacts.picoctf.net/c/299/chal.py)

# Pistas
(None)

# Solucion
```
┌──(kali㉿kali)-[~/picoctf/3erparcial/sra]
└─$ wget https://artifacts.picoctf.net/c/299/chal.py   
--2023-05-20 21:02:45--  https://artifacts.picoctf.net/c/299/chal.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.85, 18.154.144.104, 18.154.144.107, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.85|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 630 [application/octet-stream]
Saving to: ‘chal.py’

chal.py                  100%[===============================>]     630  --.-KB/s    in 0s      

2023-05-20 21:02:45 (5.91 MB/s) - ‘chal.py’ saved [630/630]

                                                                                                 
┌──(kali㉿kali)-[~/picoctf/3erparcial/sra]
└─$ open chal.py 
```

# Bandera
picoCTF{}

# Notas adicionales


# Referencias