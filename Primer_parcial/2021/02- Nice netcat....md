# Descripcion
There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 43239`, but it doesn't speak English...


# Pistas
1. You can practice using netcat with this picoGym problem: [what's a netcat?](https://play.picoctf.org/practice/challenge/34)
2. You can practice reading and writing ASCII with this picoGym problem: [Let's Warm Up](https://play.picoctf.org/practice/challenge/22)


# Solucion
```
yosshell-picoctf@webshell:~$ nc mercury.picoctf.net 43239
112 105 99 111 67 84 70 123 103 48 48 100 95 107 49 116 116 121 33 95 110 49 99 51 95 107 49 116 116 121 33 95 55 99 48 56 50 49 102 53 125 10

nums = [112, 105, 99, 111, 67, 84, 70, 123, 103, 48, 48, 100, 95, 107, 49, 116, 116, 121, 33, 95, 110, 49, 99, 51, 95, 107, 49, 116, 116, 121, 33, 95, 55, 99, 48, 56, 50, 49, 102, 53, 125, 10]
flag = ""
for number in nums:
    flag += chr(number)
print(flag)

Python 3.11.2 (main, Feb 12 2023, 00:48:52) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license()" for more information.


========================= RESTART: /home/kali/netcat.py ========================
picoCTF{g00d_k1tty!_n1c3_k1tty!_7c0821f5}

```


# Bandera
picoCTF{g00d_k1tty!_n1c3_k1tty!_7c0821f5}

# Notas adicionales


# Referencias
[Bonito netcat | Reseñas de PicoCTF 2021 (vivian-dai.github.io)](https://vivian-dai.github.io/PicoCTF2021-Writeup/General%20Skills/Nice%20netcat/Nice%20netcat.html)