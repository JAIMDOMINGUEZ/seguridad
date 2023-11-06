# ### HideToSee
# Objetivos
How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/241/atbash.jpg).
# Solucion
```bash
──(kali㉿kali)-[~/Documents/crypto/hidetosee]
└─$ steghide extract -sf atbash.jpg
Enter passphrase: 
wrote extracted data to "encrypted.txt".
                                                      
┌──(kali㉿kali)-[~/Documents/crypto/hidetosee]
└─$ ls
atbash.jpg  encrypted.txt
                                                      
┌──(kali㉿kali)-[~/Documents/crypto/hidetosee]
└─$ cat encrypted.txt 
krxlXGU{zgyzhs_xizxp_7142uwv9}

```
![[Pasted image 20231105213803.png]]
# Notas adicionales

# Referencias
https://www.dcode.fr/atbash-cipher