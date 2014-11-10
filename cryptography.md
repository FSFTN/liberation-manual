# Cryptography

Cryptography is the art and science (yes, both!) of hiding information by way of encoding them into incomprehensible code. The method in which the clear text is encoded should be known to all parties to whom the information is intended to be seen.

Cryptography ensures confidentiality of data. That is, it helps you hide data from people who are not intended to see it. It does this by encoding the information in a way that can only be decoded by people who have a key. There are two kinds of cryptography. One is symmetric key cryptography where the encryption and the decryption uses the same key (the password). This is analogous to a lock with several keys. You put your stuff in a box and then lock it up and share one of many identical keys
to whoever you want to share the contents of the box with. 

The other is called asymmetric key cryptography or public key cryptography. In this system, every party involved has two keys, a private key and a pubic key. The private key, as the name suggests, is private and is kept in secret by the owner of the key. The public key can be shared freely with anyone. Anyone who wants to encrypt information to anyone else will use the recepient's public key to encrypt data. The recepient will use their own private key to decrypt it. Let's look at analogy.
Imagine that you have a bag of locks, each of which can be locked by key-A but can only be opened by key-B. You keep key-B with yourself and hand out the lock with key-A for anybody who asks for it. Now whoever wants to send you secret stuff will put it in a box and then lock the box with the lock and key-A and send it to you. They cannot themselves open the lock once they lock it because only Key-B will unlock the lock which only you have. 

# Good crypto & Snake Oil




## Terminology

- clear text
- encrypted text
- Cipher
- Encryption
- Decryption
- Encryption Key
- Privately Shared Key
- Public Key
- Private Key
- Steganography
- Cipher
