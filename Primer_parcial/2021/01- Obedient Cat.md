# Descripcion
This file has a flag in plain sight (aka "in-the-clear"). [Download flag](https://mercury.picoctf.net/static/217686fc11d733b80be62dcfcfca6c75/flag).


# Pistas
1. Any hints about entering a command into the Terminal (such as the next one), will start with a '$'... everything after the dollar sign will be typed (or copy and pasted) into your Terminal.
2. To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/217686fc11d733b80be62dcfcfca6c75/flag`
3. `$ man cat`

# Solucion
```
yosshell-picoctf@webshell:~$  wget https://mercury.picoctf.net/static/217686fc11d733b80be62dcfcfca6c75/flag
--2023-03-21 18:30:55--  https://mercury.picoctf.net/static/217686fc11d733b80be62dcfcfca6c75/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: 'flag'

flag                                           100%[===================================================================================================>]      34  --.-KB/s    in 0s      

2023-03-21 18:30:55 (29.2 MB/s) - 'flag' saved [34/34]

yosshell-picoctf@webshell:~$ ls  
README.txt  file  flag  strings
yosshell-picoctf@webshell:~$ cat flag
picoCTF{s4n1ty_v3r1f13d_b5aeb3dd}
yosshell-picoctf@webshell:~$ less flag

[1]+  Stopped                 less flag
yosshell-picoctf@webshell:~$ more flag
picoCTF{s4n1ty_v3r1f13d_b5aeb3dd}
```

# Bandera
picoCTF{s4n1ty_v3r1f13d_b5aeb3dd}

# Notas adicionales
Comando -> less visualiza archivos de texto por medio de la consola.
En la solucion de este reto se hizo uso de la consola de python
con ella se hizo la descarga del archivo que proporciona el reto con el comando wget. una vex relizda con el comando ls enliste los archivos para verificar que si existiera el que se necesitaba, al corroborarlo y para finalizar se hizo uso del comando less para poder visualizar el archivo y obtener la bandera del reto.


# Referencias