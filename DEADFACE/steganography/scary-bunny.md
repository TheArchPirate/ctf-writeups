# Scary Bunny | Steganography

## Description
- - -
What could be inside this creepy rabbit?

## File
- - -
You can find the image in this repository:

ctf-writeups/DEADFACE/files/steganography/bunny.jpg

<img src="../files/steganography/bunny.jpg">

## Solution
- - -

We can try to extract this flag using steghide. We run the following command:

`steghide extract -sf bunny.jpg`

We are prompted for a password at this stage. Leaving this blank extracts a file:

```
Enter passphrase: 
wrote extracted data to "steganopayload730241.txt".
```

We can then cat the flag out.

## Flag
- - -
flag{Carr0t}