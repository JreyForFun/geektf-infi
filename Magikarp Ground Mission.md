Open a Terminal: Open Command Prompt or PowerShell (if you are on Windows), or Terminal (if you are on Mac/Linux).

Connect via SSH: Type the following command and press Enter. This uses the host, port, and username provided in the challenge:
ssh -p 10949 ctf-player@chatelaine.cylabacademy.net

Enter the Password: When prompted for the password, type f6904eaa and press Enter. (Note: As a security feature in terminals, your keystrokes won't show up on the screen while typing the password, but they are registering).

List the Files: Once connected, type ls and press Enter. This will list the files and folders in your current directory.

Find the Flag: Look for a file or folder that might contain the flag (it is often named something like flag.txt).

If it's a file, read its contents by typing cat <filename> (e.g., cat flag.txt).

If it's a folder, move into it by typing cd <foldername>, then type ls again to see what is inside.

Submit: Once you find the text that looks like a flag (usually formatted like picoCTF{...}), copy it and paste it into the FLAG box on the challenge page.