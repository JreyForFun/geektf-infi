StegoRSA
Cryptography
Easy
by Yahaya Meddy
·
picoCTF 2026
A message has been encrypted using RSA. The public key is gone… but someone might have been careless with the private key. Can you recover it and decrypt the message? Download the flag
 and image
.

Hints
1
Metadata can tell you more than you expect.

2
Hex can be turned back into a key file.

 
STEPS STEPS STEPS

Download image and the text

-> exiftool image.png
-> check the ambigous: in this you can see that comment are something wrong


-> exiftool -b -Comment image.jpg > comment.hex
This extracts only the comment’s contents into comment.hex, without the Comment: label.

xxd -r -p comment.hex > recovered.key

Here’s what each part means:
- xxd: a tool for working with hex.
- -r: reverses hex back into bytes.
- -p: treats the input as plain hex.
- > recovered.key: saves the result into a file named recovered.key.

openssl pkeyutl -decrypt -inkey recovered.key -in flag.enc -out decrypted.txt

- openssl pkeyutl: performs cryptographic operations using keys.
- -decrypt: decrypts the message.
- -inkey recovered.key: selects your private key.
- -in flag.enc: selects the encrypted file.
- -out decrypted.txt: saves the decrypted result.

If succeed then
nano decrypted.txt and copy the text
cat dercrypted.txt and copy the text
academy{12414nkn}