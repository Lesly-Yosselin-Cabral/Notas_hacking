# Descripcion
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/b4d62f6e431dc8e563309ea8c33a06b3/cat.jpg)


# Pistas
1. Look at the details of the file
2. Make sure to submit the flag as picoCTF{XXXXX}

# Solucion
```
┌──(kali㉿kali)-[~/picoctf/2doparcial/forensic2021/information]
└─$ wget https://mercury.picoctf.net/static/b4d62f6e431dc8e563309ea8c33a06b3/cat.jpg          
--2023-05-06 15:59:34--  https://mercury.picoctf.net/static/b4d62f6e431dc8e563309ea8c33a06b3/cat.jpg
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 878136 (858K) [application/octet-stream]
Saving to: ‘cat.jpg’

cat.jpg                              100%[======================================================================>] 857.55K  1.20MB/s    in 0.7s    

2023-05-06 15:59:36 (1.20 MB/s) - ‘cat.jpg’ saved [878136/878136]

┌──(kali㉿kali)-[~/picoctf/2doparcial/forensic2021/information]
└─$ 
** (ristretto:21227): WARNING **: 16:01:39.425: (file.c:619):rstto_file_get_thumbnail: code should not be reached
                                                                      
                                                                                                                                                    
┌──(kali㉿kali)-[~/picoctf/2doparcial/forensic2021/information]
└─$ exiftool cat.jpg                                                      
ExifTool Version Number         : 12.57
File Name                       : cat.jpg
Directory                       : .
File Size                       : 878 kB
File Modification Date/Time     : 2021:03:15 14:24:46-04:00
File Access Date/Time           : 2023:05:06 16:00:49-04:00
File Inode Change Date/Time     : 2023:05:06 15:59:36-04:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.02
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Current IPTC Digest             : 7a78f3d9cfb1ce42ab5a3aa30573d617
Copyright Notice                : PicoCTF
Application Record Version      : 4
XMP Toolkit                     : Image::ExifTool 10.80
License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
Rights                          : PicoCTF
Image Width                     : 2560
Image Height                    : 1598
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 2560x1598
Megapixels                      : 4.1
                                                                  
picoCTF{the_m3tadata_1s_modified}

```

# Bandera
picoCTF{the_m3tadata_1s_modified}

# Notas adicionales
Comando -> exiftool = manipular metadatos de imágenes

# Referencias
https://gchq.github.io/CyberChef/