# Virgil Card and Public Key

Virgil Card Service is one foundation for the Public Key Infrastructure (PKI) that provides the means for safeguarding and authenticating information. The relationship between a Virgil Card holder, the Virgil Card holder's identity, and the Virgil Card holder's [Public Key](https://github.com/VirgilSecurity/virgil/blob/wiki/wiki/glossary.md#public-key) is a critical portion of PKI. This infrastructure is made up of the following parts:

- [The Public/Private Key Pair](#head1)
- [The Virgil Card Request](#head2)
- [The Virgil Card Validation](#head3)
- [The Virgil Card](#head4)
- [Your Public Key Used for Encryption](#head5)
- [Your Public Key Used for Signature Verification](#head6)
- [The Virgil Card Service Role](#head7)


# <a name="head1"></a>The Public/Private Key Pair

PKI requires the use of Public/Private key pairs. The mathematics of Public/Private key pairs is beyond the scope of this documentation, but it is important to note the functional relationship between a Public and a Private Key. PKI [cryptographic algorithms](https://github.com/VirgilSecurity/virgil/blob/wiki/wiki/glossary.md#cryptographic-algorithm) use the [Public Key](https://github.com/VirgilSecurity/virgil/blob/wiki/wiki/glossary.md#public-key) of the receiver of an encrypted message to encrypt data, and the related [Private Key](https://github.com/VirgilSecurity/virgil/blob/wiki/wiki/glossary.md#private-key) and only the related Private Key to decrypt the encrypted message.
Similarly, a [digital signature](https://github.com/VirgilSecurity/virgil/blob/wiki/wiki/glossary.md#digital-signature) of the content, described in greater detail below, is created with the signer's Private Key. The corresponding Public Key, which is available to everyone, is used to verify this signature. The secrecy of the Private Key must be maintained because the framework falls apart after the Private Key is compromised.
Given enough time and resources, a Public/Private Key pair can be compromised, that is, the Private Key can be discovered. The longer the key, the more difficult it is to use brute force to discover the Private Key. In practice, sufficiently strong keys can be used to make it unfeasible to determine the Private Key in a timely manner, making the Public Key Infrastructure a viable security mechanism. A Private Key can be stored, in protected format, on a disk, on a smart device etc. The Public Key, but not the Private Key, of the subject of a Virgil Card is included as part of the [Virgil Card request](https://github.com/VirgilSecurity/virgil/blob/wiki/wiki/glossary.md#card-request). (Hence, a Public/Private key pair must exist before making the Virgil Card request.) That Public Key becomes part of the issued Virgil Card.

# <a name="head2"></a>The Virgil Card Request

Before a Virgil Card is issued, a Virgil Card request must be generated. This request applies to one entity, for example, an end-user, a device, or an application. For discussion, assume that the entity is yourself. Details of your identity are included in the Virgil Card request. After the request is generated, it is submitted to application server-side (App Server) for authorization.  The App Server then uses your identity information to determine whether the request meets the application's criteria for issuing a Virgil Card. If the App Server approves the request, it signs Virgil Card request with its own Private Key and sends to Virgil Services for further Publication. After that end-user can find his Virgil Card at Virgil Services at any time.

# <a name="head3"></a>The Virgil Card Validation

Before issuing your users' Virgil Card, the Virgil Services verifies your App's identity. When the Virgil Card is issued, your identity is bound to the Card, which contains your Public Key. Your Virgil Card also contains the Virgil Card Service's digital signature (which can be verified by anyone who receives your Virgil Card). Because your Virgil Card contains the identity of the issuing Virgil Card Service, an interested party that trusts Virgil Services can extend that trust to your Virgil Card.
The issuance of a Virgil Card does not establish trust, but transfers trust. If the Virgil Card consumer does not trust the issuing Virgil Card Service, it will not (or at least should not) trust your Virgil Card.
A chain of signed Virgil Card allows trust to be transferred to other Virgil Cards as well. This allows parties who use different application to still be able to trust Virgil Cards (provided there is a common Virgil Card Service in the chain, that is, a service that is trusted by both parties).


# <a name="head4"></a>The Virgil Card

In addition to your Public Key and the identity of the issuing Virgil Card, the issued Virgil Card contains information about the purposes of users' Virgil Cards. When users want to start working with your Application in a browser or mobile device, Virgil can't trust them right away. Virgil needs the developer to vouch for his users, so we can trust them too. You'll need to give your users an Access Token that tells Virgil who they are and what they can do.

Furthermore, Virgil Card does not contain the Card validity period. Thus, you do not have to worry about when you need change your Virgil Card.



# <a name="head5"></a>Your Public Key Used for Encryption

If a sender wants to encrypt a message before sending it to you, the sender first retrieves your Virgil Card. After the sender determines that the Virgil Card is trusted and your Virgil Card is not revoked, the sender uses your Public Key (recall it is part of the Virgil Card) with cryptographic algorithms to encrypt the [plaintext](https://github.com/VirgilSecurity/virgil/blob/wiki/wiki/glossary.md#plaintext) message into ciphertext. When you receive the [ciphertext](https://github.com/VirgilSecurity/virgil/blob/wiki/wiki/glossary.md#ciphertext), you use your Private Key to decrypt the ciphertext.
If a third party intercepts the ciphertext email message, the third party will not be able to decrypt it without access to your Private Key.
Note that the bulk of the activities listed here are handled by software, not directly by the user.


# <a name="head6"></a>Your Public Key Used for Signature Verification

A [Digital Signature](https://github.com/VirgilSecurity/virgil/blob/wiki/wiki/glossary.md#digital-signature) is used as confirmation that a message has not been altered and as confirmation of the message sender's identity. This digital signature is dependent on your Private Key and the message contents. Using the message as input and your Private Key, cryptographic algorithms create the Digital Signature. The contents of the message are not changed by the signing process. A recipient can use your Public Key (after checking your Virgil Card's validity, issuing Virgil Card Service) to determine whether the signature corresponds to the message contents and to determine whether the message was sent by you.
If a third party intercepts the intended message, alters it (even slightly), and forwards it and the original signature to the recipient, the recipient, upon examination of the message and signature, will be able to determine that the message is suspect. Similarly, if a third party creates a message and sends it with a bogus digital signature under the guise that it originated from you, the recipient will be able to use your Public Key to determine that the message and signature do not correspond to each other.
Nonrepudiation is also supported by digital signatures. If the sender of a signed message denies sending the message, the recipient can use the signature to refute that claim.
Note that the bulk of the activities listed here are also handled by software, not directly by the user.


# <a name="head7"></a>The Virgil Card Service Role

Virgil Card Service is a repository for all Virgil Cards after their publishing. This service has the role of issuing Virgil Cards or denying requests for Cards, it also provides the ability to search and revoke Virgil Cards.  The ability to issue, distribute, revoke, and manage Virgil Cards, provides the necessary capabilities for Public Key infrastructure.
