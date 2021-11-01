# Encryption, decryption, and cracking

Human languages tend to use some letters more than others. For example, "E" is the most popular letter in the English language. We can analyze the frequency of the characters in the message and identify the most likely "E" and narrow down the possible shift amounts based on that.


**Encryption:** scrambling the data according to a secret key (in this case, the alphabet shift).

**Decryption**: recovering the original data from scrambled data by using the secret key.

**Code cracking:** uncovering the original data without knowing the secret, by using a variety of clever techniques.


## encryption techniques 

example: 

The Caesar Cipher is a simple substitution cipher which replaces each original letter with a different letter in the alphabet by shifting the alphabet by a certain amount.

**A symmetric encryption** is any technique where the same key is used to both encrypt and decrypt the data. 


**Vigenère Cipher** : French cryptologists invented the Vigenère Cipher in the mid 1500s. The cipher was considered especially strong.

**Encryption**:
The Vigenère cipher uses an entire word as the shift key, as opposed to the Caesar Cipher’s single shift amount.

**Cracking the cipher**

The Vigenère Cipher is a type of polyalphabetic cipher, and it's a harder code to crack than the Caesar Cipher due to the use of an entire shift word.



**Modern ciphers**

In the age of computers, ciphers can't just be hard to crack by an enterprising human; they have to be hard to crack by a computer that can do trillions of calculations per second.

**Fortunately, cryptologists have invented encryption techniques that are secure in the digital world, and are continuing to improve them every year.**



## Public key encryption


![](https://cdn.kastatic.org/ka-perseus-images/850bd82076969173551d38dbe09fe9bcc2249bc4.svg)

 It's an asymmetric encryption technique which uses different keys for encryption and decryption, allowing computers over the Internet to securely communicate with each other.

 1- Key generation

Each person (or their computer) must generate a pair of keys that identifies them: a private key and a public key.

2-Key exchange

The sending and receiving computers exchange public keys with each other via a reliable channel, like TCP/IP. The private keys are never exchanged.

3- Encryption

The sending computer encrypts the secret data using the receiving computer's public key and a mathematical operation.


4- Sending encrypted data

The sender can now safely transmit the encrypted data over the Internet without worry of onlookers.

5- Decryption

Now the receiver can decrypt the message, using their private key. That's the only key that can be used to decrypt the message (in the world!).



## Caesar cipher

one of the simplest and most widely known encryption techniques. It is a type of substitution cipher in which each letter in the plaintext is replaced by a letter some fixed number of positions down the alphabet.


![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4a/Caesar_cipher_left_shift_of_3.svg/1920px-Caesar_cipher_left_shift_of_3.svg.png)

The Caesar cipher can be easily broken even in a ciphertext-only scenario. Two situations can be considered:

+ an attacker knows (or guesses) that some sort of simple substitution cipher has been used, but not specifically that it is a Caesar scheme;
+ an attacker knows that a Caesar cipher is in use, but does not know the shift value.
