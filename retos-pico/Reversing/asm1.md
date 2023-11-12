# asm1
# Objetivos
What does asm1(0x8be) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/66c927e32f3d7be7a62d13a7c2250943/test.S)
# Solucion
```bash
asm1:
        <+0>:   push   ebp
        <+1>:   mov    ebp,esp
        <+3>:   cmp    DWORD PTR [ebp+0x8],0x71c
        <+10>:  jg     0x512 <asm1+37>
        <+12>:  cmp    DWORD PTR [ebp+0x8],0x6cf
        <+19>:  jne    0x50a <asm1+29>
        <+21>:  mov    eax,DWORD PTR [ebp+0x8]
        <+24>:  add    eax,0x3
        <+27>:  jmp    0x529 <asm1+60>
        <+29>:  mov    eax,DWORD PTR [ebp+0x8]
        <+32>:  sub    eax,0x3
        <+35>:  jmp    0x529 <asm1+60>
        <+37>:  cmp    DWORD PTR [ebp+0x8],0x8be
        <+44>:  jne    0x523 <asm1+54>
        <+46>:  mov    eax,DWORD PTR [ebp+0x8]
        <+49>:  sub    eax,0x3
        <+52>:  jmp    0x529 <asm1+60>
        <+54>:  mov    eax,DWORD PTR [ebp+0x8]
        <+57>:  add    eax,0x3
        <+60>:  pop    ebp
        <+61>:  ret  
```
1. Compara el valor en `[ebp+0x8]` con `0x71c`.
2. Si el valor es mayor, salta a `0x512`.
3. De lo contrario, compara el valor con `0x6cf`.
4. Si los valores no son iguales, salta a `0x50a`.
5. Si los valores son iguales, suma `0x3` al valor y salta a `0x529`.
6. Si la primera comparación en `0x3` es falsa y la segunda comparación en `0x19` es verdadera, resta `0x3` al valor y salta a `0x529`.
7. Si las dos primeras comparaciones son falsas, compara el valor con `0x8be`.
8. Si los valores son iguales, resta `0x3` al valor y salta a `0x529`.
9. Si los valores no son iguales, suma `0x3` al valor y salta a `0x529`.

Por lo tanto, el valor devuelto por `asm1(0x8be)` depende de la comparación en la dirección `0x37`. Si el valor en `[ebp+0x8]` es igual a `0x8be`, resta `0x3`; de lo contrario, suma `0x3`.

Así que, para `asm1(0x8be)`, resta `0x3` de `0x8be`, lo que da como resultado `0x8bb`.

La respuesta es `0x8bb`.
# Notas adicionales

# Referencias
https://sge.frba.utn.edu.ar/wiki/td3/doku.php?id=guiasupervivenciaasm