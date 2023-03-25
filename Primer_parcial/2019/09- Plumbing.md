# Descripcion
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 14291`.


# Pistas
1. Remember the flag format is picoCTF{XXXX}
2. What's a pipe? No not that kind of pipe... This [kind](http://www.linfo.org/pipes.html)


# Solucion
```
┌──(kali㉿kali)-[~]
└─$ nc jupiter.challenges.picoctf.org 14291 >> flagout.txt
                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ ls
cookie  Desktop  Documents  Downloads  flagout.txt  hacking  Music  otrotoken  Pictures  Public  repetitions  Templates  Videos
                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ cat flagout.txt | grep pico
picoCTF{digital_plumb3r_ea8bfec7}

```

# Bandera
picoCTF{digital_plumb3r_ea8bfec7}

# Notas adicionales


# Referencias