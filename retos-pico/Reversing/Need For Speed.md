# Need For Speed
# Objetivos

# Solucion
```bash
┌──(kali㉿kali)-[~/Documents/reversing/needforspeed]
└─$ chmod +x need-for-speed  
                                                                                         
┌──(kali㉿kali)-[~/Documents/reversing/needforspeed]
└─$ gdb need-for-speed    

or bug reporting instructions, please see:
<https://www.gnu.org/software/gdb/bugs/>.
Find the GDB manual and other documentation resources online at:
    <http://www.gnu.org/software/gdb/documentation/>.

For help, type "help".
Type "apropos word" to search for commands related to "word"...
Reading symbols from need-for-speed...
--Type <RET> for more, q to quit, c to continue without paging--
(No debugging symbols found in need-for-speed)
(gdb) handle SIGALRM ignore
Signal        Stop      Print   Pass to program Description
SIGALRM       No        No      No              Alarm clock
(gdb) r
Starting program: /home/kali/Documents/reversing/needforspeed/need-for-speed 
[Thread debugging using libthread_db enabled]
Using host libthread_db library "/lib/x86_64-linux-gnu/libthread_db.so.1".
Keep this thing over 50 mph!
============================

Creating key...
Finished
Printing flag:
PICOCTF{Good job keeping bus #190ca38b speeding along!}
[Inferior 1 (process 14829) exited normally]
(gdb) 

```

# Notas adicionales
- **SIGALRM**: Es una señal de alarma en sistemas basados en UNIX. Esta señal se utiliza comúnmente para programar alarmas o temporizadores. Cuando un programa recibe esta señal, puede realizar alguna acción específica, como interrumpir su ejecución o ejecutar una función de manejo de señales.
    
- **handle SIGALRM ignore**: Esta instrucción indica que el programa debe "ignorar" la señal SIGALRM. En otras palabras, cuando el programa recibe la señal SIGALRM, no realizará ninguna acción especial y continuará ejecutándose sin interrupciones.
# Referencias
