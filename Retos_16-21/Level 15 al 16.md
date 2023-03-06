## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**

## Datos de acceso
contraseña: jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

## Solución
```
bandit15@bandit:~$ openssl s_client connect localhost:30001
s_client: Use -help for summary.
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 21 06:20:29 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 21 06:20:29 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 21 06:19:29 2023 GMT; NotAfter: Feb 21 06:20:29 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEA7qUdzANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjIxMDYxOTI5WhcNMjMwMjIxMDYyMDI5WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDL
vM0gZzAHdXTeD5t4ruUJo/kRs4UAodA9XcqDhNtW464W0c55RqKLp921syy3Lvjr
8Q9WkqvCFX+efShMd8XnzbT/dyRrD+cZQnSiPJ3bwDdpwqfkl9h3mb609Kb5HI6R
JgogEyuRLJI+HKtr/wXHwo1vBZ0+yaPMX6sdkd6Hu5Ra0L5Q5+E5+3F/8QgvCeVE
hDRIOrh2a7jxykb8G6+xVC6jIZY0YfrZz6LrESyQau256pqyaQPqQoUWTlitxIql
Ym2Baw7vYDxmFZrvj0FkumC6NokX6K2G9bZ0DaKR/DspPdAC4oT81SawJvsBibdN
51VI6dxBn412ZS8bS155AgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQA9
skxWNwZbedjaVTa5yMPUZQ4Nf5/LAAMtS5Q7mzGH5tdQsTGR0Z4n4eA4hzrmzHBF
MVRL5mR9n+sM5pIrKDa6f4zIc5ObxDyN19ie+3SFASCPz9tihK8Js2V8qsR6LHV1
pfD8DSG0hZPtUuK3Mfi+nWqQUFiiTGj30mb9vlS1sSWv5PGznou1gQ3ZfrDs7B4K
ZKZrllPIVV1CrlDw2Bv8Dc432LQuZAmKAjBd6FG0OAboU/WJMTwAfVjlKMtvC8tg
DZ3djSTprq6PrXlI0utw/MsMIh69b61BRXUuDvRxhU11SNmSI8aegjVL8KuK+Euh
sSLPTocV29SY1YXOwEQi
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 01D223A7042FCBFB78AC2FAFCF31AA4BF74053804F03F46667A9929B347D4B8F
    Session-ID-ctx:
    Resumption PSK: 6FDC8C1E4A4D85A1F8D4C9C5B76B9AD694078513B168C09BE670CF02DD9BF2EA384F6765CE80697CA5B14F7A1A0953A1
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - ee ae 09 e4 56 06 6c 9e-c9 80 86 77 50 83 15 59   ....V.l....wP..Y
    0010 - 34 d8 19 17 87 c2 5a 5f-be e9 08 9b 5a 45 4a 30   4.....Z_....ZEJ0
    0020 - 9a ce b9 c1 f5 53 22 93-7b 40 a8 5e 3e e1 ea db   .....S".{@.^>...
    0030 - 01 30 39 60 22 07 1b 6a-3f 02 85 f5 2c e2 13 97   .09`"..j?...,...
    0040 - b5 40 fe 41 ab 1b 52 b8-3b a6 f7 1f 1f dc 16 f2   .@.A..R.;.......
    0050 - 44 9c 03 3a ba 01 77 5a-c8 5f 83 c9 a8 b2 ec b4   D..:..wZ._......
    0060 - e3 18 37 ca a4 ce 0f 4f-b3 03 4f dc 68 b0 64 71   ..7....O..O.h.dq
    0070 - b5 af a9 67 e3 34 a2 91-4f c0 a0 15 3e 25 98 38   ...g.4..O...>%.8
    0080 - 26 0e a7 86 e0 9d 40 a4-7c 45 a0 c3 c7 b6 10 3f   &.....@.|E.....?
    0090 - cb 38 54 b6 da b8 7a 5d-4f 60 d3 6b 0d ad cb 34   .8T...z]O`.k...4
    00a0 - e1 69 4c 30 22 60 b2 7f-35 59 ad 24 a6 e8 a9 47   .iL0"`..5Y.$...G
    00b0 - 60 e4 99 de 8c 8f 1a 03-69 a0 83 eb ec 8b fe 85   `.......i.......
    00c0 - 2e 94 f9 17 37 ae 1f 00-ed 55 55 5d ad b4 96 07   ....7....UU]....

    Start Time: 1677007692
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 2D31F6FBCC9149E667DF98A46B78DAEC5A69D4EC3ECBF345FB45BB8D88E82C3E
    Session-ID-ctx:
    Resumption PSK: 8160C0C8E149FEDA871C8DCE7956BA80B31BA217EF05554D2DE2B89311AA8A2E884BBBB639EDCCFAEB4B952C8A520178
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - ee ae 09 e4 56 06 6c 9e-c9 80 86 77 50 83 15 59   ....V.l....wP..Y
    0010 - 8c 60 fa e6 7c 82 88 fe-c0 dc 44 e8 74 86 ec 6e   .`..|.....D.t..n
    0020 - 12 53 0b 5d ec b5 bd 56-2e be cb 82 23 c6 d5 80   .S.]...V....#...
    0030 - bd 2e 3b a9 40 f3 1e af-36 86 83 47 99 bd ae dd   ..;.@...6..G....
    0040 - 1a 09 27 5b 24 db da df-b1 b4 89 d9 07 a4 60 5e   ..'[$.........`^
    0050 - 51 ed 15 68 52 c1 60 da-86 a1 60 8c 71 28 98 3c   Q..hR.`...`.q(.<
    0060 - 3b 1c ca 25 42 44 2f 22-c1 71 8b 63 dc 0d 4e 1b   ;..%BD/".q.c..N.
    0070 - f7 9c 18 a8 95 f1 a4 f4-c1 b9 09 af fd 18 a9 5d   ...............]
    0080 - 52 57 9d 3a 59 59 5b fb-20 f7 a3 9a f4 b9 0a c3   RW.:YY[. .......
    0090 - 9a 09 a7 86 4d 4d a2 a3-a0 e4 bb 4a 20 83 6c 70   ....MM.....J .lp
    00a0 - 15 ba 73 67 e6 d9 d2 5d-71 ce e7 4a e6 0a b8 4a   ..sg...]q..J...J
    00b0 - 44 db 03 1e ad c0 69 73-f8 4c d4 0d 6a ea c4 56   D.....is.L..j..V
    00c0 - d0 50 2d f3 dc ed 33 38-96 70 14 d3 4f 5d fe 33   .P-...38.p..O].3

    Start Time: 1677007692
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed

```

## Notas adicionales

## Referencias