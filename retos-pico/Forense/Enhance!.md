# Enhance!
# Objetivos
Download this image file and find the flag.

- [Download image file](https://artifacts.picoctf.net/c/100/drawing.flag.svg)

# Solucion
```bash
┌──(kali㉿kali)-[~/Documents/forense/enchance]
└─$  strings drawing.flag.svg | grep "pico"  

                                                                                                               
┌──(kali㉿kali)-[~/Documents/forense/enchance]
└─$  strings drawing.flag.svg | grep "{"   

         id="tspan3764">F { 3 n h 4 n </tspan><tspan
                                                                                                               
┌──(kali㉿kali)-[~/Documents/forense/enchance]
└─$  strings drawing.flag.svg | grep "}"

         id="tspan3752">c 3 d _ a a b 7 2 9 d d }</tspan></text>
             
```

# Notas adicionales

|Comando|Descripcion|
|---|---|
|strings|se utiliza para imprimir cadenas de texto legibles en un archivo binario.|
|
# Referencias



