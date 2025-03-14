# **Hashcat Command Example**

### 📝 **General Syntax**

To crack a hash using Hashcat, use the following general syntax:

```bash
hashcat -m <hash_mode> -a <attack_mode> -o <output_file> <target_hash_file> <wordlist_file>
```
## 🔐 **Example**

### 💻 **Command: Straight Mode (MD5)**

```bash
hashcat -m 0 -a 0 -o cracked_hashes.txt hashes.txt wordlist.txt
```
### 💻 Another Example
```bash
hashcat -m 0 -a 0 -o result.txt md5hash_value /usr/share/wordlists/rockyou.txt
```
### 💻 Another Example
```bash
hashcat -m 0 -a 0 -o result.txt 48bb6e862e54f2a795ffc4e541caed4d /usr/share/wordlists/rockyou.txt
```

### Password Cracking Attack Modes 💻🔐

Below is a quick reference table for different attack modes used in password cracking:
# Attack Modes

| **Mode** | **Description**              |
|----------|------------------------------|
| 0        | Straight                     |
| 1        | Combination                  |
| 3        | Brute-force                  |
| 6        | Hybrid Wordlist + Mask       |
| 7        | Hybrid Mask + Wordlist       |
| 9        | Association                  |



# Hash Type and Hash Mode
| Hash Type                | Hash Mode (`-m`) |
|--------------------------|------------------|
| MD5                      | 0                |
| SHA-1                    | 100              |
| SHA-256                  | 1400             |
| SHA-512                  | 1700             |
| bcrypt                   | 3200             |
| PBKDF2-HMAC-SHA1         | 1000             |
| NTLM                     | 1000             |
| WPA2 PMKID               | 22000            |
| WordPress                | 400              |
| MySQL 5.x                | 300              |
| SHA-3                    | 1800             |
| MongoDB                  | 2800             |
| VNC                      | 7500             |
| Kerberos 5 TGS           | 13100            |
| Apple iOS Keychain       | 6900             |
| OpenSSL                  | 5000             |
| Drupal                   | 5500             |
| Joomla                   | 4600             |
| SHA-512 Crypt            | 1800             |
| RipeMD160                | 600              |
| Cisco PIX                | 2500             |
| Oracle 10g               | 500              |
| Base64                   | 5000             |
| LAN Manager (LM)         | 3000             |
| SSH                      | 5120             |
| Windows LANMAN           | 3000             |
| MongoDB SCRAM-SHA-1      | 17001            |
| PHPass                   | 4100             |
| PostgreSQL               | 5000             |
| SSH2                     | 10200            |

























