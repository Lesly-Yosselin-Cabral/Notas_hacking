# Descripcion
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Download the assembly dump [here](https://artifacts.picoctf.net/c/530/disassembler-dump0_c.txt).


# Pistas
Not everything in this disassembly listing is optimal.

# Solucion
```
┌──(kali㉿kali)-[~/picoctf/3erparcial/reversing/bit-o-asm-3]
└─$ wget https://artifacts.picoctf.net/c/530/disassembler-dump0_c.txt
--2023-05-22 22:08:37--  https://artifacts.picoctf.net/c/530/disassembler-dump0_c.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.132.88, 18.154.132.32, 18.154.132.108, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.132.88|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 461 [application/octet-stream]
Saving to: ‘disassembler-dump0_c.txt’

disassembler-dump0_c.txt 100%[===============================>]     461  --.-KB/s    in 0s      

2023-05-22 22:08:38 (426 MB/s) - ‘disassembler-dump0_c.txt’ saved [461/461]

                                                                                                 
┌──(kali㉿kali)-[~/picoctf/3erparcial/reversing/bit-o-asm-3]
└─$ cat disassembler-dump0_c.txt
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x14],edi
<+11>:    mov    QWORD PTR [rbp-0x20],rsi
<+15>:    mov    DWORD PTR [rbp-0xc],0x9fe1a
<+22>:    mov    DWORD PTR [rbp-0x8],0x4
<+29>:    mov    eax,DWORD PTR [rbp-0xc]
<+32>:    imul   eax,DWORD PTR [rbp-0x8]
<+36>:    add    eax,0x1f5
<+41>:    mov    DWORD PTR [rbp-0x4],eax
<+44>:    mov    eax,DWORD PTR [rbp-0x4]
<+47>:    pop    rbp
<+48>:    ret

```

# Bandera
picoCTF{}

# Notas adicionales


# Referencias