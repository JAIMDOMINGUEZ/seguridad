# WebNet0
# Objetivos
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.

# Solucion
```bash
┌──(kali㉿kali)-[~/Documents/forense/webnet0]
└─$ ls                                                                                              
capture.pcap  picopico.key
                                                                                                      
┌──(kali㉿kali)-[~/Documents/forense/webnet0]
└─$ wireshark capture.pcap                                                                          
 ** (wireshark:62507) 02:24:50.445301 [GUI WARNING] -- FIX Add drag reordering to UAT dialog
 ** (wireshark:62507) 02:26:14.882688 [GUI WARNING] -- FIX Add drag reordering to UAT dialog
 ** (wireshark:62507) 02:26:31.260529 [GUI WARNING] -- QXcbConnection: XCB error: 3 (BadWindow), sequence: 17234, resource id: 19314574, major code: 40 (TranslateCoords), minor code: 0
 ** (wireshark:62507) 02:26:33.825032 [GUI WARNING] -- QXcbConnection: XCB error: 3 (BadWindow), sequence: 17272, resource id: 19310342, major code: 40 (TranslateCoords), minor code: 0
                                                                                                      
┌──(kali㉿kali)-[~/Documents/forense/webnet0]
└─$ wireshark capture.pcap

```
![[Pasted image 20231023003249.png]]
# Notas adicionales


# Referencias

https://en.wikipedia.org/wiki/Transport_Layer_Security
