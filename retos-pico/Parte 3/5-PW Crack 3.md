#  PW Crack 3 
# Objetivos
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/16/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/16/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/16/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

# Solucion
```bash
james-backster-picoctf@webshell:~$ nano level3.py
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


flag_enc = open('level3.flag.txt.enc', 'rb').read()
correct_pw_hash = open('level3.hash.bin', 'rb').read()

def hash_pw(pw_str):
    pw_bytes = bytearray()
    pw_bytes.extend(pw_str.encode())
    m = hashlib.md5()
    m.update(pw_bytes)
    return m.digest()
def level_3_pw_check():
    pos_pw_list = ["6997", "3ac8", "f0ac", "4b17", "ec27", "4e66", "865e"]
    for x in pos_pw_list:
        user_pw_hash = hash_pw(x)    
        if user_pw_hash == correct_pw_hash:
            print("Welcome back... your flag, user:")
            decryption = str_xor(flag_enc.decode(), x)  # Replace 'user_pw' with 'x'
            print(decryption)

level_3_pw_check()
james-backster-picoctf@webshell:~$ python level3.py
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_2b072a90}
james-backster-picoctf@webshell:~$ 
```

# Notas adicionales
Modifique el programa para que en lugar de preguntar la contraseña itere por si solo entre la lista de contraseñas hasta encontrar la correcta
# Referencias
