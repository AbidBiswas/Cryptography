# Websites 🌐

- [dcode Cipher Identifier](https://www.dcode.fr/cipher-identifier) 
- [CrackStation](https://crackstation.net/) 
- [cryptii Caesar Cipher](https://cryptii.com/pipes/caesar-cipher) 
- [TunnelsUp Hash Analyzer](https://www.tunnelsup.com/hash-analyzer/) 


# command to detect and decode 💻
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
### by using *hashid* we can also determine the value we need to use for hashcat 
![image](https://github.com/user-attachments/assets/088be575-1d6d-4977-a1ae-21702ed8944e)

### by using *hashid* we can also determine the value we need to use for John the Ripper 
![image](https://github.com/user-attachments/assets/2ec9d2fa-8daa-413e-9a19-cf842068631f)

## we can do this task more smoothly and faster with haiti
![image](https://github.com/user-attachments/assets/bbe3a57c-7cae-4dcc-af41-27e6923f2fb7)

# we can identify the hash by using the hash-identifier tool in kali. We have to use the command below and then we have to press enter. Aftert that, we have to paste our hash and it will detect the possible outcome.
```bash
hash-identifier
```



### we have to make a custom wordlist like this:
![image](https://github.com/user-attachments/assets/afbaea3a-d8b9-4871-b799-eabbdd2dea82)

### A successfull decoding will be look like this:
![image](https://github.com/user-attachments/assets/ecfe386a-e7e6-4842-9a1c-ef23c854bdb8)






