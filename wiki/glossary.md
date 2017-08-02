## Access token
An access token provides authenticated and secure access to Virgil Security services. The access token also allows the API to associate your app requests with your Virgil Security Developer’s account.

## Action ID
An ID used to compare a confirmation code with a related validation action.

## Application Key (APP KEY)
This is a Private Key, that is generated in pair with a Public Key, which is part of an App's Card. During Key Pair generation at the Virgil Development Portal, the App Key is encrypted with an additional password. The App Key has a DER format.

## Application ID (APP ID)
This is an identifier, which uniquely identifies an Application at Virgil Services.
During Application Registration at the Virgil Development Portal, the App ID is created on the App's Virgil Card. The Card has its own ID, which is also the App ID

## Asymmetric Algorithm
Asymmetric cryptography is a branch of cryptography where a secret key can be divided into two parts, a public key and a private key. The public key can be given to anyone, trusted or not, while the private key must be kept secret (just like the key in symmetric cryptography).
Asymmetric cryptography has two primary use cases: authentication and confidentiality. Using asymmetric cryptography, messages can be signed with a private key, and then anyone with the public key is able to verify that the message was created by someone possessing the corresponding private key. This can be combined with a proof of identity system to know what entity (person or group) actually owns that private key, providing authentication.
Encryption with asymmetric cryptography works in a slightly different way from symmetric encryption. Someone with the public key is able to encrypt a message, providing confidentiality, and then only the person in possession of the private key is able to decrypt it.

## Asymmetric Key
One of a pair of keys used with an asymmetric cryptographic algorithm. Such an algorithm uses two cryptographic keys: a "public key" for encryption and a "private key" for decryption. In signature and verification, the roles are reversed: the public key is used for verification, and the private key is used for signature generation. The most important feature of such algorithms is that their security does not depend on keeping the public key secret (though it may require some assurance of authenticity of public keys, for example, that they be obtained from a trusted source). Secrecy of the private key is required.

## Authentication
The process of verifying that a message was created by a specific individual (or program). Like encryption, authentication can be either symmetric or asymmetric. Authentication is necessary for effective encryption.

## Athenticated Encryption
The process of encrypting and then signing data using the Sender’s Virgil Key and the Recipient’s Virgil Card. In order to do this, the Sender’s Virgil Key must be loaded from the appropriate storage, then the Recipient’s Virgil Card must be searched for, followed by preparation of the data for transmission, which is finally signed and encrypted before being sent.
Authenticated Decryption - the process of taking data that is already both encrypted and signed, and then decrypting and verifying the data. A recipient uses their Virgil Key to decrypt the data, which is followed by using the Sender’s Virgil Card to verify the integrity of the data.

## Card Request
A specially formatted electronic message (sent to a server) used to request a card. The request must contain the information required by the application to authenticate the request, plus the public key of the entity requesting the card.

## Card Service
Virgil Card Service is a dedicated service to store and manage Virgil Cardsis. This service has the role of issuing Virgil Cards or denying requests for Cards, it also provides the ability to search and revoke Virgil Cards. The ability to issue, distribute, revoke, and manage Virgil Cards, provides the necessary capabilities for Public Key infrastructure.

## Ciphertext
Applying an encryption algorithm (or cipher) to some plaintext results in the creation of a Ciphertext. The Ciphertext is encoded information that contains an encrypted form of the plaintext, but is unreadable to any human or computer without the proper Decryption Algorithm, which is based on a private key.

## Command Line Interface (CLI)
A program and command line tool for utilizing Virgil Services. The CLI can be used for a variety of actions on Virgil Services including, generating keys, retrieving keys, key search, key revocation, data encryption and decryption, data signature and verification, etc. The CLI is available for both Mac OS and Linux platforms.

## Confirmation Code
A code used to confirm ownership of a global identifier, such as an email or phone number.

## CryptoAPI
Application programming interface that enables application developers to add authentication, encoding, and encryption to Windows-based applications.

## Crypto Library
A library of API function calls and cryptographic algorithms, used by developers to implement cryptography into their software. Virgil consists of an open-source encryption library, which implements Cryptographic Message Syntax (CMS) and Elliptic Curve Integrated Encryption Scheme (ECIES) (including RSA schema), a Key Management API, and a cloud-based Key Management Service (Virgil Keys).

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

## Decryption
The process of taking encrypted information or ciphertext and converting it back into plaintext or an unencrypted form. This can only be done with the appropriate decryption algorithm and the associated private key, whose pair is the public key that encrypted the data in the first place.

## Diffie-Hellman algorithm
(DH) A public key algorithm used for secure key exchange. Diffie-Hellman cannot be used for data encryption. This algorithm is specified as the key exchange algorithm.

## Digital Signature
Data that binds a sender's identity to the information being sent. A digital signature may be bundled with any message, file, or other digitally encoded information, or transmitted separately. Digital signatures are used in Public Key environments and provide authentication and integrity services.

## Digital Signature Algorithm
(DSA) A public key algorithm specified by Digital Signature Standard (DSS). DSA is only used to generate digital signatures. It cannot be used for data encryption.

## Digital Signature Standard
(DSS) A standard that specifies the Digital Signature Algorithm (DSA) for its signature algorithm. DSA is a public key cipher that is only used to generate digital signatures and cannot be used for data encryption.

## Encrypted Communication
When two parties desire to communicate without some third-party knowing. This communication must not be able to be read or understood by any unauthorized party, leading to the need to use a cipher and/or code. Encrypted communication can be achieved through cryptographic means, which require the use of information based keys to encrypt and later decrypt some message.

## Encrypted Storage
The storage of data that is technically out in the open for anyone to access but unable to be read or understood by anyone except the holders of the appropriate cryptographic keys. Encryption must be end-to-end for any data to be stored safely.

## Encrypting for Multiple Receipients
Encryption requires the Virgil Card of the recipient, so that only the recipient’s Virgil Key can decrypt the message. For multiple recipients, the sender must have the Virgil Card of every recipient they intend to send a message to. The sender can find Virgil Cards for each recipient using Virgil Services, which they can then use to encrypt a message for each recipient, that can only be decrypted on an individual basis

## Encryption
The process of converting plaintext to ciphertext to help prevent it from being read and understood by an unauthorized party. Encryption is the opposite of decryption.

## Encrypted Data
Data that has been converted from plaintext into ciphertext. Encrypted messages are used to disguise the content of a message when it is sent or stored.

## Encryption and Decryption Functions
Simplified message functions used to encode and encrypt (or decode and decrypt) data. As a set, these functions include support for simultaneously encrypting and decrypting data.

## Exchange Key Pair
A public/private key pair used to encrypt session keys so that they can be safely stored and exchanged with other users.

## Global Virgil Card
A Virgil Card is the primary entity of the Public Keys Service, it includes information about the user and their public key. The Virgil Card identifies a user by one of their available types, such as an email, a phone number, etc. Global Cards are created with the validation token received after verification through Virgil Identity Service. Any developer with a Virgil account can create a Global Virgil Card. Virgil Identity Service ensures the user that the account, with a particular email, has been verified and that the email owner is also the Identity owner.

## Hash
A fixed-size result obtained by applying a mathematical function (the hashing algorithm) to an arbitrary amount of data.

## Hashing Functions
A set of functions used to create and destroy hash objects, get or set the parameters of a hash object, and hash data and session keys.

## Identity service
The Virgil service is responsible for the validation of user identities in anything from emails to applications.

## Initialization Vector
(IV) A sequence of random bytes appended to the front of the plaintext before encryption by a block cipher. Adding the initialization vector to the beginning of the plaintext eliminates the possibility of having the initial ciphertext block the same for any two messages. For example, if messages always start with a common header (a letterhead or "From" line) their initial ciphertext would always be the same, assuming that the same cryptographic algorithm and symmetric key was used. Adding a random initialization vector eliminates this from happening

## Integrity (Data Integrity)
The ability to ensure and maintain that some data has a known sender (one who cannot deny having sent the data) and has not been altered over its life-cycle. Data integrity is meant to safeguard data from any unintended changes to it as a result of storage, processing, transmission, malicious intent, or human error. Proper data integrity measures ensure that the data is accurate, consistent, and has a verifiable origin. It is vital to any system that sends or receives data, where privacy is concerned.

## Key Length
Values specified by some providers that indicate the length of the public/private key pairs and session keys used with that provider.

## Key Pair
The Public and Private key pair comprise of two uniquely related cryptographic keys (basically long random numbers). The Public Key is what its name suggests - Public. It is made available to everyone via a publicly accessible repository or directory. On the other hand, the Private Key must remain confidential to its respective owner. Because the key pair is mathematically related, whatever is encrypted with a Public Key may only be decrypted by its corresponding Private Key and vice versa.

## Message
Any data that has been encoded for transmission to or received from a person or entity. Messages may be encrypted for privacy, digitally signed for authentication purposes, or both

## National Institute of Standards and Technology
(NIST) A division of the United States Department of Commerce that publishes official standards for both government and private sector computer systems. These standards are published as Federal Information Processing Standards(FIPS) publications. In 1987, NIST was directed to define standards for ensuring the security of sensitive but unclassified information in government computer systems.

## Passwordless Authentication
The ability to log into applications or systems without the need for a password, by using Virgil Services to generate encrypted challenges and responses that can only be passed with the appropriate cryptographic keys. When an app receives permission to authorize users with a Virgil account, it can request authorization from Virgil Security when a user wants to log in without a password. Virgil verifies whether the app is trusted and receives user’s private key for further access to the system. If the key is correct, Virgil authenticates the user and returns an authorization code to the app. The app then receives an authentication token which allows for a unique and secure data transmission of the rest of the user details required to grant access to the application. This allows authorized users to access the application without a password, while maintaining a higher standard of security.

## Perfect Forward Secrecy (PFS)
PFS is a technique that protects previously intercepted traffic from being decrypted even if the main private key is compromised. With PFS enabled communication, a hacker could only access information that is actively transmitted because PFS forces a system to create different keys per session. In other words, PFS makes sure there is no master key to decrypt all the traffic.

## Plaintext
A message that is not encrypted. Plaintext messages are sometimes referred to as cleartext messages.

## Private Key
This is one of two keys involved in public-key cryptography. It can be used to decrypt messages which were encrypted with the corresponding public key, as well as to create signatures, which can be verified with the corresponding public key. These must be kept secret, if they are exposed, all encrypted messages are compromised, and an attacker will be able to forge signatures.

## Private Key Password
A password set for a private key adds an additional security stage and prevents any data leakage after the private key has been compromised. It is optional but highly recommended to set a private key password.

## Privilege
The right of a user to perform various application-related operations, such as reading, writing or changing something. A user's access token contains a list of the privileges held by either the user, the user's groups or devices.

## Public Key
This is one of two keys involved in public-key cryptography. It can be used to encrypt messages for someone possessing the corresponding private key and to verify signatures created with the corresponding private key. This can be distributed publicly, hence the name.

## Public Key algorithm
An asymmetric cipher that uses two keys, one for encryption, the Public Key, and the other for decryption, the Private Key. As implied by the key names, the Public Key used to encode plaintext can be made available to anyone. However, the Private Key must remain secret. Only the Private Key can decrypt the ciphertext. The Public Key algorithm used in this process is slow (on the order of 1,000 times slower than symmetric algorithms), and is typically used to encrypt session keys or digitally sign a message.

## Public Key Cryptography Standards
(PKCS) A set of syntax standards for Public Key cryptography covering security functions, including methods for signing data, exchanging keys, public key encryption and decryption, and other security functions.

## Public Key Encryption
Encryption that uses a pair of keys, one key to encrypt data and the other key to decrypt data. In contrast, symmetric encryption algorithms that use the same key for both encryption and decryption. In practice, Public Key cryptography is typically used to protect the session key used by a symmetric encryption algorithm. In this case, the public key is used to encrypt the session key, which in turn was used to encrypt some data, and the private key is used for decryption. In addition to protecting session keys, Public Key cryptography may also be used to digitally sign a message (using the Private Key) and validate the signature (using the Public Key).

## Registration Authority (RA)
The Virgil  service is a dedicated service to authorize the Virgil Card creation that is confirmed by a 3rd-party. For the majority of cases, it's enough to communicate to the Virgil Cards Service directly, except for the creation of a Global Virgil Card. For a Global Virgil Card, it's necessary to conduct the verification step to prove that the client holds the identity.

## Recipient's Identifier
An Identifier of a recipient's Virgil Card.

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

## Symmetric Cryptography
Cryptographic operations where encryption and decryption use the same key.

## Symmetric Key
A secret key used with a symmetric cryptographic algorithm (that is, an algorithm that uses the same key for both encryption and decryption). Such a key needs to be known to all communicating parties.

## User Identity
A type of Identity which is validated using a concatenated type and value of the Identity, signed by the application's private key.

## Validation Token
A validation token is used to prevent unauthorized card registration. The validation token is generated based on the Application's Private Key and Client Identity. The global ValidationToken is used for creating global Cards. The global ValidationToken can be obtained only by checking the ownership of the Identity on the Virgil Identity Service. The private ValidationToken is used for creating Private Cards. The private ValidationToken can be generated on the developer’s side, using their own service for verification, instead of the Virgil Identity Service. Developers can also completely avoid verification, by generating a validation token using the app’s Private Key created on our Developer portal.

## Virgil Card
The Virgil Card is the main entity of Virgil Services. Every user/device is represented with a Virgil Card which contains all the necessary information to identify them. Users will also need their Virgil Card to obtain their Virgil Key for further cryptographic operations.

## Virgil Key
The Virgil Key is a Private Key, which never leaves its device. The Virgil Key allows only those who hold it to sign and decode a message. The Virgil Key has a DER format.

## Virgil Card ID
A unique identifier of a Virgil Card. Virgil Card receives its ID after its publication on Virgil Services. It is used for every operation with Virgil Cards.
Each Virgil Card is created by passing the content snapshot, which contains all data related to the Virgil Card, and is represented as a JSON. This JSON representation will be used to calculate the Virgil Card's Fingerprint. If you convert the Fingerprint to its hexadecimal representation, it will return the Virgil Card's ID.
