# Space Captain Garfield
- - -
**Description**

![](https://github.com/TheArchPirate/ctf-writeups/blob/main/Space-Heroes/images/SpaceCaptainGarfield.png?raw=true)

- - -
Looking at this image it is clear that the symbols in the speech bubbles are representations of characters in the alphabet. The last scene of the comic shows John with the flag format in his speech bubble. 

To solve this I went looking for Garfield comics that were set in space. The copyright notice being from the 1990s gave me a time frame to look for. 

I tried to reverse image search it using Google and Tineye but had no success. I started searching for Space Captain Garfield and looked out for the numbers given in the first scene. I found a post on Reddit:

https://www.reddit.com/r/AlzheimersGroup/comments/syc1hb/space/

![](https://github.com/TheArchPirate/ctf-writeups/blob/main/Space-Heroes/images/space-captain-garfield-reddit.png?raw=true)

This allowed to to decode all but one of the characters.

![](https://github.com/TheArchPirate/ctf-writeups/blob/main/Space-Heroes/images/garfield-character-no-decode.png?raw=true)

There was a list of characters between scene one and two which contained the character I needed. I went seaching for it. I now knew the first phrase of the first scene so I looked for "Captain Garfield wanders through the galaxy". This led me to this comic strip:

https://www.mezzacotta.net/garfield/?comic=3568

![](https://github.com/TheArchPirate/ctf-writeups/blob/main/Space-Heroes/images/garfield-extended-comic.png?raw=true)

Using this I can now tell the blurred words from before were the name of the author Jim Davis and I was looking for the character V. 

From this I now had a full flag.

- - - 
**Flag**

shctf{lasagnalover}
