# c0rrupt
# Objetivos
We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.

# Solucion
```bash
┌──(kali㉿kali)-[~/Documents/forense/corrupt]
└─$ hexeditor mystery  
                                                                                                               
┌──(kali㉿kali)-[~/Documents/forense/corrupt]
└─$ pngcheck -v mystery
File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
  chunk IDAT at offset 0x00057, length 65445
    zlib: deflated, 32K window, fast compression
  chunk IDAT at offset 0x10008, length 65524
  chunk IDAT at offset 0x20008, length 65524
  chunk IDAT at offset 0x30008, length 6304
  chunk IEND at offset 0x318b4, length 0
No errors detected in mystery (9 chunks, 96.3% compression).
                                                                                                               
┌──(kali㉿kali)-[~/Documents/forense/corrupt]
└─$ open mystery 
```
![[Pasted image 20231022223740.png]]
# Notas adicionales


# Referencias
