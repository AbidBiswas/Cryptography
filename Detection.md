Websites:
- https://www.dcode.fr/cipher-identifier
- https://crackstation.net/


john --format=raw-md5 --wordlist=wordlist hash.txt

first, we have to detect which hash function format it is. For that we can detect it by this website "https://www.dcode.fr/cipher-identifier". Then after detect which hash function used then we have to know john the ripper sign for the command. Example:
--format=raw-md5

we can use this command to detect john the ripper hash functions:
hashid -j hash.txt
![image](https://github.com/user-attachments/assets/f209259e-175d-4604-a4a3-e57741173608)


