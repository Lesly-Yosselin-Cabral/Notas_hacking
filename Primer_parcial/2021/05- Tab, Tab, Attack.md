# Descripcion
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/659efd595171e4c40378be6a2e9b7298/Addadshashanammu.zip)


# Pistas
After `unzip`ing, this problem can be solved with 11 button-presses...(mostly Tab)...

# Solucion
```
yosshell-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/659efd595171e4c40378be6a2e9b7298/Addadshashanammu.zip
--2023-03-22 23:01:44--  https://mercury.picoctf.net/static/659efd595171e4c40378be6a2e9b7298/Addadshashanammu.zip
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4520 (4.4K) [application/octet-stream]
Saving to: 'Addadshashanammu.zip'

Addadshashanammu.zip                           100%[===================================================================================================>]   4.41K  --.-KB/s    in 0s      

2023-03-22 23:01:44 (3.44 GB/s) - 'Addadshashanammu.zip' saved [4520/4520]

yosshell-picoctf@webshell:~$ unzip Addadshashanammu.zip
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
yosshell-picoctf@webshell:~$ cd Add
-bash: cd: Add: No such file or directory
yosshell-picoctf@webshell:~$ cd Addadshashanammu/
yosshell-picoctf@webshell:~/Addadshashanammu$ cd Almurbalarammi/
yosshell-picoctf@webshell:~/Addadshashanammu/Almurbalarammi$ cd Ashalmimilkala/
yosshell-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala$ cd Assurnabitashpi/
yosshell-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi$ cd Maelkashishi/
yosshell-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi$ cd Onnissiralis/
yosshell-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis$ cd Ularradallaku/
yosshell-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls
fang-of-haynekhtnamet
yosshell-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ stat fang-of-haynekhtnamet 
  File: fang-of-haynekhtnamet
  Size: 8320            Blocks: 24         IO Block: 4096   regular file
Device: 10301h/66305d   Inode: 879661487   Links: 1
Access: (0755/-rwxr-xr-x)  Uid: (10000/yosshell-picoctf)   Gid: (10000/yosshell-picoctf)
Access: 2021-03-16 01:16:35.000000000 +0000
Modify: 2021-03-16 01:16:35.000000000 +0000
Change: 2023-03-22 23:01:52.100856742 +0000
 Birth: 2023-03-22 23:01:52.100856742 +0000
yosshell-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ./fang-of-haynekhtnamet 
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_524e3dc4}
```

# Bandera
picoCTF{l3v3l_up!_t4k3_4_r35t!_524e3dc4}

# Notas adicionales
Para la solución de este reto se hizo la descarga del archivo que propprcina el reto, al ser un archivo comprimido en zip con ayuda del comando unzip se descomprimió por medio de la consola, nos da como resultado un directorio se fueron abriendo las carpeta hasta llegar al archivo que contenia la bandera.

# Referencias