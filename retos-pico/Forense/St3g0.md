# St3g0
# Objetivos
Download this image and find the flag.

- [Download image](https://artifacts.picoctf.net/c/216/pico.flag.png)
# Solucion
```bash
──(kali㉿kali)-[~/Documents/forense/St3g0]
└─$ zsteg -a -v pico.flag.png | grep "pico"


b1,rgb,lsb,xy       .. text: "picoCTF{7h3r3_15_n0_5p00n_a1062667}$t3g0"
    00000000: 70 69 63 6f 43 54 46 7b  37 68 33 72 33 5f 31 35  |picoCTF{7h3r3_15|

```

# Notas adicionales

# Referencias
https://github.com/zed-0xff/zsteg
