#  Crack 1 
# Objetivos
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/10/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/10/level1.flag.txt.enc) in the same directory too.

# Solucion
```bash
james-backster-picoctf@webshell:~$ ls
level1.flag.txt.enc  level1.py
james-backster-picoctf@webshell:~$ cat level1.flag.txt.enc 
FPR
   umw
iK
_i
  UDjames-backster-picoctf@webshell:~$ python level1.py 
Please enter correct password for flag: FPR
That password is incorrect
james-backster-picoctf@webshell:~$ python level1.py 
Please enter correct password for flag: umw
That password is incorrect
james-backster-picoctf@webshell:~$ python level1.py 
Please enter correct password for flag: ik
That password is incorrect
james-backster-picoctf@webshell:~$ python level1.py 
Please enter correct password for flag: _i
That password is incorrect
james-backster-picoctf@webshell:~$ cat level1.py 
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

flag_enc = open('level1.flag.txt.enc', 'rb').read()


def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "691d"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_1_pw_check()
james-backster-picoctf@webshell:~$ python level1.py 
Please enter correct password for flag: 691d
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_56891419}
james-backster-picoctf@webshell:~$ 
```

# Notas adicionales
La bandera estaba escrita dentro del programa level1.py en una comparación

# Referencias
