
#### Symmetric cryptography


Symmetric-key algorithm

    use same key to encrypt and decrypt messages

    substitution cipher-->encryption mechanism that replaces your plaintext with ciphertext

    caesar Cipher--> decryption substitution alphabet key

    TOT13-->alphabet rotated 13 places

        a) stream cipher-->Takes stream of input and encrypts one digit at a time outputting one char at a time each

        b) block cipher--> takes data in, places it into block of fixed size and encodes the entire block as one

    initialization vector--> a bit random data incorporated into encryption key and the key used to encrypt data

#### Symmetric encryption Algorithm

DES-Data Encryption Standards:-by IBM

    -Designed in 1970

    -uses 64 bit key sizes

    -8 bit used for parity checking

    -adaopted as official FIPS

FIPS-Federal Standard Information Processing

    - encrypting government data

brute-force attack-guessing codes to crack a password/ algorithm

NIST -National Institute os Standards and Technology

    Adopted AES a replacement of DES

    Advanced Encryption standards

Factors to consider when choosing algorithms

    speed

    ease of implementation

    RC4(Rivest Cipher 4)-->gained widespread adoption because of its simplicity of use\

[Symmetric Encryption](http://www.rc4nomore.com/)

### Asymmetric cryptography / Public key ciphers

Different keys are used to encrypt and decrypt

Public key signatures-> uses public key and signature  and private key
        --> a small modification, verification fails

Guarantee:

    Confidentiality ->Encryption decryption

    Authenticity

    Non-repudiation -> validate message author

MAC--> A bit of information that allows authentication of received message, ensuring the right sender

HMAC-->Keyed-hash message authentication code

    --> uses hash functions and algorithm

CMACs-->Cipher-Based message Authentication codes

    CBC-MAC-->Cipher Block Chaining Message authentication codes

#### Asymmetric encryption algorithm

RSA--> First asymmetric cryptography system

    --> deals with generation and distribution of encryption keys

DSA->Digital signature Algorithm

    ->used for signing and verifying data

DH->Diffie-Hellman

    -->Key exchange algorithm

ECC->Elliptic curve cryptography

    -->public key encryption algorithm that uses the algebraic structure for elliptic curves over

    finite fields to generate secure keys

Elliptic curve variants:

    DH->ECDH
    
    DSA->ECDSA

[Sonny playstation Attack](https://nakedsecurity.sophos.com/2012/10/25/sony-ps3-hacked-for-good-master-keys-revealed/)

[Game piracy caused by hackers](https://www.theguardian.com/technology/gamesblog/2011/jan/07/playstation-3-hack-ps3)



#### Hashing

Function/operations that takes arbitrary data input and maps it to an output of fixed size, called hashing/digest


cryptographic hashing id one directional unlike encryption

Hash collisions-->Two different input mapping to the same output

#### Hashing Algorithms

MD5-->operates on 512 blocks bits 128 bit hash digest

SHA1-->designed by NSA

    -->part of secure hash Algorithm suit functions

    used in:

        TLS/SSL

        PGP SSH

        IPsec

MIC--> Message integrity check

    Hash digest of a message at hand ensuring no content are modified

#### supplementary reading

[Theoretical attacks against SHA1](https://eprint.iacr.org/2005/010)

[Formulation of the Attack](https://www.schneier.com/blog/archives/2005/02/sha1_broken.html)

[collisions demonstrated in the aatack](https://eprint.iacr.org/2007/474)

[SHA1 publication collision](https://shattered.io/)



Bruteforce are difficult to protect from

    needs time

    needs resources

Rainbow table: recovering stolen password hashes tables

password salt

    additional randomized data that's added into the hashing function to generate a hash that's unique to the pswd

    and salt combination


#### Cryptography application

public Key Infrastructure:(PKI)

    defines creation,storage and distribution of digital certificate

digital certificate:

    File that proves that an entity owns certain public key

    contains:

        Info on public key

        Registered owner

        Digital signature

CA-Certificate Authority:

    Responsible for storing,issuing and signing certificates

RA-Registration Authority:

    verify signing of certificate

Types of certificate

    SSL/TLS certificate-->for web browsing

    self-signed certificate--> by same org

    SSL/TLS client-->auth client to server

    code signing certificate-->used for signing executable programs

Root CA-->the signing auth

    intermediary/subordinate --<signed to start signing other certificate>

    leaf/end-entity--> a certificate that has no auth as CA

X.509 --> Defines the format of digital certificate

    -Also defines Certificate revocation list (CRL) for distributing no longer valid certs

    - Serial number-> unique identifier for certificate

    - certificate signature Algorithm= indicate what public key algorithm  and  Hashing algorithm is used

    - Issue Name-< Auth that signed the certificate>

    -Validity=Not before and Not after (Dates for the validity of the certificate)

    -Subject=Contain identification info about the entity

    -subject public key info-Def the algorithm of the public key along with public key itself

    -Certificate Signature Algorithm=same as Subject public key info field the two must match

    -certificate signature Value-The digital signature date itself

Web of Trust:

    Individuals instead of CA sign public keys for each other

[X.509 standards](https://www.ietf.org/rfc/rfc5280.txt)
