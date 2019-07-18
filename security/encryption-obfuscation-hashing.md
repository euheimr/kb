What is the difference between Obfuscation, Hashing, and Encryption?

* Hashing is deriving a value from another, using a set algorithm. Depending on the algo used, this may be one way, may not be.

* Obfuscating is making something harder to read by symbol replacement.

* Encryption is like hashing, except the value is dependent on another value you provide the algorithm.



Hashing is a technique of creating semi-unique keys based on larger pieces of data. In a given hash you will eventually have "collisions" (e.g. two different pieces of data calculating to the same hash value) and when you do, you typically create a larger hash key size.

* Hashing - in a perfect world, it's a random oracle. For the same input X, you always recieve the same output Y, that is in NO WAY related to X. This is mathematically impossible (or at least unproven to be possible). The closest we get is trapdoor functions. H(X) = Y for with H-1(Y) = X is so difficult to do you're better off trying to brute force a Z such that H(Z) = Y

* A hash is a one way algorithm used to compare an input with a reference without compromising the reference.

* Hashing typically reduces a large amount of data to a much smaller size. This is useful for verifying the contents of a file without having to have two copies to compare, for example.

* It is commonly used in logins to compare passwords and you can also find it on your reciepe if you shop using credit-card. There you will find your credit-card-number with some numbers hidden, this way you can prove with high propability that your card was used to buy the stuff while someone searching through your garbage won't be able to find the number of your card.

* A very naive and simple hash is "The first 3 letters of a string". That means the hash of "abcdefg" will be "abc". This function can obviously not be reversed which is the entire purpose of a hash. However, note that "abcxyz" will have exactly the same hash, this is called a collision. So again: a hash only proves with a certain propability that the two compared values are the same.

* Another very naive and simple hash is the 5-modulus of a number, here you will see that 6,11,16 etc.. will all have the same hash: 1.

* Modern hash-algorithms are designed to keep the number of collisions as low as possible but they can never be completly avoided. A rule of thumb is: the longer your hash is, the less collisions it has.



Obfuscation generally involves trying to remove helpful clues (i.e. meaningful variable/function names), removing whitespace to make things hard to read, and generally doing things in convoluted ways to make following what's going on difficult. It provides no serious level of security like "true" encryption would.

* Obfuscation in cryptography is encoding the input data before it is hashed or encrypted.

* Obfuscation is hiding some information without a separate key (or with a fixed key). In this case, keeping the method a secret is how you keep the data safe.

* This makes brute force attacks less feasible, as it gets harder to determine the correct cleartext.

* Obfuscation (my opinion) - Any function f, such that f(a) = b where you rely on f being secret. F may be a hash function, but the "obfuscation" part implies security through obscurity. If you never saw ROT13 before, it'd be obfuscation

* From this, you can see how a hash algorithm might be useful for digital signatures and content validation, how encryption is used to secure your files and network connections, and why obfuscation is used for Digital Rights Management.




Encryption can follow several models, one of which is the "secret" method, called private key encryption where both parties have a secret key. Public key encryption uses a shared one-way key to encrypt and a private recipient key to decrypt. With public key, only the recipient needs to have the secret.

* I would classify them as symmetric (shared secret key) and asymmetric (public/private)

* Encryption involves storing some secret data, and the security of the secret data depends on keeping a separate "key" safe from the bad guys.







