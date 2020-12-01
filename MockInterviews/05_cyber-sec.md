# Cybersecurity & Other Questions

NOTE: Most of these questions weren't actually asked in a mock interview, but may still be worth noting.

## How are Hashes used to encrypt Passwords?

## What are Tokens?

- Have to do cookies
- Future request to a website will store a token, which expires after a certain time

## What is Secure Sockets Layer (SSL) and Transport Layer Security (TLS, which is successor of SSL)?

- HTTPS requests
- Provide digital certificates, which are published by trusted certificate authorities

## What is encryption?

- protects data in transit
- 2-way function
- Plain text data is scrambled by a 'cypher' algorithm
- Same algorithm or key is needed on other side to decode

## What are the 2 types of Encryption?

1.  Asymmetric

- 1-way encryption, or 1 key encrypts and another 1 decrypts
- SSL/TLS uses this model

2.  Symmetric

- Each party has own key that bout encrypts and decrypts

## What is Hashing?

- ensures data hasn't been altered (authentication)
- 1-way function that uses an algo to take confidential data and map it to a hexadecimal string of a certain size (128m 160, 256, 320 bits)
- hashed text should always be unique like an ID
- browser will take hashed text that has been decoded, then use the hash algorithm to hash the decoded file to see if new hashed text matches previous hashed text

## What is salting?

- 'sprinkling' a few more characters onto your password or data to be hashed so that the hash value is changed from what it would have been
- protects against brute force and rainbow table (???) attacks
