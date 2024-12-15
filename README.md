 As its name would imply, this program can encrypt your data, and decrypt it; along with some additional features like KDF, hash and base64 encoding.

Encryption is turning your data into something unreadable, which can only be turned back to its original form using a digital key. This program lets you do this.

To decrypt the data that you had encrypted using a symmetric key encryption algorithm (AES or 3DES) with this program, you need to have the key called "the encryption key", which you had used to encrypt your data, or was generated and shown to you. This key consists of either 16, 24 or 32 random characters. Since the same key can be used to both encrypt and decrypt, these kinds of algorithms are called symmetric. Similarly, to decrypt a piece of asymmetrically encrypted data (using RSA algorithm), you need to have a key called "private key" which is usually longer than 1024 characters. In order to have two or more pieces of data be decryptable using the same private key, you need to encrypt them with the same public key, which can be extracted from the private key. Because there are two different keys involved in this process, these algorithms are called asymmetric.
some features of it include
Multi-threaded plain-text or file encryption/decryption using AES and 3DES algorithms.
Ability to generate, enter or browse an encryption key; and ability to save an encryption key to a file.
Plain-text or file encoding/decoding using base64 encoding.
Plain-text or file hash calculation using SHA-1, SHA-256, SHA-512 and MD-5.
Ability to derivate an encryption key from a password (KDF).
Usage of SQLite3 for saving the configurations made (such as what to encrypt or the length of the key to generate) to a database file when the user closes the program, and load the saved configurations in the next start-up.
