# Khaaaaaan!
- - -
We have intercepted a messages from different ships, but I can't seem to dcode what they are saying. Can you? 

![](https://github.com/TheArchPirate/ctf-writeups/blob/main/Space-Heroes/images/languages.PNG?raw=true)


Flag format: shctf{add_after_each_word}

**Author:** Lil Tipo
- - -

As can be seen in the image above, there appears to be four different message segments. I found each of these individually in Google images using search terms such as "alien language." I eventually stumbled across dcode at the end which could translate all these scripts:

https://www.dcode.fr/symbols-ciphers

**Section 1**

This is known as Alien Lanague. It decodes to:

`shctfwithoutfreedom`

**Section 2**

This is Covenant from the Halo series. It decodes to:

`ofchoice`

**Section 3:**

This is Klingon from Star Trek. It decodes to:

`thereis`

**Section 4:**

This is Alienese from Futurama. It decodes to:

`nocreativity`

Joining these together and adding the necessary underscores we get the flag. This challenge may have been easier for those who are fans of Sci Fi.

- - -
**Flag**

shctf{without_freedom_of_choice_there_is_no_creativity}