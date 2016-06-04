jk's notes 'Mastering Bitcoin' by Andreas M. Antonopoulos: https://www.safaribooksonline.com/library/view/mastering-bitcoin/9781491902639/

###Wallet, Keys, Addresses
In bitcoin, we use public key cryptography to create a key pair that controls access to bitcoins. The key pair consists of a private key and—derived from it—a unique public key. The public key is used to receive bitcoins, and the private key is used to sign transactions to spend those bitcoins.

![alt tag](https://www.safaribooksonline.com/library/view/mastering-bitcoin/9781491902639/images/msbt_0401.png)


##Private Keys
More accurately, the private key can be any number between 1 and n - 1, where n is a constant (n = 1.158 * 1077, slightly less than 2256) defined as the order of the elliptic curve used in bitcoin (see Elliptic Curve Cryptography Explained). To create such a key, we randomly pick a 256-bit number and check that it is less than n - 1. In programming terms, this is usually achieved by feeding a larger string of random bits, collected from a cryptographically secure source of randomness, into the SHA256 hash algorithm that will conveniently produce a 256-bit number.

The following is a randomly generated private key (k) shown in hexadecimal format (256 binary digits shown as 64 hexadecimal digits, each 4 bits):

1E99423A4ED27608A15A2616A2B0E9E52CED330AC530EDCC32C8FFC6A526AEDD


##PUBLIC KEYS
The public key is calculated from the private key using elliptic curve multiplication, which is irreversible:  

**K = G . k**

where k is the private key, G is a constant point called the generator point and K is the resulting public key. The reverse operation, known as “finding the discrete logarithm”—calculating k if you know K—is as difficult as trying all possible values of k, i.e., a brute-force search. Before we demonstrate how to generate a public key from a private key, let’s look at elliptic curve cryptography in a bit more detail.
