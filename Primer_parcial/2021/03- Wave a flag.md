# Descripcion
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm) has extraordinarily helpful information...


# Pistas
1. This program will only work in the webshell or another Linux computer.
2. To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm`
3. Run this program by entering the following in the Terminal prompt: `$ ./warm`, but you'll first have to make it executable with `$ chmod +x warm`
4. -h and --help are the most common arguments to give to programs to get more information from them!
5. Not every program implements help features like -h and --help.

# Solucion
```
yosshell-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm
--2023-03-21 19:00:43--  https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm'

warm                                           100%[===================================================================================================>]  10.68K  --.-KB/s    in 0s      

2023-03-21 19:00:43 (425 MB/s) - 'warm' saved [10936/10936]

yosshell-picoctf@webshell:~$ ls
README.txt  file  flag  strings  warm
yosshell-picoctf@webshell:~$ ./warm
-bash: ./warm: Permission denied
yosshell-picoctf@webshell:~$ chmod +x warm
yosshell-picoctf@webshell:~$ 11
-bash: 11: command not found
yosshell-picoctf@webshell:~$ ll
total 824
drwxr-xr-x 2 yosshell-picoctf yosshell-picoctf    188 Mar 21 19:00 ./
drwxr-xr-x 3 root             root                 30 Mar  2 18:36 ../
-rw------- 1 yosshell-picoctf yosshell-picoctf     99 Mar 12 04:03 .bash_history
-rw-r--r-- 1 yosshell-picoctf yosshell-picoctf    220 Mar  2 18:36 .bash_logout
-rw-r--r-- 1 yosshell-picoctf yosshell-picoctf   3771 Mar  2 18:36 .bashrc
-rw-r--r-- 1 yosshell-picoctf yosshell-picoctf    807 Mar  2 18:36 .profile
-rw------- 1 yosshell-picoctf yosshell-picoctf     66 Mar  2 18:56 .python_history
-rw-rw-r-- 1 yosshell-picoctf yosshell-picoctf    215 Mar 21 19:00 .wget-hsts
-rw-r--r-- 1 root             root               4443 Mar 21 18:52 README.txt
-rw-rw-r-- 1 yosshell-picoctf yosshell-picoctf  14551 Oct 26  2020 file
-rw-rw-r-- 1 yosshell-picoctf yosshell-picoctf     34 Mar 16  2021 flag
-rwxrwxrwx 1 yosshell-picoctf yosshell-picoctf 776032 Oct 26  2020 strings*
-rwxrwxr-x 1 yosshell-picoctf yosshell-picoctf  10936 Mar 16  2021 warm*
yosshell-picoctf@webshell:~$ chmod +x warm
yosshell-picoctf@webshell:~$ ./warm
Hello user! Pass me a -h to learn what I can do!
yosshell-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_755f3544}
```

# Bandera
picoCTF{b1scu1ts_4nd_gr4vy_755f3544}

# Notas adicionales


# Referencias