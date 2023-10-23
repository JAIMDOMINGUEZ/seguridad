# m00nwalk
# Objetivos
Decode this [message](https://jupiter.challenges.picoctf.org/static/fc1edf07742e98a480c6aff7d2546107/message.wav) from the moon.

# Solucion
```bash
──(kali㉿kali)-[~/Documents/forense/m00nwalk]
└─$ sstv -d message.wav -o resultado.png
[sstv] Searching for calibration header... Found!    
[sstv] Detected SSTV mode Scottie 1
[sstv] Decoding image...                                   [####################################################################################################] 100%
[sstv] Drawing image data...
[sstv] ...Done!
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Documents/forense/m00nwalk]
└─$ ls
message.wav  resultado.png
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Documents/forense/m00nwalk]
└─$ open resultado.png 
                               
```
![[Pasted image 20231022132323.png]]
# Notas adicionales


# Referencias

https://github.com/colaclanth/sstv
