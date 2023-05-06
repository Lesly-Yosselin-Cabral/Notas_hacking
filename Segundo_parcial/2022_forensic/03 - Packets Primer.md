# Descripcion
Download the packet capture file and use packet analysis software to find the flag.

-   [Download packet capture](https://artifacts.picoctf.net/c/196/network-dump.flag.pcap)

# Pistas
Wireshark, if you can install and use it, is probably the most beginner friendly packet analysis software product.

# Solucion
```                                                      
┌──(kali㉿kali)-[~/picoctf/2doparcial/forensic2022/packetsprimer]
└─$ wget https://artifacts.picoctf.net/c/196/network-dump.flag.pcap
--2023-05-06 17:39:07--  https://artifacts.picoctf.net/c/196/network-dump.flag.pcap
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.132.32, 18.154.132.74, 18.154.132.108, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.132.32|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 778 [application/octet-stream]
Saving to: ‘network-dump.flag.pcap’

network-dump.flag.pcap               100%[======================================================================>]     778  --.-KB/s    in 0s      

2023-05-06 17:39:08 (17.1 MB/s) - ‘network-dump.flag.pcap’ saved [778/778]

                                                                                                                                                    
┌──(kali㉿kali)-[~/picoctf/2doparcial/forensic2022/packetsprimer]
└─$ wireshark network-dump.flag.pcap   
p i c o C T F { p 4 c k 3 7 _ 5 h 4 r k _ 0 1 b 0 a 0 d 6 }
```

# Bandera
picoCTF{p4ck37_ 5h4rk _ 01b0a0d6}

# Notas adicionales
Para la solucion de este reto se hace la descarga del archivo que se proporciona en la descripción de el reto, se manda abrir con wireshark, ya en la herramienta se hace el seguimiento TCP y es así como se obtiene la bandera con la solución de este reto.

# Referencias