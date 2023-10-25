# Lookey here
# Objetivos
Attackers have hidden information in a very large mass of data in the past, maybe they are still doing it.Download the data [here](https://artifacts.picoctf.net/c/125/anthem.flag.txt).
# Solucion
```bash
──(kali㉿kali)-[~/Documents/forense/lookey]
└─$ ls
anthem.flag.txt  anthem.flag.txt.1
                                                                                                               
┌──(kali㉿kali)-[~/Documents/forense/lookey]
└─$ diff anthem.flag.txt anthem.flag.txt
                                                                                                               
┌──(kali㉿kali)-[~/Documents/forense/lookey]
└─$ grep "pico" anthem.flag.txt
      we think that the men of picoCTF{gr3p_15_@w3s0m3_58f5c024}
                                                                                                               
┌──(kali㉿kali)-[~/Documents/forense/lookey]
└─$ 

```

# Notas adicionales

# Referencias
