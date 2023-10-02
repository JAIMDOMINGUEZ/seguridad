#  PW Crack 5
# Objetivos
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/31/level5.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/31/level5.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/31/level5.hash.bin) in the same directory too. Here's a [dictionary](https://artifacts.picoctf.net/c/31/dictionary.txt) with all possible passwords based on the password conventions we've seen so far.

# Solucion
```bash
 james-backster-picoctf@webshell:~$ nano level5.py 
  GNU nano 6.2                                                              level5.py                                                                       
import hashlib

### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################

flag_enc = open('level5.flag.txt.enc', 'rb').read()
correct_pw_hash = open('level5.hash.bin', 'rb').read()


def hash_pw(pw_str):
    pw_bytes = bytearray()
    pw_bytes.extend(pw_str.encode())
    m = hashlib.md5()
    m.update(pw_bytes)
    return m.digest()


def level_5_pw_check():
    with open('dictionary.txt') as f:
        lines = f.readlines() 
        for x in lines:
	        x=x.strip()
            user_pw_hash = hash_pw(x)  
            if user_pw_hash == correct_pw_hash:
                print("Welcome back... your flag, user:")
                decryption = str_xor(flag_enc.decode(), x)
                print(decryption)

level_5_pw_check()
james-backster-picoctf@webshell:~$ python level5.py 
Welcome back... your flag, user:
picoCTF{h45h_sl1ng1ng_36e992a6}
```

# Notas adicionales
Edite el programa para que en lugar de solicitar la contraseña, la lea y compare directamente desde el diccionario y una vez encuentre la correcta me arroje la bandera 
# Referencias
