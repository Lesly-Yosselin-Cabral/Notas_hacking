# Descripcion
Run the Python script and convert the given number from decimal to binary to get the flag. [Download Python script](https://artifacts.picoctf.net/c/24/convertme.py)

# Pistas
1. Look up a decimal to binary number conversion app on the web or use your computer's calculator!
2. The `str_xor` function does not need to be reverse engineered for this challenge.
3. If you have Python on your computer, you can download the script normally and run it. Otherwise, use the `wget` command in the webshell.
4. To use `wget` in the webshell, first right click on the download link and select 'Copy Link' or 'Copy Link Address'
5. Type everything after the dollar sign in the webshell: `$ wget` , then paste the link after the space after `wget` and press enter. This will download the script for you in the webshell so you can run it!
6. Finally, to run the script, type everything after the dollar sign and then press enter: `$ python3 convertme.py`


# Solucion
```
──(kali㉿kali)-[~]
└─$ wget https://artifacts.picoctf.net/c/24/convertme.py
--2023-03-22 19:52:38--  https://artifacts.picoctf.net/c/24/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 99.84.203.40, 99.84.203.9, 99.84.203.115, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|99.84.203.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: ‘convertme.py’

convertme.py                     100%[========================================================>]   1.16K  --.-KB/s    in 0s      

2023-03-22 19:52:39 (24.3 MB/s) - ‘convertme.py’ saved [1189/1189]

                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ ls
convertme.py  Desktop    Downloads  flagout.txt  Music      otrotoken  Public       runme.py   Videos
cookie        Documents  flag       hacking      netcat.py  Pictures   repetitions  Templates
                                                                                                                                  
┌──(kali㉿kali)-[~]
└─$ python3 convertme.py 
If 87 is in decimal base, what is it in binary base?
Answer: 1010111
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_722f6b39}
```

# Bandera
picoCTF{4ll_y0ur_b4535_722f6b39}

# Notas adicionales


# Referencias