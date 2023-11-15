# SRA
# Objetivos
I just recently learnt about the SRA public key cryptosystem... or wait, was it supposed to be RSA? Hmmm, I should probably check...
Additional details will be available after launching your challenge instance.
# Solucion
```bash
┌──(kali㉿kali)-[~/Documents/crypto/sra]
└─$ cat rv.py   
from Crypto.Util.number import isPrime, long_to_bytes
from string import ascii_letters, digits
from itertools import combinations
from sympy import divisors
from math import log2

anger = int(input("anger = "))
envy = int(input("envy = "))
sloth = 65537

ds = divisors(envy * sloth - 1)
primes = [x + 1 for x in ds if isPrime(x + 1)]
correct_size_primes = [x for x in primes if log2(x) // 1 == 127]

valid_plaintexts = []
charset = ascii_letters + digits
for p, q in combinations(correct_size_primes, 2):
    try:
        s = long_to_bytes(pow(anger, envy, p * q)).decode("ascii")
        if all([c in charset for c in s]):
            valid_plaintexts.append(s)
    except Exception:
        continue

print(valid_plaintexts)

┌──(kali㉿kali)-[~/Documents/crypto/sra]
└─$ nc saturn.picoctf.net 57534
anger = 21400542010048240341426734732356976930493903475200030313600669783656940593199
envy = 76461608315400997163345511254231569886488988393611042497755067584127107477729
vainglory?
> qTSe1XSEuSy6TEyR
qTSe1XSEuSy6TEyR
Conquered!
picoCTF{7h053_51n5_4r3_n0_m0r3_0795e891}

```

# Notas adicionales

# Referencias
