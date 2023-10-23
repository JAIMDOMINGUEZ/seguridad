#  shark on wire 2

# Objetivos
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.

# Solucion
```bash              
rom scapy.all import *
packets = rdpcap('capture.pcap')
flag=''
for p in packets:
        if UDP in p and p[UDP].dport ==22:
                if p[UDP].sport > 5000:
                        flag += chr(p[UDP].sport - 5000)
print(flag)

──(kali㉿kali)-[~/Documents/forense/shark]
└─$ ls
capture.pcap  scrpt.py
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Documents/forense/shark]
└─$ nano scrpt.py
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Documents/forense/shark]
└─$ python scrpt.py
picoCTF{p1LLf3r3d_data_v1a_st3g0}

```

# Notas adicionales


# Referencias
