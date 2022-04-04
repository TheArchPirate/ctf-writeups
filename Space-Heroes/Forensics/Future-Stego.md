# Future Stego
- - -
![](https://github.com/TheArchPirate/ctf-writeups/blob/main/Space-Heroes/images/sallyride.jpg?raw=true)

**Author:** Lil Tipo

**Downloadable Image**

![[shuttlesteg.jpg]]
- - -
I started out by trying to use binwalk to see if I could see or extract anything. I then tried to bruteforce with StegSeek using the rockyou wordlist. This was successful.

![](https://github.com/TheArchPirate/ctf-writeups/blob/main/Space-Heroes/images/stegseek-shuttlesteg.png?raw=true)

I could now cat out the flag:
![](https://github.com/TheArchPirate/ctf-writeups/blob/main/Space-Heroes/images/shuttlesteg-file.png?raw=true)

- - -
**Flag**

shctf{weightlessness_is_a_great_equalizer}