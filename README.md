This my My README FOR RSA-Factoring-Challenge
RSA is a relatively old algorithm, having been developed in the 1970s by Ron Rivest, Adi Shamir, and Len Adleman. It is based on the difficulty of factoring large numbers.

To understand how RSA works, let's look at an example. Suppose we want to send a message that says "Hello, world!" to our friend. We can use RSA to encrypt the message so that only our friends can read it.

First, we need to generate a pair of RSA keys. One key is public and one key is private. The public key can be shared with anyone, but the private key must be kept secret.

To generate our keys, we first choose two large prime numbers, p and q. We then compute n = pq. n is called the modulus.

We also compute another number,φ(n), which is called the totient of n. φ(n) is equal to (p-1)(q-1).

Now we choose an integer esuch that 1 < e < φ(n) and gcd(e, φ(n)) = 1. gcd(a,b) is the greatest common divisor of a and b.

e is called the public exponent and it is used to encrypt our message.

The last step is to compute d such that ed = 1 mod φ(n). d is called the private exponent and it is used to decrypt our message.

Now we have everything we need to encrypt our message. To encrypt our message, we compute the following:

c = me mod n

c is the ciphertext and m is the message we want to encrypt. To decrypt the ciphertext, we compute the following:

m = cd mod n

m is the decrypted message.

Let's try this with our example message. Suppose our public key is(e, n) = (5, 143). Our private key is d = 23.

To encrypt our message, we compute:

Note that m = message (that will be converted to an integer with padding). In our case, we will use a random number. However, if you are interested to know how that is done, here is the process

To encrypt a message, each letter in the message is converted into a number using a scheme such as ASCII. Then, for each number, it is raised to the encryption key power and divided by the modulus. The remainder of this division is the encrypted number. To decrypt a message, each encrypted number is raised to the decryption key power and divided by the modulus. The remainder of this division is the decrypted number. This number is then converted back into a letter using the same scheme as before.


COPY

COPY
c = m^e mod n

c = 88^5 mod 143

c = 9408 mod 143

c = 104
To decrypt the ciphertext, we compute:


COPY

COPY
m = c^d mod n

m = 104^23 mod 143

m = 9408 mod 143

m = 88
We can see that our message has been successfully encrypted and decrypted.

RSA is used in a wide variety of applications, including email, file sharing, and secure communications. It is also used in many different protocols, such as SSL/TLS, which is used to secure communications on the Internet.

RSA is a very versatile algorithm and it is one of the most widely used public-key algorithms in the world. However, RSA is not without its weaknesses.

The biggest weakness of RSA is that it is vulnerable to attack if the private key is compromised. This is why it is important to keep the private key secret and to use a good quality random number generator to generate the keys.

Another weakness of RSA is that it is relatively slow compared to other public-key algorithms. This is not a big problem for most applications, but it can be a problem for applications that require high performance, such as video streaming or file sharing.

Despite its weaknesses, RSA is still the most widely used public-key algorithm in the world and it is likely to remain so for the foreseeable future.

