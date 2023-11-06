# vault-door-1
# Objetivos
This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: [VaultDoor1.java](https://jupiter.challenges.picoctf.org/static/87e103a8db01087de9ccf5a7a022ddf8/VaultDoor1.java)
# Solucion
```bash
 public boolean checkPassword() {

               char [] password= new char[32];

               password[0]  = 'd';

               password[29] = 'a';

               password[4]  = 'r';

               password[2]  = '5';

               password[23] = 'r';

               password[3]  = 'c';

               password[17] = '4';

               password[1]  = '3';

               password[7]  = 'b';

               password[10] = '_';

               password[5]  = '4';

               password[9]  = '3';

               password[11] = 't';

               password[15] = 'c';

               password[8]  = 'l';

               password[12] = 'H';

               password[20] = 'c';

               password[14] = '_';

               password[6]  = 'm';

               password[24] = '5';

               password[18] = 'r';

               password[13] = '3';

               password[19] = '4';

               password[21] = 'T';

               password[16] = 'H';

               password[27] = '6';

               password[30] = 'f';

               password[25] = '_';

               password[22] = '3';

               password[28] = 'd';

               password[26] = 'f';

               password[31] = '4';

        System.out.println(password);

        return true;
        
C:\Users\Admin\Pictures>javac VaultDoor1.java

C:\Users\Admin\Pictures>java VaultDoor1
d35cr4mbl3_tH3_cH4r4cT3r5_f6daf4
Access granted.
```

# Notas adicionales

# Referencias
