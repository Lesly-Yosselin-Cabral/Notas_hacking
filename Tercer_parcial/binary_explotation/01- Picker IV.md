# Descripcion
Can you figure out how this program works to get the flag?Connect to the program with netcat:`$ nc saturn.picoctf.net 64402`The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/529/picker-IV.c). The binary can be downloaded [here](https://artifacts.picoctf.net/c/529/picker-IV).

# Pistas
1. With Python, there are no binaries. With compiled languages like C, there is source code, and there are binaries. Binaries are created from source code, they are a conversion from the human-readable source code, to the highly efficient machine language, in this case: x86_64.
2. How can you find the address that `win` is at?


# Solucion
```
┌──(kali㉿kali)-[~/picoctf/3erparcial/binaryexplotation/pickerIV]
└─$ wget https://artifacts.picoctf.net/c/529/picker-IV.c
--2023-05-22 23:47:14--  https://artifacts.picoctf.net/c/529/picker-IV.c
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.132.74, 18.154.132.108, 18.154.132.88, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.132.74|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 839 [application/octet-stream]
Saving to: ‘picker-IV.c’

picker-IV.c              100%[===============================>]     839  --.-KB/s    in 0s      

2023-05-22 23:47:17 (7.72 MB/s) - ‘picker-IV.c’ saved [839/839]

                                                                                                 
┌──(kali㉿kali)-[~/picoctf/3erparcial/binaryexplotation/pickerIV]
└─$ wget https://artifacts.picoctf.net/c/529/picker-IV  
--2023-05-22 23:47:28--  https://artifacts.picoctf.net/c/529/picker-IV
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.160.124.38, 18.160.124.119, 18.160.124.108, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.160.124.38|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 17272 (17K) [application/octet-stream]
Saving to: ‘picker-IV’

picker-IV                100%[===============================>]  16.87K  --.-KB/s    in 0s      

2023-05-22 23:47:43 (190 MB/s) - ‘picker-IV’ saved [17272/17272]



```

# Bandera


# Notas adicionales


# Referencias
