# RSA-Factoring-Challenge
RSA, which stands for Rivest-Shamir-Adleman, is a widely used public-key cryptosystem invented in 1977 by Ron Rivest, Adi Shamir, and Leonard Adleman. It's a fundamental system in modern computer science used for encrypting and decrypting data.

## How RSA Works:
1. Key Generation:
Two keys are generated, a public key and a private key.
The public key is distributed openly, while the private key is kept secret.

2. Encryption:
The public key is used to encrypt the message.
The public key cannot be used to decrypt, ensuring the message's secrecy.

3. Decryption:
The private key is used to decrypt the message.
The private key ensures that only the owner can decrypt the message

## RSA Algorithm steps:
1. Choose two large prime numbers `p`, `q` then calculate: `n = p * q`
2. Compute `Φ(n)` the tontient of `n`: `Φ(n) = (p - 1) * (q - 1)`
3. Choose number `e` where `1 < e < Φ(n)` and `GCD(e, Φ(n)) = 1`.
    * NOTE: Our Public Key is made of `n` and `e`.
    * `e`: Called Public exponenet and it is used to encrypt our message
4. Computing private exponenet `d`: `e.d = 1 mod Φ(n)`
5. Message encryption: `c = m^e mod n`
    * `m`: message.
    * `c`: ciphertext. 
5. Message decryption: `m = c^d mod n` 
