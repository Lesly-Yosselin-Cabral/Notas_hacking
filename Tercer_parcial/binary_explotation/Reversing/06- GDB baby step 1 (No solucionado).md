# Descripcion
Can you figure out what is in the `eax` register at the end of the `main` function? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Disassemble [this](https://artifacts.picoctf.net/c/512/debugger0_a).


# Pistas
1. gdb is a very good debugger to use for this problem and many others!
2. `main` is actually a recognized symbol that can be used with gdb commands.

# Solucion
```
┌──(kali㉿kali)-[~/picoctf/3erparcial/GDBbabbystp1]
└─$ wget https://artifacts.picoctf.net/c/512/debugger0_a             
--2023-05-22 22:14:16--  https://artifacts.picoctf.net/c/512/debugger0_a

Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.132.88, 18.154.132.108, 18.154.132.74, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.132.88|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16472 (16K) [application/octet-stream]
Saving to: ‘debugger0_a’

debugger0_a              100%[===============================>]  16.09K  --.-KB/s    in 0.02s   

2023-05-22 22:14:17 (830 KB/s) - ‘debugger0_a’ saved [16472/16472]


```

# Bandera
picoCTF{}

# Notas adicionales


# Referencias