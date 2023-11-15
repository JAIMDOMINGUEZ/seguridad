#  Bit-O-Asm-1
# Objetivos
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Download the assembly dump [here](https://artifacts.picoctf.net/c/509/disassembler-dump0_a.txt).
# Solucion
```bash
`picoCTF{48}`
```

# Notas adicionales
- La instrucción en la dirección de memoria <+15> (`mov eax,0x30`) mueve el valor hexadecimal `0x30` al registro `eax`.
- El valor hexadecimal `0x30` es equivalente al valor decimal `48`.
# Referencias
