# Matryoshka doll
# Objetivos
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/f6cc2560a70b1ea811c151accba5390f/dolls.jpg)

# Solucion
```bash
    ──(kali㉿kali)-[~/Documents/forense/matt]
└─$ open dolls.jpg 
 
┌──(kali㉿kali)-[~/Documents/forense/matt]
└─$ bimwalk -e dolls.jpg 
Command 'bimwalk' not found, did you mean:
  command 'binwalk' from deb binwalk
Try: sudo apt install <deb name>
           
┌──(kali㉿kali)-[~/Documents/forense/matt]
└─$ binwalk -e dolls.jpg

┌──(kali㉿kali)-[~/Documents/forense/matt]
└─$ ls
dolls.jpg  _dolls.jpg.extracted

┌──(kali㉿kali)-[~/Documents/forense/matt]
└─$ cd _dolls.jpg.extracted 

┌──(kali㉿kali)-[~/Documents/forense/matt/_dolls.jpg.extracted]
└─$ ls
4286C.zip  base_images
 
┌──(kali㉿kali)-[~/Documents/forense/matt/_dolls.jpg.extracted]
└─$ cd base_images         

┌──(kali㉿kali)-[~/…/forense/matt/_dolls.jpg.extracted/base_images]
└─$ ls
2_c.jpg

┌──(kali㉿kali)-[~/…/forense/matt/_dolls.jpg.extracted/base_images]
└─$ open 2_c.jpg   

┌──(kali㉿kali)-[~/…/forense/matt/_dolls.jpg.extracted/base_images]
└─$ binwalk -e 2_c.jpg     

┌──(kali㉿kali)-[~/…/forense/matt/_dolls.jpg.extracted/base_images]
└─$ ls
2_c.jpg  _2_c.jpg.extracted

┌──(kali㉿kali)-[~/…/forense/matt/_dolls.jpg.extracted/base_images]
└─$ cd _2_c.jpg.extracted  

┌──(kali㉿kali)-[~/…/matt/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted]
└─$ ls
2DD3B.zip  base_images

┌──(kali㉿kali)-[~/…/matt/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted]
└─$ cd base_images       
 
┌──(kali㉿kali)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ ls
3_c.jpg
 
┌──(kali㉿kali)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ open 3_c.jpg  

┌──(kali㉿kali)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ binwalk -e 3_c.jpg   

┌──(kali㉿kali)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ ls
3_c.jpg  _3_c.jpg.extracted

┌──(kali㉿kali)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ cd _3_c.jpg.extracted 

┌──(kali㉿kali)-[~/…/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted]
└─$ ls
1E2D6.zip  base_images

┌──(kali㉿kali)-[~/…/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted]
└─$ cd base_images       

┌──(kali㉿kali)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ ls            
4_c.jpg

┌──(kali㉿kali)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ open 4_c.jpg                                                                      

┌──(kali㉿kali)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ binwalk -e 4_c.jpg 


┌──(kali㉿kali)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ ls
4_c.jpg  _4_c.jpg.extracted

┌──(kali㉿kali)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ cd _4_c.jpg.extracted 

┌──(kali㉿kali)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ ld
ld: no input files

┌──(kali㉿kali)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ ls
136DA.zip  flag.txt

┌──(kali㉿kali)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ cat flag.txt 
picoCTF{ac0072c423ee13bfc0b166af72e25b61}                     
```

# Notas adicionales


# Referencias



