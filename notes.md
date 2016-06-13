https://www.reddit.com/r/Bitcoin/comments/3025v8/how_does_the_blockchain_know_that_your_private/

The blockchain doesn't need your Private Key. It just needs proof that you know the Private Key. The Public Key you provide when you want to spend Bitcoins has to A) hash to the Bitcoin Address the coins were sent to and B) decrypt the signature which can only have been created with the matching Private Key. By being able to encrypt a signature that the Public Key can decrypt you have proven you know the Private Key. By verifying that same Public Key hashes to the Bitcoin Address you have proven you own the address by proving you know the Private Key which matches the Public Key which matches the Bitcoin Address.
The confusing part is how do they know that the private key is correct?
Only the one true Private Key can encrypt a signature that can be decrypted by the Public Key.
