# Descripcion

Can you find the robots? `https://jupiter.challenges.picoctf.org/problem/60915/` ([link](https://jupiter.challenges.picoctf.org/problem/60915/)) or http://jupiter.challenges.picoctf.org:60915

# Pistas
What part of the website could tell you where the creator doesn't want you to look?

# Solucion
```
User-agent: *
Disallow: /8028f.html

https://jupiter.challenges.picoctf.org/problem/60915/8028f.html
```

# Bandera
picoCTF{ca1cu1at1ng_Mach1n3s_8028f}

# Notas adicionales
Robots.txt = Es un metodos para evitar que ciertos boots analicen 


# Referencias