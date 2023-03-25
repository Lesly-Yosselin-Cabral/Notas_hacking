# Descripcion
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/bc72945175d643626d6ea9a689672dbd/static)? This [BASH script](https://mercury.picoctf.net/static/bc72945175d643626d6ea9a689672dbd/ltdis.sh) might help!

# Pistas


# Solucion
```
yosshell-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/bc72945175d643626d6ea9a689672dbd/ltdis.sh
--2023-03-21 22:41:54--  https://mercury.picoctf.net/static/bc72945175d643626d6ea9a689672dbd/ltdis.sh
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 785 [application/octet-stream]
Saving to: 'ltdis.sh'

ltdis.sh                                       100%[===================================================================================================>]     785  --.-KB/s    in 0s      

2023-03-21 22:41:54 (293 MB/s) - 'ltdis.sh' saved [785/785]

yosshell-picoctf@webshell:~$ ls
README.txt  file  flag  ltdis.sh  static  strings  warm
yosshell-picoctf@webshell:~$ ls -l
total 816
-rw-r--r-- 1 root             root               4443 Mar 21 22:20 README.txt
-rw-rw-r-- 1 yosshell-picoctf yosshell-picoctf  14551 Oct 26  2020 file
-rw-rw-r-- 1 yosshell-picoctf yosshell-picoctf     34 Mar 16  2021 flag
-rw-rw-r-- 1 yosshell-picoctf yosshell-picoctf    785 Mar 16  2021 ltdis.sh
-rw-rw-r-- 1 yosshell-picoctf yosshell-picoctf   8376 Mar 16  2021 static
-rwxrwxrwx 1 yosshell-picoctf yosshell-picoctf 776032 Oct 26  2020 strings
-rwxrwxr-x 1 yosshell-picoctf yosshell-picoctf  10936 Mar 16  2021 warm
yosshell-picoctf@webshell:~$ ./ltdis.sh         
-bash: ./ltdis.sh: Permission denied
yosshell-picoctf@webshell:~$ ./ltdis.sh static
-bash: ./ltdis.sh: Permission denied
yosshell-picoctf@webshell:~$ chmod +x ltdis.sh
yosshell-picoctf@webshell:~$ ./ltdis.sh static
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
yosshell-picoctf@webshell:~$ ls 
README.txt  file  flag  ltdis.sh  static  static.ltdis.strings.txt  static.ltdis.x86_64.txt  strings  warm
yosshell-picoctf@webshell:~$ cat static.ltdis.strings.txt | grep pico
   1020 picoCTF{d15a5m_t34s3r_1e6a7731}
```

# Bandera
picoCTF{d15a5m_t34s3r_1e6a7731}

# Notas adicionales
Se hizo la descarga del archivo, se le dió permiso de ejecución y con un grep se recopilo solo la linea de codigo que contenia la bandera para la solucion del reto.


# Referencias