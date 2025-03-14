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





















# 🔒 Password Hash Cracking Workflow

This document outlines a systematic approach to cracking password hashes, a crucial skill in penetration testing.

## 🔍 Hash Identification

* **Purpose:** Determine the hash algorithm used.
* **Tools:**
    * 🌐 [dcode.fr/cipher-identifier](https://www.dcode.fr/cipher-identifier) - Web-based identifier.
    * 💻 `hashid -j hash.txt` - Command-line identification (for scripting).
        * Example output:
            ```bash
            hashid -j hash.txt
            ```
            ![image](https://github.com/user-attachments/assets/f209259e-175d-4604-a4a3-e57741173608)
    * 📊 [tunnelsup.com/hash-analyzer/](https://www.tunnelsup.com/hash-analyzer/) - Another web-based option.
* **Importance:** Crucial for selecting the correct cracking tool and format.

## 🔨 Cracking with John the Ripper (John)

* **Tool:** `john` - A powerful password cracking tool.
* **Format Specification:**
    * Use `--format=<hash_type>` to specify the hash algorithm.
    * Example: `--format=raw-md5`
    * Detect John the ripper formats with:
        ```bash
        john --list-formats
        ```
* **Wordlist Attacks:**
    * Use `--wordlist=<wordlist_file>` to specify a dictionary.
    * Creating custom wordlists is highly effective.
        * Example custom wordlist structure:
            ![image](https://github.com/user-attachments/assets/afbaea3a-d8b9-4871-b799-eabbdd2dea82)
    * Successful cracking example:
        ![image](https://github.com/user-attachments/assets/ecfe386a-e7e6-4842-9a1c-ef23c854bdb8)
* **Example command:**
    ```bash
    john --format=raw-md5 --wordlist=wordlist hash.txt
    ```

## 📚 Additional Resources

* 🔑 [crackstation.net/](https://crackstation.net/) - Pre-computed hash lookup.
* 🔄 [cryptii.com/pipes/caesar-cipher](https://cryptii.com/pipes/caesar-cipher) - For simple ciphers (less relevant for complex hashes).

## 💡 Advanced Considerations

* 🧂 **Salted Hashes:** Modern systems use salts. `john` can handle them, but you need the salt.
* 🚀 **Hashcat:** A faster, GPU-accelerated alternative to `john`.
* 📜 **Rule-Based Attacks:** Use rules to modify wordlist entries (e.g., append numbers or symbols).
* ⏱️ **Time Management:** Cracking can take time. Prioritize targets and use efficient techniques.
* 🛡️ **Legal and Ethical:** Always obtain proper authorization before attempting to crack passwords.

## 📝 Best Practices for Wordlists

* Combine common passwords, variations, and target-specific terms.
* Utilize tools like `crunch` or `cupp` to generate custom wordlists.
* Regularly update and expand your wordlists.






