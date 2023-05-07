# Descripcion
This vault uses for-loops and byte arrays. The source code for this vault is here: [VaultDoor3.java](https://jupiter.challenges.picoctf.org/static/943ea40e3f54fca6d2145fa7aadc5e09/VaultDoor3.java)


# Pistas
Make a table that contains each value of the loop variables and the corresponding buffer index that it writes to.

# Solucion
```
allow pasting
Uncaught SyntaxError: unexpected token: identifier
var password = "jU5t_a_sna_3lpm18g947_u_4_m9r54f"
undefined
var buffer = Array(32);
undefined
> for (i=0; i<8; i++) {
        buffer[i] = password.charAt(i);
}                                                                                                              for (; i<16; i++){
    buffer[1] = password.charAt(23-1);..****
```

# Bandera
picoCTF{jU5t_a_sImpl3_an4gr4m_4_ulfb380}

# Notas adicionales


# Referencias
https://www.youtube.com/watch?v=B5y2spPIXj0&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=49
