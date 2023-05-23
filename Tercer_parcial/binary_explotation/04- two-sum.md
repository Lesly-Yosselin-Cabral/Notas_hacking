# Descripcion
Can you solve this?What two positive numbers can make this possible: `n1 > n1 + n2 OR n2 > n1 + n2`Enter them here `nc saturn.picoctf.net 58638`. [Source](https://artifacts.picoctf.net/c/456/flag.c)


# Pistas
1. Integer overflow
2. Not necessarily a math problem
# Solucion
```
┌──(kali㉿kali)-[~/picoctf/3erparcial/binaryexplotation/twosum]
└─$ wget https://artifacts.picoctf.net/c/456/flag.c     
--2023-05-22 22:46:31--  https://artifacts.picoctf.net/c/456/flag.c
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.132.108, 18.154.132.74, 18.154.132.88, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.132.108|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1346 (1.3K) [application/octet-stream]
Saving to: ‘flag.c’

flag.c                   100%[===============================>]   1.31K  --.-KB/s    in 0s      

2023-05-22 22:46:32 (31.0 MB/s) - ‘flag.c’ saved [1346/1346]

                                                                                                 
┌──(kali㉿kali)-[~/picoctf/3erparcial/binaryexplotation/twosum]
└─$ code . flag.c          
┏━(Message from Kali developers)
┃ code is not the binary you may be expecting.
┃ You are looking for \"code-oss\"
┃ Starting code-oss for you...
┗━
libva error: vaGetDriverNameByIndex() failed with unknown libva error, driver_name = (null)
[38075:0522/224657.928693:ERROR:gpu_memory_buffer_support_x11.cc(44)] dri3 extension not supported.
[main 2023-05-23T02:46:58.587Z] update#ctor - updates are disabled as there is no update URL
[main 2023-05-23T02:47:03.539Z] Starting extension host with pid 38218 (fork() took 26 ms).


#include <stdio.h>

#include <stdlib.h>

  

static int addIntOvf(int result, int a, int b) {

result = a + b;

if(a > 0 && b > 0 && result < 0)

return -1;

if(a < 0 && b < 0 && result > 0)

return -1;

return 0;

}

  

int main() {

int num1, num2, sum;

FILE *flag;

char c;

  

printf("n1 > n1 + n2 OR n2 > n1 + n2 \n");

fflush(stdout);

printf("What two positive numbers can make this possible: \n");

fflush(stdout);

if (scanf("%d", &num1) && scanf("%d", &num2)) {

printf("You entered %d and %d\n", num1, num2);

fflush(stdout);

sum = num1 + num2;

if (addIntOvf(sum, num1, num2) == 0) {

printf("No overflow\n");

fflush(stdout);

exit(0);

} else if (addIntOvf(sum, num1, num2) == -1) {

printf("You have an integer overflow\n");

fflush(stdout);

}

  

if (num1 > 0 || num2 > 0) {

flag = fopen("flag.txt","r");

if(flag == NULL){

printf("flag not found: please run this on the server\n");

fflush(stdout);

exit(0);

}

char buf[60];

fgets(buf, 59, flag);

printf("YOUR FLAG IS: %s\n", buf);

fflush(stdout);

exit(0);

}

}

return 0;

}


```

# Bandera
picoCTF{}

# Notas adicionales


# Referencias