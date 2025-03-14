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






























# Password Hash Cracking Guide Using John the Ripper

This guide provides a detailed process for identifying and cracking password hashes using **John the Ripper**. It covers the steps from hash detection, format identification, wordlist creation, to the cracking process. The tools referenced in this guide include:

- [dCode Cipher Identifier](https://www.dcode.fr/cipher-identifier) (for hash type detection)
- [CrackStation](https://crackstation.net/) (for wordlist generation)
- [Cryptii](https://cryptii.com/pipes/caesar-cipher) (for generating cipher variations)
- [TunnelsUp Hash Analyzer](https://www.tunnelsup.com/hash-analyzer/) (for analyzing hash algorithms)

## Prerequisites

Ensure you have the following tools installed and ready to use:

- **John the Ripper**: A powerful password cracking tool.
  - [John the Ripper Installation Guide](https://www.openwall.com/john/)
- **hashid**: A tool for identifying the hash algorithm used.
  - Install with: `pip install hashid`
- **Wordlist**: A file containing potential password guesses.

## Steps to Detect and Crack Password Hashes

### Step 1: Detect the Hash Algorithm

Before cracking a password hash, you need to determine which hash algorithm was used. You can do this by using the **dCode Cipher Identifier** tool or the **hashid** tool. This step is essential to apply the correct format in John the Ripper.

- **Using dCode Cipher Identifier:**
  1. Visit [dCode Cipher Identifier](https://www.dcode.fr/cipher-identifier).
  2. Paste your hash in the input box.
  3. The website will attempt to identify the hash format and display the corresponding algorithm.
  
  ![dCode Cipher Identifier](https://github.com/user-attachments/assets/f209259e-175d-4604-a4a3-e57741173608)

- **Using hashid (Command Line Tool):**
  1. Run the following command to detect the hash type:
     ```bash
     hashid -j hash.txt
     ```
  2. The output will display the hash format, for example: `MD5`, `SHA-1`, `SHA-256`, etc.

  ![Hashid Output](https://github.com/user-attachments/assets/afbaea3a-d8b9-4871-b799-eabbdd2dea82)

### Step 2: Identify the Correct John the Ripper Format

Once you've identified the hash type, it's time to map it to the correct format for **John the Ripper**. Below are some common hash formats and their corresponding John the Ripper identifiers:

- **MD5**: `--format=raw-md5`
- **SHA-1**: `--format=raw-sha1`
- **SHA-256**: `--format=raw-sha256`
- **bcrypt**: `--format=bcrypt`
- **LM Hash**: `--format=lm`

Refer to the [John the Ripper documentation](https://www.openwall.com/john/doc/) for more details on supported formats.

### Step 3: Create or Obtain a Wordlist

John the Ripper requires a wordlist of potential password guesses to crack the hash. You can either create a custom wordlist or download a pre-existing one from online resources. Below are a few sources:

- **CrackStation**: [CrackStation Wordlist Generator](https://crackstation.net/)
- **Cryptii**: [Cryptii Cipher Generator](https://cryptii.com/pipes/caesar-cipher)

A basic wordlist might look like this:





