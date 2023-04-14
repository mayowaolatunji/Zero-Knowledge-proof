---
description: Introduction to Proof-of-Knowledge
---

# The Proof-of-Knowledge Concept

Proof of Knowledge (PoK) is a cryptographic protocol that allows a prover to demonstrate to a verifier that they possess certain knowledge or information without revealing the knowledge itself. The protocol ensures the correctness and reliability of the prover's claims by requiring two essential characteristics: soundness and completeness.

Soundness means that if the prover does not possess the knowledge or information they claim to possess, then the protocol should not convince the verifier otherwise. Completeness means that if the prover possesses the knowledge or information, the protocol should convince the verifier of this fact. These two characteristics are essential to ensure the security and accuracy of PoK protocols.

In the [Schnorr protocol](https://crypto.stanford.edu/cs355/19sp/lec5.pdf), the prover starts by selecting a secret value x and computing a value g^x, where g is a publicly known generator of a cyclic group G. The prover then sends a commitment to the value g^x, typically in the form of a digital signature using x as the signing key.

The verifier then sends a random challenge e to the prover. The prover responds by computing a value r = x + e \* w, where w is a random value chosen by the prover. The prover then sends the value r as evidence of their knowledge to the verifier.

The verifier checks that g^r = (commitment) \* g^e, where (commitment) is the value previously sent by the prover. If the equation is true, the verifier accepts the proof and is convinced of the prover's knowledge.

{% code overflow="wrap" %}
```python
import random
import hashlib

# Define the parameters of the Schnorr protocol
q = 2**256 - 2**32 - 977
Gx = 0x79BE667EF9DCBBAC55A06295CE870B07029BFCDB2DCE28D959F2815B16F81798
Gy = 0x483ADA7726A3C4655DA4FBFC0E1108A8FD17B448A68554199C47D08FFB10D4B8
g = (Gx, Gy)

# Generate a random secret value x
x = random.randint(1, q-1)

# Compute the commitment to the value g^x
commitment = hashlib.sha256(str(g).encode() + str(pow(g, x, q)).encode()).hexdigest()

# Send the commitment to the verifier

# Verifier generates a random challenge value e
e = random.randint(1, q-1)

# Prover computes r = x + e*w
w = random.randint(1, q-1)
r = (x + e*w) % q

# Prover sends r to verifier

# Verifier checks that g^r = commitment * g^e
if pow(g, r, q) == (int(commitment, 16) * pow(g, e, q)) % q:
    print("Proof is valid!")
else:
    print("Proof is invalid.")
```
{% endcode %}

\
In the context of Bitcoin, the Schnorr protocol is used to implement digital signatures for transactions. When a user wants to spend some Bitcoin, they create a transaction that includes a digital signature of the transaction data. The signature is computed using the Schnorr protocol, with the user's private key x as the secret value. The signature serves as proof that the user is authorized to spend the Bitcoin without revealing their private key.

