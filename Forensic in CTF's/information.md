# information
Forensics
Easy
by susie
·
picoCTF 2021
Files can always be changed in a secret way. Can you find the flag? cat.jpg

Hints
1
Look at the details of the file

2
Make sure to submit the flag as academy{XXXXX}

------------------------------------------------------

DOwnload cat.jpg

- exiftool cat.jpg (so we can see the metadata)

- Look for suspicious thing (in this challenge License are the suspicious thing)

- echo "license_long_string" | base64 -d OR go to cyberchef.org -> from base64 then paste it so it will show the translated flag


flag: academy{the_m3tadata_1s_modified}