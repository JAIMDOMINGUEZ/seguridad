# Mind your Ps and Qs
# Objetivos
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/3cfeb09681369c26e3f19d886bc1e5d9/values)
# Solucion
```bash
┌──(kali㉿kali)-[~/Documents/crypto/mindyourpsand]
└─$ python
Python 3.11.4 (main, Jun  7 2023, 10:13:09) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from Crypto.Util.number import inverse, long_to_bytes
>>> from Crypto.Util.number import inverse, long_to_bytes
>>> 
>>> c= 8533139361076999596208540806559574687666062896040360148742851107661304651861689
>>> n= 769457290801263793712740792519696786147248001937382943813345728685422050738403253
>>> e= 65537  
>>> p=1617549722683965197900599011412144490161
>>> q=475693130177488446807040098678772442581573
>>> n=p*q
>>> print(n)
769457290801263793712740792519696786147248001937382943813345728685422050738403253
>>> tn = (p-1)*(q-1)
>>> 
>>> d = inverse(e, tn)
>>> 
>>> m = pow(c,d,n)
>>> 
>>> print(long_to_bytes(m))
b'picoCTF{sma11_N_n0_g0od_45369387}'

```

# Notas adicionales

# Referencias
