# Descripcion
Can you decrypt this message?Decrypt this [message](https://artifacts.picoctf.net/c/160/cipher.txt) using this key "CYLAB".

# Pistas
https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher

# Solucion
```
┌──(kali㉿kali)-[~/picoctf/3erparcial/vigenere]
└─$ wget https://artifacts.picoctf.net/c/160/cipher.txt 
--2023-05-20 20:53:35--  https://artifacts.picoctf.net/c/160/cipher.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.103, 18.154.144.85, 18.154.144.104, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.103|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 43 [application/octet-stream]
Saving to: ‘cipher.txt’

cipher.txt               100%[===============================>]      43  --.-KB/s    in 0s      

2023-05-20 20:53:35 (105 MB/s) - ‘cipher.txt’ saved [43/43]

                                                                                                 
┌──(kali㉿kali)-[~/picoctf/3erparcial/vigenere]
└─$ cat cipher.txt 
rgnoDVD{O0NU_WQ3_G1G3O3T3_A1AH3S_2951c89f}

```

# Bandera
picoCTF{D0NT_US3_V1G3N3R3_C1PH3R_2951a89h}

# Notas adicionales
Para la solución de este reto se hizo la descarga del archivo que se proporciona en la descripción del reto, al mandarlo abrir podemos observar que contiene la bandera del reto, pero se encuentra en cifrado vigenere, para lo cual lo llevamos a un decifrador de este mismo y es así como se obtiene la badera para la solución de este reto.


# Referencias
https://www.dcode.fr/vigenere-cipher