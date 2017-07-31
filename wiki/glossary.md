## An Access token
An access token provides authenticated and secure access to Virgil Security services. The access token also allows the API to associate your app requests with your Virgil Security Developer’s account.

## Asymmetric Algorithm
See public key algorithm.

## Asymmetric Key
One of a pair of keys used with an asymmetric cryptographic algorithm. Such an algorithm uses two cryptographic keys: a "public key" for encryption and a "private key" for decryption. In signature and verification, the roles are reversed: the public key is used for verification, and the private key is used for signature generation. The most important feature of such algorithms is that their security does not depend on keeping the public key secret (though it may require some assurance of authenticity of public keys, for example, that they be obtained from a trusted source). Secrecy of the private key is required.

## Card Request
A specially formatted electronic message (sent to a server) used to request a card. The request must contain the information required by the application to authenticate the request, plus the public key of the entity requesting the card.

## Ciphertext
A message that has been encrypted.

## Context
The security data relevant to a connection. A context contains information such as a session key and duration of the session.

## CryptoAPI
Application programming interface that enables application developers to add authentication, encoding, and encryption to Windows-based applications.

## Cryptographic Algorithm
A mathematical function used for encryption and decryption. Most cryptographic algorithms are based on a substitution cipher, a transposition cipher, or a combination of both.

## Cryptographic Key
A cryptographic key is a piece of data that is required to initialize a cryptographic algorithm. Cryptographic systems are generally designed so that their security depends only on the security of their cryptographic keys and not, for example, on keeping their algorithms secret.
There are many different types of cryptographic keys, corresponding to the wide variety of cryptographic algorithms. Keys can be classified according to the type of algorithm they are used with (for example, as symmetric or asymmetric keys). They can also be classified based on their lifetime within a system (for example, as long-lived or session keys).

## Cryptographic Service Provider
(CSP) An independent software module that actually performs cryptography algorithms for authentication, encoding, and encryption.

## Cryptography
The art and science of information security. It includes information confidentiality, data integrity, entity authentication, and data origin authentication.

## CryptoSPI
The system program interface used with a cryptographic service provider (CSP).

## Data Encryption
See encryption.

## Data Encryption Function
See encryption and decryption functions.

## Decryption
The process of converting ciphertext to plaintext. Decryption is the opposite of encryption.

## DER
See Distinguished Encoding Rules.

## DH
See Diffie-Hellman algorithm.

## Diffie-Hellman algorithm
(DH) A public key algorithm used for secure key exchange. Diffie-Hellman cannot be used for data encryption. This algorithm is specified as the key exchange algorithm.

## Digital Signature
Data that binds a sender's identity to the information being sent. A digital signature may be bundled with any message, file, or other digitally encoded information, or transmitted separately. Digital signatures are used in Public Key environments and provide authentication and integrity services.

## Digital Signature Algorithm
(DSA) A public key algorithm specified by Digital Signature Standard (DSS). DSA is only used to generate digital signatures. It cannot be used for data encryption.

## Digital Signature Key Pair
See signature key pair.

## Digital Signature Standard
(DSS) A standard that specifies the Digital Signature Algorithm (DSA) for its signature algorithm. DSA is a public key cipher that is only used to generate digital signatures and cannot be used for data encryption.

## Encryption
The process of converting plaintext to ciphertext to help prevent it from being read and understood by an unauthorized party. Encryption is the opposite of decryption.

## Encrypted Data
Data that has been converted from plaintext into ciphertext. Encrypted messages are used to disguise the content of a message when it is sent or stored.

## Encryption and Decryption Functions
Simplified message functions used to encode and encrypt (or decode and decrypt) data. As a set, these functions include support for simultaneously encrypting and decrypting data.

## Exchange Key Pair
A public/private key pair used to encrypt session keys so that they can be safely stored and exchanged with other users.

## Hash
A fixed-size result obtained by applying a mathematical function (the hashing algorithm) to an arbitrary amount of data. (Also known as "message digest.").

## Hashing Functions
A set of functions used to create and destroy hash objects, get or set the parameters of a hash object, and hash data and session keys.

## Initialization Vector
(IV) A sequence of random bytes appended to the front of the plaintext before encryption by a block cipher. Adding the initialization vector to the beginning of the plaintext eliminates the possibility of having the initial ciphertext block the same for any two messages. For example, if messages always start with a common header (a letterhead or "From" line) their initial ciphertext would always be the same, assuming that the same cryptographic algorithm and symmetric key was used. Adding a random initialization vector eliminates this from happening

## Integrity
The completeness and accuracy of a message after it has been sent or stored.

## Key Length
Values specified by some providers that indicate the length of the public/private key pairs and session keys used with that provider.

## Key Pair
The Public and Private key pair comprise of two uniquely related cryptographic keys (basically long random numbers). The Public Key is what its name suggests - Public. It is made available to everyone via a publicly accessible repository or directory. On the other hand, the Private Key must remain confidential to its respective owner. Because the key pair is mathematically related, whatever is encrypted with a Public Key may only be decrypted by its corresponding Private Key and vice versa.

## Message
Any data that has been encoded for transmission to or received from a person or entity. Messages may be encrypted for privacy, digitally signed for authentication purposes, or both

## National Institute of Standards and Technology
(NIST) A division of the United States Department of Commerce that publishes official standards for both government and private sector computer systems. These standards are published as Federal Information Processing Standards(FIPS) publications. In 1987, NIST was directed to define standards for ensuring the security of sensitive but unclassified information in government computer systems.

## Plaintext
A message that is not encrypted. Plaintext messages are sometimes referred to as cleartext messages.

## Private Key
The secret half of a key pair used in a Public Key algorithm. Private keys are typically used to encrypt a symmetric session key, digitally sign a message, or decrypt a message that has been encrypted with the corresponding Public Key.

## Privilege
The right of a user to perform various application-related operations, such as reading, writing or changing something. A user's access token contains a list of the privileges held by either the user, the user's groups or devices.

## Public/Private key pair
A set of cryptographic keys used for Public Key cryptography. For each user, a cryptographic service provider usually maintains two public/private key pairs: an exchange key pair and a Digital Signature key pair. Both key pairs are maintained from session to session.

## Public Key
A cryptographic key typically used when decrypting a session key or a digital signature. The Public Key can also be used to encrypt a message, guaranteeing that only the person with the corresponding Private Key can decrypt the message.

## Public Key algorithm
An asymmetric cipher that uses two keys, one for encryption, the Public Key, and the other for decryption, the Private Key. As implied by the key names, the Public Key used to encode plaintext can be made available to anyone. However, the Private Key must remain secret. Only the Private Key can decrypt the ciphertext. The Public Key algorithm used in this process is slow (on the order of 1,000 times slower than symmetric algorithms), and is typically used to encrypt session keys or digitally sign a message.

## Public Key Cryptography Standards
(PKCS) A set of syntax standards for Public Key cryptography covering security functions, including methods for signing data, exchanging keys, public key encryption and decryption, and other security functions.

## Public Key Encryption
Encryption that uses a pair of keys, one key to encrypt data and the other key to decrypt data. In contrast, symmetric encryption algorithms that use the same key for both encryption and decryption. In practice, Public Key cryptography is typically used to protect the session key used by a symmetric encryption algorithm. In this case, the public key is used to encrypt the session key, which in turn was used to encrypt some data, and the private key is used for decryption. In addition to protecting session keys, Public Key cryptography may also be used to digitally sign a message (using the Private Key) and validate the signature (using the Public Key).

## Salt Value
Random data that is sometimes included as part of a session key. When added to a session key, the plaintext salt data is placed in front of the encrypted key data. Salt values are added to increase the work required to mount a brute-force (dictionary) attack against data encrypted with a symmetric-key cipher.

## Secure Sockets Layer Protocol
(SSL) A protocol for secure network communications using a combination of public and secret key technology.

## Security Protocol
A specification that defines security-related data objects and rules about how the objects are used to maintain security on a computer system.

## Server
A computer that responds to commands from a client computer. The client and server work together to perform distributive application functionality.

## Session
An exchange of messages under the protection of a single piece of keying material. For example, SSL sessions use a single key to send multiple messages back and forth under that key.

## Session Key
A relatively short-lived cryptographic key, often negotiated by a client and a server based on a shared secret. A session key's lifespan is bounded by the session to which it is associated. A session key should be strong enough to withstand cryptanalysis for the lifespan of the session. When session keys are transmitted, they are generally protected with key exchange keys (which are usually asymmetric keys) so that only the intended recipient can access them.

## SHA
The CryptoAPI name for the Secure Hash Algorithm.

## Signature Card
A Virgil Card that contains a Public Key that is used to verify digital signatures.

## Signature Functions
Functions used to create and verify digital signatures.

## Signature Key Pair
The public/private key pair used for authenticating (digitally signing) messages. See [Public/Private key pair](https://github.com/VirgilSecurity/virgil/blob/wiki/wiki/glossary.md#publicprivate-key-pair)

## Signature Private Key
See [Private Key](https://github.com/VirgilSecurity/virgil/blob/wiki/wiki/glossary.md#private-key).  

## Symmetric Key
A secret key used with a symmetric cryptographic algorithm (that is, an algorithm that uses the same key for both encryption and decryption). Such a key needs to be known to all communicating parties.
