# Safe Opener 2
# Objetivos
What can you do with this file?I forgot the key to my safe but this [file](https://artifacts.picoctf.net/c/286/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?
# Solucion
```bash
james-backster-picoctf@webshell:~/safe$ ls                  
SafeOpener.class  cfr-0.144.jar
james-backster-picoctf@webshell:~/safe$ java -jar cfr-0.144.jar SafeOpener.class > Class-file.java
james-backster-picoctf@webshell:~/safe$ ls
Class-file.java  SafeOpener.class  cfr-0.144.jar
james-backster-picoctf@webshell:~/safe$ cat Class-file.java 
/*
 * Decompiled with CFR 0.144.
 */
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStream;
import java.io.InputStreamReader;
import java.io.PrintStream;
import java.io.Reader;
import java.util.Base64;

public class SafeOpener {
    public static void main(String[] args) throws IOException {
        BufferedReader keyboard = new BufferedReader(new InputStreamReader(System.in));
        Base64.Encoder encoder = Base64.getEncoder();
        String encodedkey = "";
        String key = "";
        for (int i = 0; i < 3; ++i) {
            System.out.print("Enter password for the safe: ");
            key = keyboard.readLine();
            encodedkey = encoder.encodeToString(key.getBytes());
            System.out.println(encodedkey);
            boolean isOpen = SafeOpener.openSafe(encodedkey);
            if (isOpen) break;
            System.out.println("You have  " + (2 - i) + " attempt(s) left");
        }
    }

    public static boolean openSafe(String password) {
        String encodedkey = "picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_3dae8463}";
        if (password.equals(encodedkey)) {
            System.out.println("Sesame open");
            return true;
        }
        System.out.println("Password is incorrect\n");
        return false;
    }
```

# Notas adicionales

# Referencias
