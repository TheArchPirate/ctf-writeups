# Star Pcap
- - -
**Author:** v10l3nt

**File Location**

Pcap can be found in ctf-writeups/Space-Heroes/files/star.pcap

- - -
When we open the PCAP we see it is full of ICMP traffic. If we examine the content we will see that it is the same on every packet except for one section. For example:

**Packet One**

![](https://github.com/TheArchPirate/ctf-writeups/blob/main/Space-Heroes/images/star-pcap-packet-one.png?raw=true)

**Packet Two**

![](https://github.com/TheArchPirate/ctf-writeups/blob/main/Space-Heroes/images/star-pcap-packet-two.png?raw=true)

Carrying on collecting each charcter will give us the following string:

`c2hjdGZ7TDBnMWMtaSQtdGgzLWJlZ2lOTmluZy0wZi13aSRkb019`


Putting this into CyberChef we can decode it. I applied the "magic" recipe which identifies it as a base64 encoded string giving us the flag.

- - -
**Flag**

shctf{L0g1c-i\$-th3-begiNNing-0f-wi\$doM}