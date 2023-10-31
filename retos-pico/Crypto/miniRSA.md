# miniRSA
# Objetivos
Let's decrypt this: [ciphertext](https://jupiter.challenges.picoctf.org/static/eb5e6df8e14c52873cf88c582a1a4008/ciphertext)? Something seems a bit small.
# Solucion
```bash
┌──(kali㉿kali)-[~/Documents/crypto/minirsa]
└─$ cat ciphertext 
┌──(kali㉿kali)-[~]
└─$ python
Python 3.11.4 (main, Jun  7 2023, 10:13:09) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from gmpy2 import *
>>> from Crypto.Util.number import long_to_bytes
>>> gmpy2.get_context().precision=2048
>>> e=3
>>> c= 2205316413931134031074603746928247799030155221252519872650080519263755075355825243327515211479747536697517688468095325517209911688684309894900992899707504087647575997847717180766377832435022794675332132906451858990782325436498952049751141
>>> root, exact = iroot(c,e)
>>> root
mpz(13016382529449106065894479374027604750406953699090365388203722801043052339225981)
>>> print(long_to_bytes(root) )

picoCTF{n33d_a_lArg3r_e_d0cd6eae}
```

# Notas adicionales

# Referencias
