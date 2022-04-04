# Interstellar Mystery
- - -
We've stumbled across a ship in the depths of space. There were no life readings. For reasons as yet unknown to us, the hull was filled with Nutter Butters and insecticide.

Can you help us solve this interstellar mystery?

author: condor0010

**File Location**
The zip file can be found in ctf-writeups/Space-Heroes/files/chall.zip
- - -

First we want to know what is in the zip file. Inflating it results in an img directory with two qcow2 images. I found a guide by James Coyle which allowed me to mount these files for examination. The article can be found here:
https://www.jamescoyle.net/how-to/1818-access-a-qcow2-virtual-disk-image-from-the-host


I loaded the nbd kernel module:
`modprobe nbd`

I then attached the two images:
`sudo qemu-nbd -c /dev/nbd2 master0-3.qcow2`
`sudo qemu-nbd -c /dev/nbd1 master0-4.qcow2`

Both images needed to be mounted for to access any of the data. After this I entered Thunar and mounted the drive. I could see a binary file called "e" in there.

![[binary-e.png]]

I was wondering if I could head or tail this to get anything useful, but that wasn't the case. I then tried to grep the file but kept getting an error about a Binary file. I found a stackoverflow thread that helped with this:

https://stackoverflow.com/questions/23512852/grep-binary-file-matches-how-to-get-normal-grep-output

With this I could get the flag with grep:
`grep -ia shctf e`

grep flags:
- i - ignore-case
- a - text (process binary as if it was text)

![[grep-e.png]]

- - -
**Flag**
shctf{btrfs_is_awsome}