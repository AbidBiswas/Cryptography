# 🔐 **Hashcat Command Example**

## 📝 **General Syntax**

To crack a hash using Hashcat, use the following general syntax:

```bash
hashcat -m <hash_mode> -a <attack_mode> -o <output_file> <target_hash_file> <wordlist_file>

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




