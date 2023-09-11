# Class 14

### Intro to password hashing

1. Define the term “hashing”.<br>
   Hashing is the process of taking input data of any size and producing output data of a fixed size. A hash function is used to generate the fixed-size output data, which is commonly referred to as a hash value, hash code, or simply hash. This value represents a unique digital fingerprint of the input data. Hashing is used in a variety of applications such as cryptography, data integrity checking, digital signatures, and password storage. When used for password storage, hashing is a way to store user passwords securely by converting them into a fixed-size hash that is almost impossible to reverse engineer back to the original password.

2. Explain to a non-technical friend what a hash function does to a password.<br>Think of it like this: if your password is a key, the hash function is like the key maker who creates a new, secret copy of your key that only the website or app can use to open the lock. Nobody can steal or duplicate your original key because it's been turned into a secret code that only the website or app knows how to decode.

### bcrypt overview

1. What does it mean to ‘salt’ a password?<br>
    Adding salt to a password means adding a random string of characters to the password before hashing it. This random string of characters helps to make the hashed password more secure because it is unique to each user. Even though two users may have the same password, their hashed passwords will not be the same because of the added 'salt'. This makes it much harder for attackers to guess or crack passwords, even if they have access to the hashed passwords.
2. What piece of information would a hacker need to access in order to find the ‘salt’ string for your passwords?<br>If a hacker wants to find the 'salt' string for passwords, they would need to have access to the source code of the application or website that uses the salted passwords. The salt value is often stored in the same database as the hashed password, but it is not a secret value and can be easily seen by anyone with access to the database. Therefore, it's important for developers to keep their source code and databases secured to prevent unauthorized access.

### jBCrypt (the paragraphs and code example at the top of the page)

1. How does the Blowfish block cipher handle the increased computation speed of new computers?<br>The Blowfish block cipher used in jBCrypt handles the increased computation speed of new computers by allowing for the computation cost of the algorithm to be parameterized and increased as necessary. The work factor of the algorithm is 2^log(rounds), where the log_rounds parameter determines the complexity. By increasing the log_rounds value, the computation cost of the algorithm is increased, making it slower and more difficult for attackers to crack passwords using fast hardware. This ensures that the system remains resistant to off-line password cracking, even as computers become more powerful.

2. What are the issue with the two most commong password hashes for Java (“Java password hash” and “Java password encryption”)?<br>According to the jBCrypt website, the top two Google search results (as of May 24, 2006) for "Java password hash" and "Java password encryption" offer bad advice. One of these approaches uses an unsalted hash, which allows for reverse dictionary lookups of passwords, and the other recommends using reversible encryption, which is rarely necessary and should only be used as a last resort. These approaches are not secure enough to protect passwords against various types of attacks, making them inadequate solutions for password hashing in Java.