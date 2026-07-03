# TryHackMe Day 58–59: Cryptography Concepts

## 🧠 What I Learned

In this room, I learned the fundamentals of cryptography and why it is one of the most important security controls used on the internet today. Cryptography helps protect sensitive information by ensuring that only authorized people can read data while also preventing unauthorized modifications.

I also learned how cryptography supports the Confidentiality and Integrity principles of the CIA Triad. Without encryption, attackers who intercept network traffic could easily read or alter sensitive information.

---

## Key Concepts

### What is Cryptography?

Cryptography is the process of protecting information by converting readable data into an unreadable format that can only be understood by someone with the correct key.

Its primary goals are:

- Protect confidentiality
- Maintain data integrity
- Secure communication over untrusted networks

---

### Plaintext vs Ciphertext

One of the first concepts I learned was the difference between plaintext and ciphertext.

- **Plaintext** is readable information.
- **Ciphertext** is encrypted information that appears meaningless without the correct key.

Example:

Plaintext

```
HELLO
```

Ciphertext

```
KHOOR
```

The encrypted version cannot be understood unless it is decrypted with the correct key.

---

### Keys and Algorithms

Encryption relies on two important components.

**Algorithm**

- The method used to encrypt and decrypt data.
- Algorithms are usually public knowledge.

**Key**

- The secret value used by the algorithm.
- Security depends on protecting the key, not hiding the algorithm.

This follows an important security principle:

> The algorithm can be public, but the key must remain secret.

---

## Symmetric Encryption

I learned that symmetric encryption uses **one shared key** for both encryption and decryption.

Both the sender and receiver must possess the same secret key.

### Advantages

- Very fast
- Efficient for encrypting large amounts of data
- Used for files, disks and network traffic

### Disadvantage

The biggest challenge is securely sharing the secret key with another person.

If someone intercepts the key, they can decrypt every message protected with it.

---

## The Caesar Cipher

To understand encryption, the room introduced the Caesar Cipher.

Each letter is shifted by a fixed number of positions.

For example, using a key of **3**:

```
HELLO
```

becomes

```
KHOOR
```

Although this cipher demonstrates how encryption works, it is **not secure** because there are only a small number of possible shifts, making it easy to crack.

Modern encryption algorithms such as AES are much more secure.

---

## Asymmetric Encryption

Unlike symmetric encryption, asymmetric encryption uses **two keys**.

- Public Key
- Private Key

The public key can be shared with anyone.

The private key must never be shared.

A message encrypted with the public key can only be decrypted using the matching private key.

This solves the key distribution problem found in symmetric encryption.

---

## How HTTPS Uses Cryptography

One of the most interesting things I learned is how HTTPS combines both encryption methods.

When visiting a secure website:

1. The browser requests the server's public key.
2. The server provides its digital certificate.
3. A secure symmetric session key is generated.
4. The rest of the communication uses fast symmetric encryption.

This hybrid approach provides both security and performance.

---

## Digital Certificates

I also learned about digital certificates.

Certificates:

- Contain a website's public key
- Verify the website's identity
- Are issued by trusted Certificate Authorities (CAs)

Browsers verify certificates before establishing secure HTTPS connections.

This prevents attackers from impersonating legitimate websites.

---

## Symmetric vs Asymmetric Encryption

### Symmetric Encryption

- Uses one shared key
- Very fast
- Best for encrypting large amounts of data
- Requires secure key sharing

### Asymmetric Encryption

- Uses public and private keys
- Slower
- Solves the key exchange problem
- Used for HTTPS, certificates and secure communication

Most modern systems combine both methods.

---

## Key Takeaways

From this room I learned that:

- Cryptography protects confidentiality and integrity.
- Plaintext becomes ciphertext after encryption.
- Keys are more important to protect than algorithms.
- Symmetric encryption is fast but has key distribution challenges.
- Asymmetric encryption solves secure key exchange.
- HTTPS combines both encryption methods for secure web browsing.
- Digital certificates verify website identities and establish trust online.

This room helped me understand how encryption works behind the scenes whenever I browse secure websites, use online banking, or send encrypted messages.

---

## 📸 Proof of Completion

![Cryptography Concepts](../../assets/cryptography-concepts.jpg)
