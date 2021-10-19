# Blood Bash | Forensics

## Description
- - -
We've obtained access to a system maintained by bl0ody_mary. There are five flag files that we need you to read and submit. Submit the contents of flag1.txt.

Username: bl0ody_mary

Password: d34df4c3

bloodbash.deadface.io:22 

## Solution 
- - -
We have been provided with credentials to SSH to the bloodbash machine. Doing this we land in the home directory of Bl0ody_mary.

To quickly find the flag the following command was run:

`find flag / | grep flag`

This provides us with the following output

```
...
find: '/var/lib/apt/lists/partial': Permission denied
find: '/run/sudo': Permission denied
find: '/root': Permission denied
/home/bl0ody_mary/Documents/flag1.txt
```

We can now see where flag1.txt is. After naivgating to this directory we can use cat to get the flag.

## Flag
- - -
flag{cd134eb8fbd794d4065dcd7cfa7efa6f3ff111fe}