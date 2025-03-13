# Websites:
- https://www.dcode.fr/cipher-identifier
- https://crackstation.net/
- https://cryptii.com/pipes/caesar-cipher
- https://www.tunnelsup.com/hash-analyzer/


# command to detect and decode:
```bash
john --format=raw-md5 --wordlist=wordlist hash.txt
```
First, we have to detect which hash function format it is. For that we can detect it by this website "https://www.dcode.fr/cipher-identifier". 
Then after detect which hash function used then we have to know john the ripper sign for the command. 
### Example:
--format=raw-md5

### we can use this command to detect john the ripper hash functions:
```bash
hashid -j hash.txt
```
![image](https://github.com/user-attachments/assets/f209259e-175d-4604-a4a3-e57741173608)

### we have to make a custom wordlist like this:
![image](https://github.com/user-attachments/assets/afbaea3a-d8b9-4871-b799-eabbdd2dea82)

### A successfull decoding will be look like this:
![image](https://github.com/user-attachments/assets/ecfe386a-e7e6-4842-9a1c-ef23c854bdb8)






