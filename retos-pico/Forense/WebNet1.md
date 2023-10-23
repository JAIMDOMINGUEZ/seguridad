# WebNet1
# Objetivos
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.

# Solucion
```bash
┌──(kali㉿kali)-[~/Documents/forense/webnet1]
└─$ ls                      
capture.pcap  imagen.pcap  picopico.key
                                                                                                      
┌──(kali㉿kali)-[~/Documents/forense/webnet1]
└─$ strings imagen.pcap  
┌──(kali㉿kali)-[~/Documents/forense/webnet1]
└─$ strings imagen.pcap -n15
picoCTF{honey.roasted.peanuts}
 )/'%'/9339GDG]]}
 )/'%'/9339GDG]]}
%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz


```
Exportando la imagen encontrada
![[Pasted image 20231023004139.png]]
# Notas adicionales


# Referencias

https://en.wikipedia.org/wiki/Transport_Layer_Security
