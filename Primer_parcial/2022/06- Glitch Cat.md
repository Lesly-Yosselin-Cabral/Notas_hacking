# Descripcion
Our flag printing service has started glitching! `$ nc saturn.picoctf.net 50561`

# Pistas
1. ASCII is one of the most common encodings used in programming
2. We know that the glitch output is valid Python, somehow!
3. Press Ctrl and c on your keyboard to close your connection and return to the command prompt.

# Solucion
```
                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ nc saturn.picoctf.net 50561
'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ python3          
Python 3.11.2 (main, Feb 12 2023, 00:48:52) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
'picoCTF{gl17ch_m3_n07_9c42a45d}'
>>> 

```

# Bandera
picoCTF{gl17ch_m3_n07_9c42a45d}

# Notas adicionales
Para la solución de este reto se accede al puerto que da el reto con ayuda del comando nc. Ya dentro nos proporciona la salida de programa hecho en python, por ende se manda llamar a Python por consola y ahí se pega la salida ya antes mencionada y es así como se obtiene la bandera con la solución de este reto.


# Referencias