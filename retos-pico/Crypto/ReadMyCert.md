# ReadMyCert
# Objetivos
How about we take you on an adventure on exploring certificate signing requestsTake a look at this CSR file [here](https://artifacts.picoctf.net/c/426/readmycert.csr).
# Solucion
```bash
──(kali㉿kali)-[~/Documents/crypto/ReadMyCert]
└─$ openssl req -in readmycert.csr -noout -text
Certificate Request:
    Data:
        Version: 1 (0x0)
        Subject: CN = picoCTF{read_mycert_41d1c74c}, name = ctfPlayer
        Subject Public Key Info:
            Public Key Algorithm: rsaEncryption
                Public-Key: (2048 bit)
                Modulus:
                    00:e7:5c:0e:3d:bf:9b:52:f1:06:b5:db:dd:c8:7d:
                    fb:60:6d:29:dd:db:f0:d1:67:e1:44:97:03:92:4e:
                    44:f7:de:19:c0:dd:21:7e:15:4a:24:6
```

# Notas adicionales
- `openssl`
    
    Esta es la herramienta de línea de comandos utilizada para realizar varias operaciones criptográficas utilizando la biblioteca OpenSSL.
    
- Opción: `req`
    
    Es un subcomando de OpenSSL utilizado específicamente para trabajar con solicitudes de certificados, incluidas las CSR.
    
- Opción: `-in `
    
    Este indicador especifica el archivo de entrada para la CSR. 
    
- Opción: `-noout`
 
    Este indicador indica a OpenSSL que no emita el certificado real, sino que solo muestre la representación de texto CSRR. Impide generar cualquier salida que no sea la información textual.
    
- Opción: `-text`
    
    Esta bandera le dice a OpenSSL que muestre los detalles de CSR en un formato legible por humanos. Proporciona una visión completa de los contenidos de las CSRR, incluido el nombre distinguido de los sujetos (DN), la información de clave pública y cualquier otro atributo incluido en la solicitud.
# Referencias
