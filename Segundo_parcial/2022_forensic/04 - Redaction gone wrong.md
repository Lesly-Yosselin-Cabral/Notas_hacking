# Descripcion
Now you DON’T see me. This [report](https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?

# Pistas
How can you be sure of the redaction?

# Solucion
```
┌──(kali㉿kali)-[~/picoctf/2doparcial/forensic2022/redctiongonewrong]
└─$ wget https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf
--2023-05-06 17:48:53--  https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.132.88, 18.154.132.108, 18.154.132.74, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.132.88|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34915 (34K) [application/octet-stream]
Saving to: ‘Financial_Report_for_ABC_Labs.pdf’

Financial_Report_for_ABC_Labs.pdf    100%[======================================================================>]  34.10K  --.-KB/s    in 0.07s   

2023-05-06 17:48:55 (478 KB/s) - ‘Financial_Report_for_ABC_Labs.pdf’ saved [34915/34915]

                                                                                                                                                    
┌──(kali㉿kali)-[~/picoctf/2doparcial/forensic2022/redctiongonewrong]
└─$ open Financial_Report_for_ABC_Labs.pdf 

┌──(kali㉿kali)-[~/picoctf/2doparcial/forensic2022/redctiongonewrong]
└─$ pdftotext Financial_Report_for_ABC_Labs.pdf 
                                                                                                                                                    
┌──(kali㉿kali)-[~/picoctf/2doparcial/forensic2022/redctiongonewrong]
└─$ ls
Financial_Report_for_ABC_Labs.pdf  Financial_Report_for_ABC_Labs.txt
┌──(kali㉿kali)-[~/picoctf/2doparcial/forensic2022/redctiongonewrong]
└─$ cat Financial_Report_for_ABC_Labs.txt 
Financial Report for ABC Labs, Kigali, Rwanda for the year 2021.
Breakdown - Just painted over in MS word.

Cost Benefit Analysis
Credit Debit
This is not the flag, keep looking
Expenses from the
picoCTF{C4n_Y0u_S33_m3_fully}
Redacted document.

```

# Bandera
picoCTF{C4n_Y0u_S33_m3_fully}

# Notas adicionales
Para la solución de este reto se hizo la descarga el documento Pdf que se proporciona en la descripción de el reto, se manda abrir pero no se obseva nada que nos pueda ayudar a encontrar la bandera, entonces con la ayuda de la funcion pdftotext  que nos ayuda a convertir archivos PDF a archivos de texto simple mandamos hacer una copia de el archivo .pdf ahora con extención .txt, se manda abrir con el comando cat y es así como se obtiene la bandera para la solución de este reto.

# Referencias