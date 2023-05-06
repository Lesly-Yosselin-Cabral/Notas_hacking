# Descripcion
Attackers have hidden information in a very large mass of data in the past, maybe they are still doing it. Download the data [here](https://artifacts.picoctf.net/c/126/anthem.flag.txt).

# Pistas
Download the file and search for the flag based on the known prefix.
# Solucion
```
┌──(kali㉿kali)-[~/picoctf/2doparcial/forensic2022/lookeyhere]
└─$ wget https://artifacts.picoctf.net/c/126/anthem.flag.txt   
--2023-05-06 17:28:33--  https://artifacts.picoctf.net/c/126/anthem.flag.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.132.88, 18.154.132.74, 18.154.132.108, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.132.88|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 108668 (106K) [application/octet-stream]
Saving to: ‘anthem.flag.txt’

anthem.flag.txt                      100%[======================================================================>] 106.12K   700KB/s    in 0.2s    

2023-05-06 17:28:34 (700 KB/s) - ‘anthem.flag.txt’ saved [108668/108668]

                                                                                                                                                    
┌──(kali㉿kali)-[~/picoctf/2doparcial/forensic2022/lookeyhere]
└─$ open anthem.flag.txt 


      These things help us in our work. We do not understand them, but
      we think that the men of picoCTF{gr3p_15_@w3s0m3_2116b979}

┌──(kali㉿kali)-[~/picoctf/2doparcial/forensic2022/lookeyhere]
└─$ strings anthem.flag.txt | grep pico
      we think that the men of picoCTF{gr3p_15_@w3s0m3_2116b979}
```

# Bandera
picoCTF{gr3p_15_@w3s0m3_2116b979}

# Notas adicionales
Para la solucion de este reto se hace la descarga del archivo que se proporciona en la descripción de el reto, se manda abrir, al observar demasiados caracteres buscamos una opción más fácil para obtener la bandera, esto con la ayuda de un strings y un grep añadiendo la palabra "pico" y es así como se obtiene la bandeera para la solución de este reto.
# Referencias