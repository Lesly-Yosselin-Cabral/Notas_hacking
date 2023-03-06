## Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

## Datos de acceso
contraseña: EN632PlfYiZbn3PhVK3XOGSlNInNE00t

## Solución
```
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ wc data.txt
   50   414 19379 data.txt
bandit9@bandit:~$ file data.txt
data.txt: data
bandit9@bandit:~$ strings data.txt | grep ==
f========== theM
========== password
========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```

## Notas adicionales

## Referencias