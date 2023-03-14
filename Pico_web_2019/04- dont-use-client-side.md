# Descripcion
Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/29835/` ([link](https://jupiter.challenges.picoctf.org/problem/29835/)) or http://jupiter.challenges.picoctf.org:29835

# Pistas
Never trust the client

# Solucion
```
function verify() {

checkpass = document.getElementById("pass").value;

split = 4;

if (checkpass.substring(0, split) == 'pico') {

if (checkpass.substring(split*6, split*7) == '723c') {

if (checkpass.substring(split, split*2) == 'CTF{') {

if (checkpass.substring(split*4, split*5) == 'ts_p') {

if (checkpass.substring(split*3, split*4) == 'lien') {

if (checkpass.substring(split*5, split*6) == 'lz_7') {

if (checkpass.substring(split*2, split*3) == 'no_c') {

if (checkpass.substring(split*7, split*8) == 'e}') {

alert("Password Verified")

}
```

# Bandera
picoCTF{no_clients_plz_7723ce}

# Notas adicionales


# Referencias
https://www.youtube.com/watch?v=19Hkmb1Guzk&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=4