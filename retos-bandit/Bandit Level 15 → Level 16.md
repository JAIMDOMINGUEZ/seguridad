# Bandit Level 15 → Level 16

# Objetivos
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**
# Datos de acceso al nivel
```bach
bandit15
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
```
# Solucion
```bash
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Sep  9 01:47:01 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Sep  9 01:47:01 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Sep  9 01:46:01 2023 GMT; NotAfter: Sep  9 01:47:01 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEC3lb1TANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwOTA5MDE0NjAxWhcNMjMwOTA5MDE0NzAxWjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDE
6JvfXGuRLl9vhsp6vfdk+yRxsWQlE5vKo8PoOxofsNPdmOH2H5loItC0kRCLyZj5
Byaeg/T4RWDgmLdBLUqSsMTZoUAFKBepLFjYqULJ+fduZSntt2Z6YqZJTHWJ/zzX
ib5i9jktlX/FJxJFO6/ypjbEZX34QHrlZ2MQv2C7bHiccVUf1PlSbDHgTZ4kq8Hy
g6S7YpsC/ddwowzjVV10b0hqqw9XJEHesvKZYDyblnJdTLbiFbWI921el1WaQavu
/jsKT6AGZpgH3ouK7FSLCKO8fF0wA3/H+8CWoLyjuK4S130gKzpanQQ+RXVwcMyJ
6CdfNVCH4MCJ398ZnVi/AgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQCZ
AD6KmVr+auzrS6J5rA6i+tCNsCJnTJVfZHETouLgd9iFd8TvJCPaTxI8w91Zuk8b
kUpfW7ZRhkYP3K8w4iqogg+73DHVCVhMd1zGRL//HF3IKtmNrEv0nNSrrscEgepS
m/XGyFsmgXzUTmZ/0eghVGE7fMHRbO8e9ITjqlvRMcZN4ycm1o0KTfc0Awem7dro
oF6a+La5KLsuexubxO6y+uf87seLwWcR6WagszJSJPCCpCnCjEXzAPqu0nXfLBlY
IjA8qJh5ZTeL4CVxWNilpZ/bZWv9V74FsVCDHnhE+DRB1ZflEPar+nqT7AncnVbN
FJSTxHOxfdwiZ/xygyem
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
    Session-ID: 54EC91021C32D912ED64DF2FB849CC96B55DE34CB2EF080009CAE74DEDCB0C32
    Session-ID-ctx:
    Resumption PSK: E8410F20B55C91759A2183F9C984AD38DC0DC2A62F19F5F61D2780DE177B5B8A10DAEECC2FC2A9A78E5A99BCF6CD26D2
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 62 90 a4 d2 27 7d 99 5e-76 c8 b5 05 9d 67 2a 03   b...'}.^v....g*.
    0010 - 06 ac 88 51 6a 63 2d 60-3f 48 91 81 12 c4 a6 c2   ...Qjc-`?H......
    0020 - 7c ef 35 dd 74 52 ac 38-6d 35 c1 23 66 12 da 2e   |.5.tR.8m5.#f...
    0030 - 7c d5 39 02 a3 ea 92 f7-8c 15 d1 6d ce 9b 1d 45   |.9........m...E
    0040 - 6a df ec ce 64 d1 77 d9-ff fc ba ac f6 e7 4d 9a   j...d.w.......M.
    0050 - cd 9a c9 d4 9d 8b 5c 3e-57 3b 18 14 4b e1 f9 cb   ......\>W;..K...
    0060 - 13 08 b6 a2 9b 1f 92 0e-a6 4f d0 63 b9 72 f2 35   .........O.c.r.5
    0070 - 40 c3 bd 2f 89 7a 76 9b-f8 6d cb f1 08 4d 3a 03   @../.zv..m...M:.
    0080 - 62 af ba 32 b0 39 1c c8-c1 b6 f1 4b d0 c4 c5 b0   b..2.9.....K....
    0090 - 02 fe fd 3a 1f 0a ab 9a-2a a4 18 64 23 68 9c 5f   ...:....*..d#h._
    00a0 - 11 bb ab 89 6a c5 6b 2f-3c b2 80 17 54 64 d0 74   ....j.k/<...Td.t
    00b0 - f2 6d 84 84 58 d2 9c 8b-06 c9 fa 6a e6 82 fe 25   .m..X......j...%
    00c0 - d9 39 1d 48 1a 3b ae 62-82 58 60 f2 d0 8a 62 0a   .9.H.;.b.X`...b.

    Start Time: 1694235274
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
    Session-ID: 135A940B3471629B7B88D3F44783376DE7C96333098BBBA8CCE8AE7B47626F25
    Session-ID-ctx:
    Resumption PSK: 1BCFC565F4DE6C6521529DB5C89338F719C2AE8DEAFC3470BE114409116F4E1C5B0C021A665F902488B6F98222F4DD40
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 62 90 a4 d2 27 7d 99 5e-76 c8 b5 05 9d 67 2a 03   b...'}.^v....g*.
    0010 - 8f 7f b6 08 bb c2 1a b0-cb 1a 86 6d 20 dc bd a2   ...........m ...
    0020 - 52 e5 25 8f cf 6f 44 fe-e0 68 e3 87 0d eb 9c 1d   R.%..oD..h......
    0030 - 38 80 71 2b f9 28 2e ca-94 7e 49 22 cc c0 d4 f7   8.q+.(...~I"....
    0040 - 0f a3 ee 33 19 05 86 5b-f3 a9 a2 b2 b2 66 d2 ca   ...3...[.....f..
    0050 - 7f 0b a2 35 88 a0 c4 58-14 8d ea d1 a6 28 7d 92   ...5...X.....(}.
    0060 - 98 2f 6b 06 14 99 a4 db-3e 4a d9 16 b7 5e 40 a4   ./k.....>J...^@.
    0070 - 7c 54 f1 91 76 9e 87 83-7b 3d 33 ce 4c 9d 81 7e   |T..v...{=3.L..~
    0080 - 24 f8 09 bc 82 aa 73 69-82 0b ab 8e 3f d8 18 e1   $.....si....?...
    0090 - 27 a1 9e f1 31 e8 ca 36-8a 11 32 9e e2 13 e5 99   '...1..6..2.....
    00a0 - 96 fd b1 a2 06 44 fe 7f-3c 7c f6 75 c0 2a 37 72   .....D..<|.u.*7r
    00b0 - 3f b6 55 b5 29 4b 71 80-c5 e9 66 05 c9 87 f5 b7   ?.U.)Kq...f.....
    00c0 - 11 4f b4 16 58 29 fc 44-1c 83 81 45 fb 46 90 60   .O..X).D...E.F.`

    Start Time: 1694235274
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


# Notas adicionales
|Comando|Descripcion|
|---|---|
|openssl | OpenSSL es una herramienta y una biblioteca de código abierto ampliamente utilizada en sistemas operativos Linux y otros sistemas Unix-like. OpenSSL se utiliza principalmente para implementar protocolos de seguridad, cifrar y descifrar datos, y realizar operaciones criptográficas en general


# Referencias
