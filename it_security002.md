
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

