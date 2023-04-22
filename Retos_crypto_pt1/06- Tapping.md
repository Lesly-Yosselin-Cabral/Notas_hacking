# Descripcion
Theres tapping coming in from the wires. What's it saying `nc jupiter.challenges.picoctf.org 9422`.

# Pistas
1.  What kind of encoding uses dashes and dots?
2. The flag is in the format PICOCTF{}

# Solucion
```
┌──(kali㉿kali)-[~/picoctf/crypto/tapping]
└─$ nc jupiter.challenges.picoctf.org 9422 
.--. .. -.-. --- -.-. - ..-. { -- ----- .-. ... ...-- -.-. ----- -.. ...-- .---- ... ..-. ..- -. ..--- -.... ---.. ...-- ---.. ..--- ....- -.... .---- ----- } 

PICOCTFM0RS3C0D31SFUN2683824610 
```

# Bandera
picoCTF{M0RS3C0D31SFUN2683824610}

# Notas adicionales


# Referencias
https://www.youtube.com/watch?v=g1bGxseNsxA&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=38

https://gchq.github.io/CyberChef/#recipe=From_Morse_Code('Space','Line%20feed')&input=Li0tLiAuLiAtLi0uIC0tLSAtLi0uIC0gLi4tLiB7IC0tIC0tLS0tIC4tLiAuLi4gLi4uLS0gLS4tLiAtLS0tLSAtLi4gLi4uLS0gLi0tLS0gLi4uIC4uLS4gLi4tIC0uIC4uLS0tIC0uLi4uIC0tLS4uIC4uLi0tIC0tLS4uIC4uLS0tIC4uLi4tIC0uLi4uIC4tLS0tIC0tLS0tIH0K