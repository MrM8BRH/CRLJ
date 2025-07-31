Cryptography
------------
Cryptography, or cryptology, is the practice and study of techniques for secure communication in the presence of adversarial behavior. More generally, cryptography is about constructing and analyzing protocols that prevent third parties or the public from reading private messages. Modern cryptography exists at the intersection of the disciplines of mathematics, computer science, information security, electrical engineering, digital signal processing, physics, and others. Core concepts related to information security are also central to cryptography. Practical applications of cryptography include electronic commerce, chip-based payment cards, digital currencies, computer passwords, and military communications. Cryptography prior to the modern age was effectively synonymous with encryption, converting readable information to unintelligible nonsense text, which can only be read by reversing the process.

What is Encryption?
-------------------
Encryption is a cybersecurity measure that scrambles plain text so it can only be read by the user who has the secret code, or decryption key. It provides added security for sensitive information.

**Types of encryption**
- Symmetric encryption
  - Block algorithms: Encrypt a group of plain text symbols as one block.
  - Stream algorithms: Convert one symbol of plain text directly into ciphertext.
- Asymmetric encryption
  - Encrypting with the public key: ensures only the intended recipient can use the corresponding private key to decrypt the message, even if the information was breached during transit
  - Encrypting with the private key: allows the recipient of the information to verify the sender’s identity, since they won’t be able to decrypt data that’s been tampered with by an unauthorized user

**7 types of encryption algorithms**
1. Data Encryption Standard (DES)
2. Triple DES (3DES)
3. Advanced Encryption Standard (AES)
4. Rivest-Shamir-Adleman (RSA)
5. Twofish
6. Blowfish
7. Elliptic curve cryptography (ECC)

**Real symmetric encryption examples**
1. Data storage: When you encrypt files on your computer or a USB drive using a password, it often involves symmetric encryption. The same password is used to both encrypt and decrypt the data.
2. Secure Sockets Layer (SSL) and Transport Layer Security (TLS): These protocols use symmetric network encryption to protect data transmitted over the internet, such as during online banking transactions or when you log in to a secure website.
3. Virtual Private Networks (VPNs): Many VPN services use symmetric encryption to secure the data transmitted between your device and the VPN server, ensuring privacy and security while browsing the Internet.
4. Disk encryption: Whole-disk encryption tools like BitLocker (Windows) and FileVault (macOS) use symmetric encryption to protect the entire contents of a hard drive or solid-state drive (SSD).
5. Messaging apps: Some messaging apps like WhatsApp use symmetric encryption to safeguard the messages sent between users, so that only the recipient with the correct decryption key can read the messages.

Steganography
-------------
Steganography is the practice of representing information within another message or physical object, in such a manner that the presence of the information is not evident to human inspection. In computing/electronic contexts, a computer file, message, image, or video is concealed within another file, message, image, or video. The word steganography comes from Greek steganographia, which combines the words steganós, meaning "covered or concealed", and -graphia meaning "writing". The first recorded use of the term was in 1499 by Johannes Trithemius in his Steganographia, a treatise on cryptography and steganography, disguised as a book on magic. Generally, the hidden messages appear to be something else: images, articles, shopping lists, or some other cover text. For example, the hidden message may be in invisible ink between the visible lines of a private letter.

What is Hashing?
----------------
Hashing is the process of converting data — text, numbers, files, or anything, really — into a fixed-length string of letters and numbers. Data is converted into these fixed-length strings, or hash values, by using a special algorithm called a hash function.

For example, a hash function that creates 32-character hash values will always turn text input into a unique 32-character code. Whether you want to generate a hash value for the word “Codecademy” or for the entire works of Shakespeare, the hash value will always be 32 characters long.

What is Encoding and Decoding?
--------------------------------------------
Encoding and decoding are used in many forms of communications, including computing, data communications, programming, digital electronics and human communications. These two processes involve changing the format of content for optimal transmission or storage.

In computers, encoding is the process of putting a sequence of characters (letters, numbers, punctuation, and certain symbols) into a specialized format for efficient transmission or storage. Decoding is the opposite process -- the conversion of an encoded format back into the original sequence of characters.

These terms should not be confused with encryption and decryption, which focus on hiding and securing data. (We can encrypt data without changing the code or encode data without deliberately concealing the content.)

Resources and Tools
-------------------
- [Ciphey](https://github.com/Ciphey/Ciphey)
- [CyberChef](https://cyberchef.io/)
- [John the Ripper](https://github.com/openwall/john)
- [Medusa](https://github.com/jmk-foofus/medusa)
- [THC Hydra](https://github.com/vanhauser-thc/thc-hydra)
- [Aircrack-ng](https://github.com/aircrack-ng/aircrack-ng)
- [RainbowCrack](http://project-rainbowcrack.com/index.htm)
- [BruteSpray](https://github.com/x90skysn3k/brutespray)
- [Cain and Abel](https://github.com/xchwarze/Cain)
- [Hashcat](https://github.com/hashcat/hashcat)
- [ophcrack](https://ophcrack.sourceforge.io/)
- [L0phtCrack](https://ophcrack.sourceforge.io/)
- [CyberChef](https://gchq.github.io/CyberChef/)
- [Steganography - A list of useful tools and resources](https://0xrick.github.io/lists/stego/)
- [Google Apps Toolbox - Encode/Decode](https://toolbox.googleapps.com/apps/encode_decode/)
- [Hashkiller](https://hashkiller.io/listmanager)
- [dCode](https://www.dcode.fr/en)
- [CrackStation](https://crackstation.net/)
- [Shattered.io](https://shattered.io/)
- [Online Hash Crack](https://www.onlinehashcrack.com/)
- [RsaCtfTool](https://github.com/RsaCtfTool/RsaCtfTool)
- [CMD5](https://www.cmd5.org/)
- [Password Recovery](https://passwordrecovery.io/)
- [MD5 Decrypt](https://md5decrypt.net/en/)
- [Hashes.com](https://hashes.com/en/decrypt/hash)
- [Boxentriq](https://www.boxentriq.com/)
- [Cryptii](https://cryptii.com/)
- [XOR.pw](https://xor.pw/)
- [ASCII to Hex Converter](https://www.asciitohex.com/)
- [openstego](https://github.com/syvaidya/openstego)
- [zsteg](https://github.com/zed-0xff/zsteg)
- [Code Beautifier](https://beautifier.io/)
- [PHP Decoder](http://ddecode.com/phpdecoder/)
- [KahuSecurity Tools](https://www.kahusecurity.com/tools.html)
- [rot13](https://rot13.com/)
- [Online Barcode Reader](https://online-barcode-reader.inliteresearch.com/)
- [Steganography - Encode Text into Image](https://manytools.org/hacker-tools/steganography-encode-text-into-image)
- [AppEncryptor](https://github.com/AlanQuatermain/appencryptor)
- [Class-Dump](http://stevenygard.com/projects/class-dump/)
- [Readmem](https://github.com/gdbinit/readmem)
