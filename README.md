Sure! Here's a professionally structured and detailed `README.md` for your Python encryption-decryption tool **ENDEBUG**, tailored for GitHub. It includes features, usage, technologies, SVG stats badges, and other enhancements.

---

````markdown
# 🔐 ENDEBUG - Python Encryption & Decryption Utility

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat-square&logo=python)](https://www.python.org/)
[![License](https://img.shields.io/github/license/your-repo/ENDebug?style=flat-square)](LICENSE)
[![Security](https://img.shields.io/badge/encryption-AES%20%7C%203DES%20%7C%20RSA-critical?style=flat-square&logo=veracrypt&color=green)]()
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS-informational?style=flat-square&logo=linux)]()
[![Stars](https://img.shields.io/github/stars/your-repo/ENDEBUG?style=flat-square&logo=github)]()

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com/?lines=Encrypt+%26+Decrypt+Text+or+Files;AES+%7C+3DES+%7C+RSA+Support;Base64+%7C+Hash+%7C+KDF+Tools&center=true&width=500&height=45">
</p>

---

## 🧩 What is ENDEBUG?

**ENDEBUG** is a Python-powered encryption-decryption utility designed for both beginners and professionals to easily protect their data using **symmetric** (AES, 3DES) and **asymmetric** (RSA) encryption methods. It also features **base64 encoding**, **KDF**, and **hash calculators**, making it an all-in-one privacy toolkit.

> This tool is useful for educational purposes, secure messaging, safe file storage, or any application where secure information handling is required.

---

## ⚙️ Features

- 🔐 **Symmetric Encryption** (AES, 3DES) for files and plain text
- 🔐 **Asymmetric Encryption** (RSA) with public-private key pair
- 🔑 Key management (generate, save, load, or enter keys manually)
- 🧪 **KDF (Key Derivation Function)** to generate secure keys from passwords
- 🧬 Base64 encoding/decoding for plain text or file content
- 🧮 Hash calculator (MD5, SHA-1, SHA-256, SHA-512)
- 🧠 Multi-threaded encryption/decryption for improved performance
- 💾 SQLite3 database support to save/load configurations
- 📁 File and plain-text operations supported

---

## 🖥️ Technologies Used

| Category         | Libraries                          |
|------------------|------------------------------------|
| 🔐 Encryption     | `pycryptodome`, `rsa`              |
| 🔑 Encoding & KDF | `base64`, `hashlib`, `getpass`     |
| 🧠 UI/Config      | `argparse`, `sqlite3`, `os`, `sys` |
| 📁 File Handling  | `threading`, `pathlib`             |

---

## 🔓 Symmetric Encryption

ENDEBUG supports **AES (128, 192, 256-bit)** and **Triple DES (3DES)** encryption. You can:

- Use a key of 16, 24, or 32 bytes
- Encrypt/decrypt plaintext or files
- Automatically generate secure random keys
- Store/load keys from files

```bash
python endebug.py --encrypt --algo aes --input message.txt --key mysecret.key
````

---

## 🔐 Asymmetric Encryption (RSA)

Asymmetric encryption uses **public/private key pair**. You can:

* Generate a new RSA key pair (1024+ bits)
* Encrypt using public key
* Decrypt using private key

```bash
python endebug.py --generate-keys --algo rsa
python endebug.py --encrypt --algo rsa --input message.txt --key public.pem
python endebug.py --decrypt --algo rsa --input message.enc --key private.pem
```

---

## 🔑 KDF - Key Derivation

A **Key Derivation Function (KDF)** lets you securely derive encryption keys from user passwords.

```python
from hashlib import pbkdf2_hmac

key = pbkdf2_hmac('sha256', b'my-password', b'salt', 100000)
```

---

## 🧬 Base64 Encode / Decode

```bash
python endebug.py --base64-encode --input myfile.txt
python endebug.py --base64-decode --input encoded.b64
```

---

## 🔍 Hash Generator

Supported algorithms:

* MD5
* SHA-1
* SHA-256
* SHA-512

```bash
python endebug.py --hash --algo sha256 --input myfile.txt
```

---

## 📦 SQLite3 Config Persistence

Your app automatically stores:

* Last used encryption algorithm
* Key size
* Paths and preferences

It uses `sqlite3` to save and reload preferences upon restarting.

---

## 📁 Example Commands

```bash
# Encrypt text using AES
python endebug.py --encrypt --algo aes --input "hello world" --key mykey.key

# Decrypt file
python endebug.py --decrypt --algo 3des --input myfile.enc --key mykey.key

# Hash a file
python endebug.py --hash --algo sha512 --input notes.txt
```

---

## 📊 Project Stats

![Languages](https://img.shields.io/github/languages/top/saadoxyz/ENDEBUG?style=for-the-badge)
![Repo Size](https://img.shields.io/github/repo-size/saadoxyz/ENDEBUG?style=for-the-badge)
![Last Commit](https://img.shields.io/github/last-commit/saadoxyz/ENDEBUG?style=for-the-badge)

---

## 🤝 Contributing

Contributions are welcome! Open issues or submit PRs.

```bash
# Clone repo
git clone https://github.com/Saadoxyz/ENDEBUG.git
cd ENDEBUG
pip install -r tempCodeRunnerFile.pyw
```

---

## 🙋‍♂️ Author

**Saad Khan**
🔗 [GitHub](https://github.com/saadoxyz) | 📧 [saadok652004@gmail.com](mailto:saadok652004@gmail.com)

---

<p align="center">
<imgsrc="https://readmetypingsvg.herokuapp.comfont=Fira+Code&duration=2500&pause=1000&color=34D399&width=435&lines=Secure+Your+Data+with+Python;ENCRYPT+%7C+DECRYPT+%7C+HASH+%7C+KDF">
</p>
```

