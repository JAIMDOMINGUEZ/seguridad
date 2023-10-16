#  So Meta
# Objetivos
Find the flag in this [picture](https://jupiter.challenges.picoctf.org/static/916b07b4c87062c165ace1d3d31ef655/pico_img.png).

# Solucion
```bash
      ┌──(kali㉿kali)-[~/Documents/forense]
└─$ identify -verbose pico_img.png | grep "pico"
  Filename: pico_img.png
    Artist: picoCTF{s0_m3ta_d8944929}
    filename: pico_img.png
                                 
```

# Notas adicionales
|Comando|Descripcion|
|---|---|
|-verbose|imprime información detallada sobre la imagen|

# Referencias
https://www.ochobitshacenunbyte.com/2016/05/19/metadatos-en-gnu-linux/