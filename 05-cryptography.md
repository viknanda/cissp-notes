# Cryptography

Cryptography is a method of storing and transmitting data in a form that only those it is intended for can read and process. It is considered a science of protecting information by encoding it into an unreadable format.

Substitution cipher – one character is replaced with another character Monoalphabetic substitution cipher – uses only one alphabet Polyalphabetic substitution ciper – uses multiple alphabets at a time Encryption is a method of transforming original data, called plaintext or cleartext, into a form that appears to be random and unreadable, which is called ciphertext.

Plaintext --> encryption --> Ciphertext --> decryption --> Plaintext A system that provides encryption and decryption is referred to as a cryptosystem and can be created through hardware components or program code in an application.

A secret value called a key, works with the the encryption algorithm to encrypt and decrypt the text. The key is a value that is made up of a large sequence of random bits.

An algorithm contains a keyspace, which is a range of values that can be used to construct a key.

The algorithm, the set of mathematical rules, dictates how enciphering and deciphering take place.

The strength of the encryption method comes from the algorthm, secrecy of the key, length of the key, initialization vectors and how they all work together.

Cryptosystems provide confidentiality, authenticity, integrity and nonrepudiation services. They do not provide availability of data or systems.

Nonrepudiation means that a sender cannot deny sending the message at a later date.

Cryptanalysis is the practice of obtaining plaintext from ciphertext without a key or of breaking the encryption.

Key clustering refers to the instance when two different keys generate the same ciphertext from the same plaintext.

Work factor refers to the estimated time, effort and resources necessary to break a cryptosystem.

The substitution cipher replaces bits, characters or blocks of characters with different bits, characters or blocks.

The transposition cipher does not replace the original text with different text, but moves the original text around. It rearranges the bits, characters, or blocks of characters to hide the original meaning.

Simple substitution and transposition ciphers are vulnerable to attacks that perform frequency analysis.

Other types of ciphers include the running key cipher and the concealment cipher.

Steganography is a method of hiding data in another media so that the very existence of the data is concealed. Steganography is mainly used by hiding messages in graphic images. The least significant bit of each byte of the image can be replaced with bits of the secret message. This practice does not afect the graphic enough to be detected.

The Clipper Chip is an NSA-designed tamperproof chip for encrypting data. It is one of the two chips implemented in the US Government's Escrowed Encryption Standard (EES). Each chip has a unit key, which is used to encrypt a copy of each user's session key, not the message itself. Each Clipper Chip has a unique serial number and a copy of the unit key is stored in the database under this serial number. The sending Clipper Chip generates and sends a Law Enforcement Access Field (LEAF) value included in the transmitted message. This field value contains the serial number of the Clipper Chip used to encrypt the message in the first place. This is how the government or law enforcement knows which unit key to retrieve from the database. This unit key enables them to decrypt and find out the session key, which enables them to actually decrypt the message and eavesdrop on the conversation. The unit key is split into two pieces and kept in different databases maintained by two different escrow agencies. The Clipper Chip was based on the SkipJack algorithm that was classified and never opened for public review or testing.

Weaknesses of Clipper Chip

- The SkipJack algorithm was never publicly scrutinized and tested

- An 80-bit key is very weak

- A 16-bit checksum can be defeated

- The Clipper Chip ID tagged and identified every communication session Kerckhoff's Principle states that the only secrecy involved with a cryptography system should be the key.

He claimed the algorithm should be publicly known. He asserted that if security were based on too many secrets, there could be more vulnerabilities.

Key escrow refers to the process of splitting keys into two sections and being given to two different escrow agencies to maintain.

In a cryptosystem that uses symmetric cryptogrpahy, both parties will be using the same key for encryption and decryption. Symmetric keys are also called secret keys because this type of encryption relies on each user to keep the ley a secret and properly protected.

For N people, N(N-1)/2 symmetric keys will be required.

Security of symmetric key encryption is totally dependent on how well user protect their keys.

Strengths:

- Much faster than asymmetric systems

- Hard to break if using a large key size Weaknesses:

- Requires a secure mechanism to deliver keys properly

- Each pair of users needs a unique pair of keys so the number of keys grows and key management can become overwhelming

- Provide confidentiality, but not authenticity or nonrepudiation Examples of symmetric algorithms:

- Data Encryption Standard (DES)

- Triple-DES (3DES)

- Blowfish

- IDEA

- RC4, RC5 and RC6

- Advanced Encryption Standard (AES)

In asymmetric systems, each entity has different keys or asymmetric keys. The two different asymmetric keys are mathematically related. If a message is encrypted by one key, the other key is required in order to decrypt the message.

In a public key system, the pair of keys is made up of one public key and one private key. The public key can be known to everyone and the private key must only be known and used by the owner.

If confidentiality is the most important security service to a sender, then she would encrypt the data with the receiver's public key. This is called secure message format.

If authentication is the most important security service to the sender, then she would encrypt the data with her private key. This is called open message format.

Secure and signed message format: the sender would encrypt the message with her private key and then encrypt it again with the receiver's public key. This provides confidentiality and authentication for the delivered message.

Strengths:

- Better key distribution than symmetric systems

- Better scalability than symmetric systems

- Can provide authentication and nonrepudiation Weaknesses:

- Works much more slowly than symmetric systems

- Mathematically intensive tasks Examples of asymmetric key algorithms:

- RSA

- Elliptic Curve Cryptosystem (ECC)

- Diffie-Hellman

- El Gamal

- Digital Signature Algorithm (DSA)

- Knapsack There are two main types of symmetric algorithms: stream and block ciphers.

When a block cipher algorithm is used for encryption and decryption purposes, the message is divided into blocks of bits. These blocks are then put through substitution, transposition and other mathematical functions, one block at a time.

The properties of a cipher should contain confusion and diffusion.

Confusion – the complexity of the algorithm and not knowing the key value cause confusion Diffusion – accomplished by puttng the bits within the plaintext through many different functions so that they are dispersed throughout the algorithm.

A stream cipher treats the message as a stream of bits and performs mathematical functions on them individually. When using a stream cipher, the same plaintext bit will be transformed into different ciphertext bit each time it is encrypted.

Some stream ciphers use a keystream generator, which produces a stream of bits that is XORed with the plaintext bits to produce ciphertext. This by itself is not a strong solution. Stick a key and apply it to the keystream generator to make the algorithm stronger.

A strong and effective stream cipher algorithm contains the following characteristics:

- Long periods of no repeating patterns within keystream values

- Statistically unpredictable keystream

- A keystream not linearly related to the key

- Statistically unbiased keystream (as many 0s as 1s)

Since stream ciphers encrypt and decrypt one bit at a time, they are more suitable for hardward implementations. Block ciphers are easier to implement in software because they work with blocks of data that the software is used to working with.

DES is a block symmetric encryption algorithm. When 64-bits blocks of plaintext go in, 64-bit blocks of ciphertext come out. It is also a symmetric algorithm, meaning the same key is used for encryption and decryption. It uses a 64-bit key: 56 bits make up the true key and 8 bits are used for parity.

Electronic Code Book (ECB) Mode – this operates like a code book. A 64-bit data block is entered into the algorithm with a key and a block of ciphertext is produced. For a given block of plaintext and a given key, the same block of ciphertext is always produced. ECB incorporates padding to address the problem of not all messages ending up in neat and tidy 64-bit blocks. This mode is usually used for small amounts of data like encrypting and protecting encryption keys.

Applications include challenge-response encryption operations, some key management tasks and encryption of PINs in ATM transactions.

Cipher Block Chaining (CBC) Mode – this mode does not reveal a pattern (unlike ECB mode) because each block of text, the key and the value based on the previous block is processed in the algorithm and applied to the next block of text. This gives a more random resulting ciphertext. This provides dependence between the blocks and in a sense, they are chained together.

A particular ciphertext is dependent upon all blocks before it, not just the previous block.

Cipher Feedback (CFB) Mode – in this mode, the previously generated ciphertext from the last encrypted block of data is inputted into the algorithm to generate random values. The random values are processed with the current block of plaintext to creat ciphertext. Similar to CBC mode but emulates a stream cipher by using a keystream generator. CBC mode operates purely as a block cipher.

This mode is used when encrypting individual characters is required.

Output Feedback (OFB) Mode – this mode is very similar to CFB mode, but it is functioning like a stream cipher by generating a stream of random binary bits to be combined with the plaintext to create ciphertext.

The ciphertext is fed back to the algorithm to form a portion of the next input to encrypt the next stream of bits.

Double-DS has a key length of 112 bits but there is a specific attack against Double-DES that reduces its work factor to about the same as DES.

3DES uses 48 rounds in its computation, which makes it highly resistant to differential cryptanalysis and approximately 2^56 times stronger than DES. However, there is a heavy performance hit. It can take up to three times longer than DES to perform encryption and decryption.

DES-EEE3 uses three different keys for encryption. Data is encrypted, encrypted, encrypted.

DES-EDE3 uses three different keys and it encrypts, decrypts and encrypts.

DES-EEE2 and DES-EDE2 are the same as the previous mode but the first and third operations use the same key.

Advanced Encryption Standard – Rijndael was NIST's choic in replacing DES. It is the algorithm that is used to protect sensitive but unclassified US government information. Rijndael is a block cipher with a variable block length and key length.

International Data Encryption Algorithm (IDEA) is a block cipher and operates on 64-bit blocks of data.

The 64-bit data block is divided into 16 smaller blocks and each has 8 rounds of mathematical functions performed on it. The key is 128 bits long. IDEA is used in PGP encryption software.

Blowfish is a block cipher that works on 64-bit blocks of data. The key length is up to 448 bits and the data blocks go through 16 rounds of cryptographic functions. Designed by Bruce Schneier.

RC5 is a block cipher that has a variety of parameters it can use for block size, key size and the number of rounds used. It was created by Ron Rivest and analyzed by RSA. The block sizes in this algorithm are usually 32, 64 or 128 bits and the key size goes up to 2048 bits.

RSA is a public key algrithm that is most popular when it comes to asymmetric algorithms. The security of this algorithm comes from the difficulty of factoring large numbers. The public and private keys are functions of a pair of large prime numbers and the necessary activities required to decrypt a message from ciphertext to plaintext using a private key is comparable to factoring a product into two prime numbers.

Using RSA's one-way function, RSA provides encryption and signature verification, and the inverse direction performs decryption and signature generation.

A one-way function is a mathematical function that is easier to compute in one direction than in the opposite direction.

El Gamal is a public key algorithm that can be used for digital signatures, encryption and key exchange. It is based on calculating discrete logarithms in a finite field.

ECC algorithms use the properties of elliptic curves. The elliptic curves provide ways of constructing groups of elements and specific rules of how the elements within these groups combine. The properties between the groups are used to build cryptographic algorithms.

ECC provides encryption functionality requiring a smaller percentage of the resources required by RSA and other algorithms. ECC can also provide the same level of protection with a key size smaller than that of RSA because of the efficiency.

In a hybrid system, the asymmetric key is used to encrypt the symmetric key; the symmetric key is used to encrypt the message.

Symmetric algorithm creates keys that are used for encrypting bulk data and an asymmetric algorithm creates keys that are used for automated key distribution.

Faster algorithm is used on the message (symmetric) and the slower algorithm is used on the key (asymmetric).

Message encrypted with symmetric key.

Symmetric key encrypted with receiver's public key.

Decrypt symmetric key with receiver's private key.

Decrypt message with symmetric key.

A session key is a secret key that is used to encrypt messages between two users but is only good for one communication session between the users.

Diffie-Hellman Key Exchange enables users to exchange secret keys over a nonsecure medium. The Diffie-Hellman algorithm is used for key distribution, and it cannot be used to encrypt and decrypt messages or for digital signatures.

Attribute Symmetric Asymmetric Keys One key is chared between two or One entity has a public key and the other more entities. entity has a private key.

Key exchange Out-of-band. Symmetric key is encrypted and sent with message; thus, the key is distributed by inbound means.

Speed Algorithm is less complex and Algorithm is more complex and slower.

Faster.

Use Bulk encryption, which means Key encryption and distributing keys.

encrypting files and communication paths.

Security service provided Confidentiality. Authentication and nonrepudiation.

Public key infrastructure (PKI) consists of programs, data formats, procedures, communication protocols, security policies and public key cryptographic mechanisms working in a comprehensive mannr to enable a wide range of dispersed people to communicate in a secure and predictable fashion. PKI establishes a level of trust within an environment. PKI is an ISO authentication framework that uses public key cryptography and the X.509 standard protocols.

PKI provides authentication, confidentiality, nonrepudiation and integrity of the messages exchanged. PKI is a hybrid system of symmetric and asymmetric key algorithms and methods.

Each person who wants to participate in a PKI requires a digital certificate, which is a credential that contains the public key for that individual along with other identifying information. The certificate is created and signed by a trusted third party or a certificate authority (CA). When the CA signs the certificate, it binds the individual's identity to the public key and the CA takes liability for the authenticity of that public key.

A CA is a trusted organization that maintains and issues digital certificates. When a person requests a certificate, the registration authority (RA) verifies that individual's identity and passes the certificate request off to the CA. The CA constructs the certificate, signs it and passes the certificate request off to the CA.

Revocation is handled by the CA and stored on a certificate revocation list (CRL). This is a list of every certificate that has been revoked.

A certificate is the mechanism used to associate a public key with a collection of components sufficient to uniquely authenticate the claimed owner. The standard for how the CA creates the certificate is X.509, which dictates the different fields used in the certificate and the valid values that can populate those fields.

Certificate includes the serial number, version number, identity information, algorithm information, lifetime dates and the signature of the issuing authority.

The RA performs the certification registration duties. The RA establishes and confirms the identity of an individual, initiates the certification process with a CA on behalf of an end user and performs certificate lifecycle management functions. The RA cannot issue certificates but can act as a middleman between the user and the CA.

In a PKI, an individual requests another individual's public key from the directory. The other individual can validates the first individual's public key with the CA.

A one-way hash is a function that takes a variable-length string, a message and produces a fixed-length value called a has value that represents that original data. A hash value is also called a message digest.

Hashing process:

- The sender puts the message through a hashing function.

- A message digest value is generated.

- The message digest is appended to the message.

- The sender sends the messageto the receiver.

- The receiver puts the message (only) through a hashing function.

- The receiver generates her own message digest value.

- The receiver compares the two message digest values. If they are the same, the message has not been altered.

Steps of a Message Authentication Code (MAC):

- The sender concatenates a symmetric key with the message.

- The result is put through a hashing algorithm.

- A MAC value is generated.

- The MAC value is appended to the message.

- The sender sends the message to the receiver.

- The receiver concatenates a symmetric key with the message.

- The receiver puts the results through a hashing algorithm and generates her own MAC value.

- The receiver compares the two MAC values. If they are the same, the message has not been modified.

One-Way Hashing Function:

- It provides integrity of a message, not confidentiality or authentication.

- The result of a one-way hash is a hashing value also referred to as a message digest.

- The hashing value is used in hashing to create a fingerprint for a message.

Message Authentication Code:

- A symmetric key is combined with the message before being put through a hashing algorithm.

- It provides integrity and data origin authentication.

A digital signatue is a hash value that has been encrypted with the sender's private key.

The hashing function ensures the integrity of the message and the signing of the hash value provides authentication and nonrepudiation. The act of signing just means that the value was encrypted with a private key.

Overview of choices in cryptography:

- A message can be encrypted, which provides confidentiality.

- A message can be hashed which provides integrity.

- A message can be digitally signed, which provides authentication, nonrepudiation and integrity.

- A messaged can be encryped and digitally signed, which provides confidentiality, authentication, nonrepudiation and integrity.

Digital Signature Standard (DSS) – federal standard proposed by NIST in 1991 Characteristics of good cryptographic hashing functions:

- The hash should be computed over the entire message.

- The hash should be a one-way function so that messages are not disclosed by their values.

- It should be impossible, given a message and its hash value, to compute another message with the same hash value.

- It should be resistant to birthday attacks, meaning an attacker should not be able to find two messages with the same hash value.

Algorithm Description MD2 One-way function. Produces a 128-bit hash value. Much slower than MD4 and MD5.

MD4 One-way function. Produces a 128-bit hash value.

MD5 One-way function. Produces a 128-bit hash value. More complex than MD4.

HAVAL One-way function. Variable-length hash value. Modification of MD5 algorithm and provides more protection against attacks that affect MD5.

SHA One-way function. Produces a 160-bit hash value. Used with DSA.

If a hashing algorithm produces the same value for two distinctly different messages, this is called a collision.

The output of a hashing algorithm is n and to find a message through a brute force attack that results in a specific hash value would require hashing 2^n random messages. Finding two messages that hash to the same value would only require 2^(n/2) messages to be reviewed.

A one-time pad uses a truly nonrepeating set of random bits that are combined bitwise using the binary XOR function. The bits of the message are XORed to the bits in the pad to generate ciphertext.

Rules for Keys and Key Management:

- The key length should be long enough to provide the necessary level of protection.

- Keys should be stored and transmitted by secure means.

- Keys should be extremely random and use the full spectrum of the keyspace.

- The key's lifetime should correspond with the sensitivity of the data it is protecting.

- The more the key is used, the shorter its lifetime should be.

- Keys should be backed up or escrowed in case of emergencies.

- Keys should be properly destroyed when their lifetime comes to an end.

Link encryption encrypts all the data along a specific communication path, as in a satellite link, T3 line or telephone circuit. Not only is the user information encrypted, but the header, trailers, addresses and routing data that are part of the packets are also encrypted. The only traffic that is not encrypted in this technology is the data link control messaging information. Link encryption provides extra protection against packet sniffers and eavesdroppers.

In end-to-end encryption, the headers, addresses, routing and trailing information are not encrypted, enabling attackers to learn more about a capture packet and where it is headed.

If encryption happens at the lower layers of the OSI model, then it is link encryption; at the higher layers, it is considered end-to-end encryption.

Advantages of end-to-end encryption:

- It protects information from start to finish throughout the network.

- It provides more flexibility to the user in choosing what gets encrypted and how.

- Higher granularity of encryption is available because each application or user can use a different key.

- Each hop computer on the network does not need to have a key to decrypt each packet.

Disadvantages of end-to-end encryption:

- Headers, addresses and routing information are not encrypted and therefore not protected.

- The destination system needs to have the same encryption mechanisms to properly decrypt the message.

Advantages of link encryption:

- All data is encrypted, including headers, addresses and routing information.

- Users do not need to do anything to initiate it; it works at a lower layer in the OSI model.

Disadvantages of link encryption:

- Key distribution and management is more complex because each hop device must receive a key; and when the keys change, each must be updated.

- Messages are decrypted at each hope; thus, there are more points of vulnerability.

Multipurpose Internet Mail Extension (MIME) is a technical specification indicating how multimedia data and email attachments are to be transferred.

Secure MIME (S/MIME) is a standard for encrypting and digitally signing electronic mail that contains attachments and for providing secure data transmissions.

Privacy-Enhanced Mail (PEM) is an Internet standard to provide secure e-mail over the Internet and for in-house communication infrastructures. The protocols within PEM provide authentication, message integrity, encryption and key management.

- Messages encrypted with DES in CBC mode

- Public key management provided using RSA

- X.509 standard for certification structure and format The Message Security Protocol (MSP) is the military's PEM.

PGP is a cryptosystem that has all the necessary components: confidentiality through the IDEA encryption algorithm, integrity by using the MD5 hashing algorithm, authentication by using the publickey ceritificates and nonrepudiation through the use of cryptographically signed messages.

PGP does not use a hierarchy of CAs but relies on a "web of trust" in its key management approach. Each user generates and distributes his or her public key and users sign each other's public keys, which creates a community of users who trust each other.

Each user keeps a collection of signed public keys he has received from other users in a file referred to as a key ring. Each key in that ring has a parameter that indicates the level of trust assigned to that user and the validity of that particular key.

Secure Hypertext Transport Protocol (S-HTTP) is HTTP with added-on security features. S-HTTP can provide data integrity and sender authentication capabilities. S-HTTP computes a hash value of the message and the value can then be digitally signed.

HTTPS protects the communication channel between two computers, messages and all. HTTPS uses SSL and HTTP to provide a protected circuit between a client and server.

SSL protects a communication channel instead of individual messages.

Server sends message to client indicating that a secure session needs to be established.

Client sends its security parameters.

Server compares security parameters to its own until it finds a match --> handshaking phase.

Server authenticates to client by sending it a digital certificate. Server may require client to send a digital certificate for mutual authentication but that is rare.

Client generates a session key and encrypts it with the server's public key.

Encrypted key is sent to the Web server and they both use this symmetric key to encrypt the data they send back and forth.

SSL can be thought of as residing at the bottom of session layer and top of transport layer. For CISSP, it is a transport layer protocol.

Secure Electronic Transaction (SET) is a cryptographic protocol and infrastructure developed to send encrypted credit card numbers over the Internet.

HTTP is a stateless protocol, meaning that each HTTP connection has no memory of any prior connections.

This is one main reason to use cookies. Cookies are text files that a browser maintains on a user's hard drive; they can be used to track demographic information, etc.

Secure Shell (SSH) functions as a type of tunnelling mechanism that provides terminal-like access to remote computers.

Client requests SSH connection.

Handshake to find out protocol version.

Algorithm negotiation and key exchange.

Secure session setup.

Client runs remote application.

The Internet Protocol Security (IPSec) protocol suite is a method of setting up a secure channel for protected data exchange between two devices. It is used to establish virtual private networks (VPNs) among networks across the Internet.

Authentication Header (AH) is the authenticating protocol.

Encapsulating Security Payload (ESP) is an authenticating and encrypting protocol that uses cryptographic mechanisms to provide source authentication, confidentiality and message integrity.

IPSec can work in one of two modes: transport mode, where the payload of the message is protected and tunnel mode, where the payload and the routing and header information is also protected.

The SA (security association) is critical to the IPSec architecture and is a record of the configurations the device needs to support an IPSec connection.

SAs are directional, so a device will have one SA for outbound traffic and a different SA for inbound traffic for each individual communication channel.

Each device has a security parameter index (SPI) that keeps track of the different SAs and tells the device which one is appropriate to invoke for the different packets is receives. The SPI value is in the header of an IPSec packet.

AH Protocol computes ICV value over Network Header | Transport Header | Data Payload.

ESP Protocol computs ICV value only over Transport Header | Data Payload (takes care of NAT situations).

ICV is basically a MAC (message authentication code) value.

Internet Key Exchange (IKE), Simple Key Management Protocol for IP (SKIP) are all network layer protocols.

Ciphertext-only attack – attacker has ciphertext of several messages. Each of the messages has been encrypted using the same encryption algorithm. The attacker's goal is to discover the key that was used in the encryption algorithm.

Known-plaintext attack – attacker has plaintext and ciphertext of one or more messages. Goal is again to discover the key used to encrypt the messages.

Chosen-plaintext attack – attacker has plaintext and ciphertext, but the attacker can choose the plaintext that gets encrypted to see the corresponding ciphertext.

Chosen-ciphertext attack – attacker can choose the ciphertext to be decrypted and has access to the resulting decrypted plaintext.

Man-in-the-middle Attack A sends C her public key. B intercepts and sends C his own public key.

C sends A his public key. B intercepts and sends A his own public key.

A and C communicate with "each other's" public keys. However, keys they have are B's public key, so communication between A and C can be decrypted using B's private key.

Using digital signatures during the session-key exchange can circumvent the man-in-the-middle attack.

Dictionary attack – take a list of commonly used passwords and run it through a one-way function and store the results in a file. Next, compare file results of hashed values to password file stolen from an authentication server.

A replay attack is when an attacker captures some type of data and resubmits it with the hopes of folling the receiving device into thinking it is legitimate information. Many times the data that is captured and resubmitted is authentication information and the attacker is trying to authenticate herself as someone else to gain unauthorized access.

Timestamps and sequence numbers are countermeasures to replay vulnerabilities.

Side Channel Attacks – looking around something is referred to as looking at that item's side channels.
