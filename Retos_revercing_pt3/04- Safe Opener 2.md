# Descripcion
What can you do with this file?I forgot the key to my safe but this [file](https://artifacts.picoctf.net/c/290/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?

# Pistas
Download and try to decompile the file.

# Solucion
```
┌──(kali㉿kali)-[~/picoctf/revercing/safeopener2]
└─$ wget https://artifacts.picoctf.net/c/290/SafeOpener.class
--2023-05-10 00:34:04--  https://artifacts.picoctf.net/c/290/SafeOpener.class
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.132.74, 18.154.132.88, 18.154.132.32, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.132.74|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2036 (2.0K) [application/octet-stream]
Saving to: ‘SafeOpener.class’

SafeOpener.class                         100%[===============================================================================>]   1.99K  --.-KB/s    in 0s      

2023-05-10 00:34:04 (56.2 MB/s) - ‘SafeOpener.class’ saved [2036/2036]

                                                                                                                                                                 
┌──(kali㉿kali)-[~/picoctf/revercing/safeopener2]
└─$ open SafeOpener.class    

import java.io.IOException;

import java.util.Base64;

import java.io.Reader;

import java.io.BufferedReader;

import java.io.InputStreamReader;

  

//

// Decompiled by Procyon v0.5.36

//

  

public class SafeOpener

{

public static void main(final String[] args) throws IOException {

final BufferedReader keyboard = new BufferedReader(new InputStreamReader(System.in));

final Base64.Encoder encoder = Base64.getEncoder();

String encodedkey = "";

String key = "";

for (int i = 0; i < 3; ++i) {

System.out.print("Enter password for the safe: ");

key = keyboard.readLine();

encodedkey = encoder.encodeToString(key.getBytes());

System.out.println(encodedkey);

final boolean isOpen = openSafe(encodedkey);

if (isOpen) {

break;

}

System.out.println("You have " + (2 - i) + " attempt(s) left");

}

}

public static boolean openSafe(final String password) {

final String encodedkey = "picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_7db9fb8c}";

if (password.equals(encodedkey)) {

System.out.println("Sesame open");

return true;

}

System.out.println("Password is incorrect\n");

return false;

}

}

┌──(kali㉿kali)-[~/picoctf/revercing/safeopener2]
└─$ javac SafeOpener.java 
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
                                                                                                                                                                 
┌──(kali㉿kali)-[~/picoctf/revercing/safeopener2]
└─$ java SafeOpener      
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
Enter password for the safe: picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_7db9fb8c}
cGljb0NURntTQWYzXzBwM24zcnJfeTB1X3NvbHYzZF9pdF83ZGI5ZmI4Y30=
Password is incorrect

```

# Bandera
picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_7db9fb8c}

# Notas adicionales


# Referencias
https://www.youtube.com/watch?v=d32kAPLLgmA