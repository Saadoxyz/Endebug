
# 🔐 ENDEBUG - Python Encryption & Decryption Utility

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)](https://www.python.org/)
[![License](https://img.shields.io/github/license/saadoxyz/ENDEBUG?style=for-the-badge)](LICENSE)
[![Security](https://img.shields.io/badge/Security-AES%20%7C%203DES%20%7C%20RSA-critical?style=for-the-badge&logo=veracrypt)]()
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS-informational?style=for-the-badge&logo=linux)]()
[![Stars](https://img.shields.io/github/stars/saadoxyz/ENDEBUG?style=for-the-badge&logo=github)]()
[![Issues](https://img.shields.io/github/issues/saadoxyz/ENDEBUG?style=for-the-badge&logo=github)]()
[![Forks](https://img.shields.io/github/forks/saadoxyz/ENDEBUG?style=for-the-badge)]()
[![Contributors](https://img.shields.io/github/contributors/saadoxyz/ENDEBUG?style=for-the-badge)]()
[![Last Commit](https://img.shields.io/github/last-commit/saadoxyz/ENDEBUG?style=for-the-badge)]()

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&duration=3000&pause=500&center=true&width=600&lines=🔐+Encrypt+and+Decrypt+Text+or+Files+with+Confidence;AES+%2F+3DES+%2F+RSA+Support+Built+In;Includes+Hashing%2C+Base64%2C+KDF%2C+Multithreading+%26+SQLite3">
</p>

---

## 🧩 What is ENDEBUG?

ENDEBUG is a robust **Python-based data security toolkit** that allows you to:

- Encrypt and decrypt files and text using **symmetric** (AES, 3DES) and **asymmetric** (RSA) cryptography.
- Generate secure **hashes**, perform **base64 encoding/decoding**, and use **key derivation functions (KDF)** for secure key generation.
- Maintain configuration persistence with **SQLite3**.
- Execute **multi-threaded operations** for better performance on large files.

Whether you're a **student**, **developer**, or **IT security enthusiast**, ENDEBUG is an all-in-one solution to understand and implement cryptography easily in Python.

---

## ⚙️ Features

| Feature                          | Description |
|----------------------------------|-------------|
| 🔒 **AES / 3DES / RSA Encryption** | Choose between symmetric and asymmetric methods. |
| 🔐 **Secure Key Handling**        | Generate, save, and load keys. |
| 🧪 **KDF Integration**            | Generate keys securely from passwords. |
| 📁 **File & Text Encryption**     | Works on both string content and files. |
| 🧬 **Base64 Encode/Decode**       | Supports file-safe transformations. |
| 🔍 **SHA / MD5 Hashing**          | Quickly compute file or string hashes. |
| 💽 **SQLite3 Persistence**        | Saves user settings and session preferences. |
| ⚡ **Multithreaded**              | Better performance for file operations. |

> ✅ All commands are executed via a user-friendly CLI interface with strong error-handling and helpful output.

---

## 🖥️ Technologies Used

| Category         | Libraries                                  |
|------------------|--------------------------------------------|
| 🔐 Cryptography   | `pycryptodome`, `rsa`                      |
| 🔑 Encoding/KDF   | `base64`, `hashlib`, `getpass`             |
| 🧠 CLI Handling   | `argparse`, `os`, `sys`                    |
| ⚡ Threading      | `threading`                                |
| 💾 Persistence    | `sqlite3`                                  |
| 📂 Filesystem     | `pathlib`                                  |

These tools are carefully combined to give you fast, secure, and cross-platform support.

---

## 🔓 Symmetric Encryption (AES/3DES)

Symmetric encryption uses the **same key** for encryption and decryption.

- AES supports 128, 192, and 256-bit keys.
- Triple DES uses 56-bit keys (repeated thrice).
- Requires the same key for both processes.

### Example Command:

```bash
python endebug.py --encrypt --algo aes --input message.txt --key mykey.key
python endebug.py --decrypt --algo 3des --input message.enc --key mykey.key
````

You can also auto-generate keys:

```bash
python endebug.py --generate-key --algo aes
```

---

## 🔐 Asymmetric Encryption (RSA)

RSA uses a **public-private key pair**:

* Public key is used for encryption
* Private key is used for decryption

### Generate Key Pair:

```bash
python endebug.py --generate-keys --algo rsa
```

### Encrypt/Decrypt:

```bash
python endebug.py --encrypt --algo rsa --input plain.txt --key public.pem
python endebug.py --decrypt --algo rsa --input secret.enc --key private.pem
```

---

## 🔑 KDF (Key Derivation Function)

KDF helps generate **secure encryption keys from passwords** using salt and hashing rounds.

### Example in Python:

```python
from hashlib import pbkdf2_hmac
key = pbkdf2_hmac('sha256', b'my-password', b'some_salt', 100000)
```

Used internally to convert your password into a strong cryptographic key.

---

## 🧬 Base64 Encoding/Decoding

Convert binary files or text into readable ASCII strings.

### Encode a file:

```bash
python endebug.py --base64-encode --input mydoc.txt
```

### Decode base64:

```bash
python endebug.py --base64-decode --input encoded.b64
```

---

## 🔍 Hash Calculator (Checksum Generator)

Generate message digests to validate data integrity.

### Supported Hashes:

* MD5
* SHA-1
* SHA-256
* SHA-512

### Example:

```bash
python endebug.py --hash --algo sha256 --input file.txt
```

---

## 💾 SQLite3 Config Persistence

ENDEBUG automatically stores user preferences like:

* Algorithm last used
* Input/output paths
* Preferred hash algorithm
* Key lengths

These are loaded at next startup from a **SQLite database file** so you don’t lose your settings.

---

## ⚡ Multithreaded Execution

ENDEBUG can run **file encryption/decryption in threads**, making it 2x–3x faster on large files.

Benefit: Use all available CPU cores.

No special flags are required – it's automatically triggered when needed.

---

## 📁 Example Usage

```bash
# AES Encrypt
python endebug.py --encrypt --algo aes --input notes.txt --key mysecret.key

# 3DES Decrypt
python endebug.py --decrypt --algo 3des --input secure.bin --key mysecret.key

# RSA Key Generation
python endebug.py --generate-keys --algo rsa

# Hash using SHA-512
python endebug.py --hash --algo sha512 --input data.csv
```

---

## 📊 GitHub Project Insights

![Top Language](https://img.shields.io/github/languages/top/saadoxyz/ENDEBUG?style=for-the-badge)
![Repo Size](https://img.shields.io/github/repo-size/saadoxyz/ENDEBUG?style=for-the-badge)

![Last Commit](https://img.shields.io/github/last-commit/saadoxyz/ENDEBUG?style=for-the-badge)
![Open Issues](https://img.shields.io/github/issues/saadoxyz/ENDEBUG?style=for-the-badge)
![Contributors](https://img.shields.io/github/contributors/saadoxyz/ENDEBUG?style=for-the-badge)
![GitHub stats](https://github-readme-stats.vercel.app/api?username=saadoxyz&show_icons=true&theme=radical)

---

##🤝 Contributing

Want to contribute? Here's how:

``bash
# Clone repo
git clone https://github.com/saadoxyz/ENDEBUG.git
cd ENDEBUG

Pull requests for new features, bug fixes, or performance improvements are welcome! 🙌

---

## 📌 Future Plans

* ✅ Add GUI using PyQt or Tkinter
* ✅ Add zip + encrypt feature
* 🔜 GPG-style signing for messages
* 🔜 Progress bars and logging for file ops
* 🔜 Dockerized CLI installer

---

## 🙋‍♂️ Author

**Saad Khan**

* 🔗 GitHub: [@saadoxyz](https://github.com/saadoxyz)
* 📧 Email: [saadok652004@gmail.com](mailto:saadok652004@gmail.com)
* 💼 LinkedIn: *Coming Soon*

---

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&pause=1000&color=6EE7B7&center=true&vCenter=true&width=600&lines=🔐+ENDEBUG+-+Python+Encryption+Toolkit;Your+Privacy+Matters+%7C+Encrypt+Everything;Secure+%7C+Simple+%7C+Fast+%7C+Open+Source">
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=saadoxyz&show_icons=true&theme=radical" alt="Saad's GitHub stats"/>
</p>

---

> ENDEBUG is built with 💙 and a deep respect for user privacy and open-source security principles.

