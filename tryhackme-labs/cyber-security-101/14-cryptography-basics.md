# Cryptography Basics

In this TryHackMe room, I learned the fundamentals of **cryptography** and how it enables secure communication and data protection in the presence of adversaries.

The room introduced important cryptographic terminology, historical ciphers such as the Caesar Cipher, symmetric and asymmetric encryption, commonly used encryption algorithms, and mathematical operations such as XOR and modulo that form part of the foundation of modern cryptography.

---

## 🧠 What I Learned

### 🔐 What is Cryptography?

Cryptography is the practice and study of techniques used to protect information and enable secure communication, even when adversaries or third parties may be present.

Its purpose is to prevent unauthorized parties from reading or modifying protected information.

Cryptography helps protect:

- **Confidentiality** — preventing unauthorized access to information
- **Integrity** — ensuring information has not been altered
- **Authenticity** — helping verify that we are communicating with the intended party

Although users rarely interact directly with cryptographic algorithms, cryptography is used throughout modern digital systems.

---

## 🌐 Cryptography in Everyday Life

Cryptography is used in many activities I perform online.

Examples covered in this room include:

### Login Credentials

When logging into a website such as TryHackMe, credentials can be encrypted while being transmitted so that someone monitoring the connection cannot easily retrieve them.

### SSH Connections

When connecting to another system using SSH, the client and server establish an encrypted tunnel to protect the session from eavesdropping.

### Online Banking

When accessing online banking, the browser can check the remote server's certificate to help confirm that it is communicating with the legitimate server.

### File Integrity

Cryptographic hash functions can help verify whether a downloaded file is identical to the original.

---

## 🛡️ Protecting Sensitive Information

Cryptography is also important when organizations handle sensitive information.

For example, organizations processing payment card information may need to follow **PCI DSS (Payment Card Industry Data Security Standard)** requirements.

Sensitive payment information may need to be protected:

- **At rest** — while stored
- **In motion** — while being transmitted

Medical information can also be subject to laws and regulations depending on the country, including examples such as:

- HIPAA
- HITECH
- GDPR
- DPA

This demonstrated how cryptography is not simply a technical concept but an important component of protecting sensitive information.

---

## 🔄 From Plaintext to Ciphertext

One of the most important concepts I learned was the basic encryption and decryption process.

The process can be represented as:

```text
Plaintext + Key
       ↓
   Encryption
       ↓
   Ciphertext
```

To recover the original information:

```text
Ciphertext + Key
       ↓
   Decryption
       ↓
    Plaintext
```

---

## 📖 Important Cryptography Terms

### Plaintext

**Plaintext** is the original readable information before encryption.

It can include:

- Text
- Documents
- Images
- Multimedia
- Credit card information
- Medical records
- Other binary data

---

### Ciphertext

**Ciphertext** is the scrambled and unreadable version of the plaintext produced after encryption.

Ideally, someone looking at the ciphertext should not be able to determine information about the original plaintext except approximately its size.

---

### Cipher

A **cipher** is an algorithm or method used to convert plaintext into ciphertext and back again.

The cipher itself does not need to remain secret.

---

### Key

A **key** is a string of bits used by the cipher during encryption or decryption.

The cipher can be publicly known while the appropriate key remains protected, except for public keys used in asymmetric cryptography.

---

### Encryption

**Encryption** converts:

```text
Plaintext → Ciphertext
```

using a cipher and a key.

---

### Decryption

**Decryption** reverses the encryption process:

```text
Ciphertext → Plaintext
```

Without the correct key, recovering the original plaintext should be computationally infeasible for a secure cryptographic system.

---

## 🏛️ Historical Ciphers

Cryptography has existed for thousands of years.

One of the simplest historical encryption techniques covered in this room was the **Caesar Cipher**.

---

## 🔤 Caesar Cipher

The Caesar Cipher encrypts a message by shifting each letter of the alphabet by a specified number.

For example:

```text
Plaintext: TRYHACKME
Key:       3
Cipher:    Caesar Cipher
```

Using a right shift of three:

```text
T → W
R → U
Y → B
```

The resulting ciphertext becomes:

```text
WUBKDFNPH
```

To decrypt the message, the letters are shifted in the opposite direction using the same key.

---

## ⚠️ Weakness of the Caesar Cipher

The Caesar Cipher is considered insecure by modern standards.

Because the English alphabet contains only 26 letters, there are only **25 useful shift keys** that need to be tested.

An attacker who knows that Caesar Cipher was used can simply try the possible keys until meaningful plaintext appears.

This demonstrated why modern cryptography requires algorithms and keys that cannot realistically be defeated through simple brute-force attempts.

---

## 📜 Other Historical Ciphers

Other historical cryptographic systems mentioned in the room include:

- Vigenère Cipher
- Enigma machine
- One-time pad

These represent different stages in the historical development of cryptography.

---

# 🔑 Types of Encryption

The two main categories of encryption covered were:

1. **Symmetric Encryption**
2. **Asymmetric Encryption**

---

## 🔒 Symmetric Encryption

Symmetric encryption uses the **same key for encryption and decryption**.

```text
              Secret Key
                  ↓
Plaintext → Encryption → Ciphertext
                              ↓
                         Decryption
                              ↓
                          Plaintext
                              ↑
                          Secret Key
```

Because the same key is required by both parties, that key must remain secret.

Symmetric encryption is therefore also referred to as **private key cryptography**.

---

## 🔑 The Symmetric Key Distribution Problem

One challenge with symmetric encryption is securely sharing the secret key.

For example, if I encrypt a password-protected document and email it to someone, sending the password through the same email account could create a security problem.

Someone who gains access to that mailbox could potentially obtain both:

```text
Encrypted File + Password
```

A separate secure method may therefore be required to exchange the key.

The challenge becomes more significant as the number of people who need access increases.

---

## 🧰 Symmetric Encryption Algorithms

The room introduced three important symmetric encryption standards:

- DES
- 3DES
- AES

---

## DES — Data Encryption Standard

**DES** was adopted as a standard in 1977.

It uses a:

```text
56-bit key
```

As computing power increased, DES became vulnerable to brute-force attacks.

A DES key was successfully broken in less than 24 hours in 1999, demonstrating that DES could no longer provide adequate security.

---

## 3DES — Triple DES

**3DES** applies DES three times.

Its key size is:

```text
168 bits
```

with effective security of:

```text
112 bits
```

3DES served as an interim solution after DES became insecure.

It was later deprecated and should be replaced by stronger modern encryption such as AES, although it may still exist in legacy systems.

---

## AES — Advanced Encryption Standard

**AES** was adopted as a standard in 2001.

AES supports key sizes of:

```text
128 bits
192 bits
256 bits
```

AES represents a modern symmetric encryption standard compared with DES and 3DES.

---

# 🔓 Asymmetric Encryption

Unlike symmetric encryption, **asymmetric encryption uses two different keys**.

These are:

```text
Public Key
Private Key
```

The public key can be shared, while the private key must remain protected.

For confidentiality, data encrypted using the public key can be decrypted using the corresponding private key.

```text
Public Key
    ↓
Encryption
    ↓
Ciphertext
    ↓
Decryption
    ↓
Private Key
```

This approach is also known as **public key cryptography**.

---

## 🔐 Public and Private Keys

The important distinction is:

### Public Key

Can be shared with others.

### Private Key

Must remain secret and protected by its owner.

This allows asymmetric cryptography to address some of the key-distribution challenges associated with symmetric encryption.

---

## 🧮 Asymmetric Cryptographic Systems

Examples introduced in this room include:

- **RSA**
- **Diffie-Hellman**
- **Elliptic Curve Cryptography (ECC)**

Asymmetric cryptography generally uses larger keys and tends to be slower than symmetric cryptography.

---

## 🔢 RSA Key Sizes

The room discussed RSA key sizes such as:

```text
2048 bits
3072 bits
4096 bits
```

The material identifies **2048 bits** as the recommended minimum RSA key size.

---

## 🔢 Diffie-Hellman Key Sizes

The room also discussed Diffie-Hellman key sizes including:

```text
2048 bits
3072 bits
4096 bits
```

with 2048 bits presented as the recommended minimum.

---

## 🧮 Elliptic Curve Cryptography

**ECC** can provide comparable levels of security using shorter keys than some other asymmetric systems.

An example provided in the room was:

```text
256-bit ECC ≈ 3072-bit RSA
```

This demonstrates that simply comparing key lengths between different cryptographic algorithms does not necessarily indicate their relative security.

---

## 👩‍💻 Alice and Bob

Cryptography examples frequently use fictional characters called **Alice** and **Bob**.

They represent two parties who want to communicate securely.

For example:

```text
Alice  →  Secure Communication  →  Bob
```

Using these characters makes it easier to explain encryption, key exchange, and other cryptographic concepts.

---

# 🧮 Basic Mathematics in Cryptography

Modern cryptography relies heavily on mathematics.

This room introduced two mathematical operations commonly encountered in cryptographic concepts:

- XOR
- Modulo

---

## ❌ XOR Operation

**XOR**, meaning **Exclusive OR**, is a logical operation used in binary arithmetic.

It compares two bits.

The result is:

- `1` when the bits are different
- `0` when the bits are the same

The XOR symbol is commonly represented as:

```text
⊕
```

or:

```text
^
```

---

## 📊 XOR Truth Table

| A | B | A ⊕ B |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

Therefore:

```text
0 ⊕ 0 = 0
0 ⊕ 1 = 1
1 ⊕ 0 = 1
1 ⊕ 1 = 0
```

---

## 🧠 XOR Example

Consider:

```text
1010
1100
```

Performing XOR bit by bit:

```text
1 ⊕ 1 = 0
0 ⊕ 1 = 1
1 ⊕ 0 = 1
0 ⊕ 0 = 0
```

Therefore:

```text
1010
⊕ 1100
------
  0110
```

---

## 🔐 XOR and Cryptography

XOR has several useful properties.

For any binary value `A`:

```text
A ⊕ A = 0
```

and:

```text
A ⊕ 0 = A
```

XOR is also **commutative**:

```text
A ⊕ B = B ⊕ A
```

and **associative**:

```text
(A ⊕ B) ⊕ C = A ⊕ (B ⊕ C)
```

These properties allow XOR to demonstrate a simple form of symmetric encryption.

---

## 🔑 XOR Encryption Example

Let:

```text
P = Plaintext
K = Secret Key
C = Ciphertext
```

Encryption can be represented as:

```text
C = P ⊕ K
```

To recover the plaintext:

```text
C ⊕ K
```

Substituting the ciphertext:

```text
(P ⊕ K) ⊕ K
```

Because:

```text
K ⊕ K = 0
```

we get:

```text
P ⊕ 0 = P
```

Therefore:

```text
C ⊕ K = P
```

This demonstrates how XOR can be used to illustrate symmetric encryption.

---

# ➗ Modulo Operation

Another mathematical operation used in cryptography is the **modulo operation**.

Modulo is commonly represented as:

```text
%
```

or:

```text
mod
```

Modulo returns the **remainder after division**.

---

## 🧮 Modulo Examples

### Example 1

```text
25 % 5 = 0
```

because:

```text
25 = 5 × 5 + 0
```

### Example 2

```text
23 % 6 = 5
```

because:

```text
23 = 3 × 6 + 5
```

### Example 3

```text
23 % 7 = 2
```

because:

```text
23 = 3 × 7 + 2
```

---

## 🔄 Modulo is Not Reversible

An important property I learned is that modulo is not reversible.

For example:

```text
x % 5 = 4
```

does not give us one unique value for `x`.

Many different values can satisfy the equation.

The modulo operation also produces a non-negative result smaller than the positive divisor.

For:

```text
a % n
```

the result falls within:

```text
0 to n - 1
```

---

## 🐍 Using Python for Large Numbers

Cryptography often requires working with very large integers.

The room noted that Python can be useful for these calculations because its built-in integer type can handle integers of arbitrary size.

For example:

```python
print(23 % 6)
```

Output:

```text
5
```

This makes Python useful when experimenting with the mathematical concepts used in cryptography.

---

## ⚖️ Symmetric vs Asymmetric Encryption

| Feature | Symmetric | Asymmetric |
|---|---|---|
| Keys | One shared key | Public and private key pair |
| Encryption/Decryption | Same key | Different keys |
| Key secrecy | Shared key must remain secret | Private key remains secret |
| Examples | DES, 3DES, AES | RSA, Diffie-Hellman, ECC |
| Relative performance | Generally faster | Generally slower |
| Key distribution | Can be challenging | Public key can be shared |

---

## 🎯 Key Takeaways

- Cryptography provides techniques for secure communication and data protection.
- Cryptography helps protect confidentiality, integrity, and authenticity.
- Plaintext is readable information before encryption.
- Ciphertext is the unreadable result produced by encryption.
- A cipher is an algorithm used for encryption and decryption.
- A cryptographic key is used with the cipher to encrypt or decrypt information.
- The Caesar Cipher demonstrates the basic concept of shifting characters but is insecure by modern standards.
- Symmetric encryption uses the same secret key for encryption and decryption.
- DES, 3DES, and AES are examples of symmetric encryption algorithms.
- AES supports 128-bit, 192-bit, and 256-bit keys.
- Asymmetric cryptography uses a public and private key pair.
- RSA, Diffie-Hellman, and ECC are examples of asymmetric cryptographic systems.
- Public keys can be shared, while private keys must remain protected.
- XOR compares binary bits and is useful in cryptographic operations.
- XOR can demonstrate a simple symmetric encryption process.
- Modulo calculates the remainder after division and is commonly encountered in cryptography.
- Mathematics provides important building blocks for modern cryptography.

---

## 📸 Proof of Completion

![Cryptography Basics](../../assets/14-cryptography-basics.jpg)
