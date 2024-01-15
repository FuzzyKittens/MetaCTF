## RSA Encryption

start with two prime numbers, p and q.

N = Modulus (p*q)

r = (p-1)*(q-1)

Generate candidates for (1 mod r).  "What numbers divided by r result in a remainder of 1?"

Pick the candidate that can be factored into two numbers, e and d.

e = Encryption Key (Public Key)
d = Decryption Key (Private Key)

Enc = (msg)^e mod N

Dec = (enc)^d mod N


