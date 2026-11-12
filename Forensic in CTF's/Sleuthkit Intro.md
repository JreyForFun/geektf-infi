Sleuthkit Intro
Forensics
Medium
by LT 'syreal' Jones
·
picoCTF 2022
Download the disk image and use mmls on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.

Note: if you are using the webshell, download and extract the disk image into /tmp not your home directory.

=========================================

S1 - DOWNLOAD THE IMAGE DISK FILE THEN gunzip disk.image.dz

S - ls

S2 - mmls disk.image

S3 - Analyze the Output: The command will output a table. Scan the "Description" column to find the partition labeled "Linux". Once you find it, look at the corresponding number in the "Length" column. That specific number is the answer you are looking for.

Claim the Flag: Click the orange Launch Instance button on your screen. This will reveal a connection string (usually an nc or ssh command). Run that command in your terminal, submit the length number you found, and the remote service will hand you the flag.

S4 - Once you have a clear command line again:

Run mmls on the disk image you extracted.

Find the number in the Length column for the Linux partition.

Run that nc command again to reconnect.

Type in the number you found!

s5 - I see you got the command to work perfectly!

Look at the output table in your terminal screenshot. If you trace the row with the Description Linux (0x83) over to the Length column, you will see your answer.

The size of the Linux partition you need is 202752 (you can ignore the leading zeros).

Now, just run the checker program command provided on the challenge page (nc xebec.cylabacademy.net 20657), enter that number, and claim your flag!