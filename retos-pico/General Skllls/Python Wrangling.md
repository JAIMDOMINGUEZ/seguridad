#  Python Wrangling
# Objetivos
Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/ende.py) using [this password](https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/pw.txt) to get [the flag](https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/flag.txt.en)?

# Solucion
```bash
james-backster-picoctf@webshell:~$ python ende.py 
Usage: ende.py (-e/-d) [file]
james-backster-picoctf@webshell:~$ python ende.py -d flag.txt.en
Please enter the password:67c6cc9667c6cc9667c6cc9667c6cc96
picoCTF{4p0110_1n_7h3_h0us3_67c6cc96}
james-backster-picoctf@webshell:~$ 
```

# Notas adicionales

# Referencias
