---
description: The two main types of  Zero-Knowledge Proofs.
---

# Zk-SNARKs & zk-STARKs.

### [zk-SNARKs](https://minaprotocol.com/blog/what-are-zk-snarks)

Stands for **Zero-Knowledge** [**Succinct**](https://cointelegraph.com/explained/zk-starks-vs-zk-snarks-explained) **Non-Interactive Argument of Knowledge**, which implies the type of zero-knowledge proof protocol that allows for the efficient verification of computational integrity without requiring interaction between the prover and verifier.

#### Succinctness&#x20;

implies that the proof is smaller than the witness and can be verified quickly, which is useful for blockchain applications.&#x20;

This efficiency is particularly important for blockchain systems, as it enables the network to process large numbers of transactions quickly and with minimal computational overhead. In addition, the low storage requirements of zk-SNARKs make them suitable for use in resource-constrained environments, such as mobile devices or IoT devices, where storage space is limited.

#### Non-interactivity&#x20;

means that the prover and verifier only interact once, unlike interactive proofs that require multiple rounds of communication, making zk-SNARKs efficient.

#### Argumentation&#x20;

means that the proof satisfies the soundness requirement, making cheating extremely unlikely.

#### Of Knowledge&#x20;

refers to the fact that without knowing the secret information or witness, it is nearly impossible for a prover to produce valid proof. In other words, the prover must have access to the witness to construct valid proof; otherwise, they would not be able to demonstrate knowledge of the information being proven.\
\


### zk-STARKs

zk-STARKs stands for Zero-Knowledge Scalable Transparent Argument of Knowledge. The name provides insight into the technical key components and implications of this type of zero-knowledge proof.

<figure><img src="https://cdn-fagpn.nitrocdn.com/nvawPUgmLuenSpEkZxPTWilYhwRGNGyf/assets/images/optimized/rev-25c5cdf/wp-content/uploads/Screen-Shot-2022-10-13-at-2.52.35-PM-1536x798.png" alt=""><figcaption><p><a href="https://minaprotocol.com/blog/zk-you-should-know-snarks-starks">Mina</a></p></figcaption></figure>

#### Zero-knowledge

As with zk-SNARKs, zk-STARKs also provide zero-knowledge proofs. Verifiers can validate the integrity of a statement without learning anything else about the statement.

#### Scalable

Unlike zk-SNARKs, which have a fixed size and cannot scale, zk-STARKs are highly scalable, meaning they can handle larger computational tasks while maintaining a low degree of complexity. This makes zk-STARKs ideal for blockchain and other decentralized systems where scalability is critical.

#### Transparent

Unlike zk-SNARKs, which require a trusted setup phase to generate the public parameters used to create the proof, zk-STARKs are transparent, meaning they do not require a trusted setup. This makes zk-STARKs more resistant to attacks and reduces the risk of centralization.

#### Argument&#x20;

Similar to zk-SNARKs, zk-STARKs also satisfy the soundness requirement, ensuring that cheating is highly unlikely.

Of Knowledge: As with all zero-knowledge proofs, zk-STARKs require access to secret information, which is called the "witness." Without access to the witness, it is difficult if not impossible, for a prover to construct a valid zk-STARK.

<figure><img src="https://s3.cointelegraph.com/storage/uploads/view/8db6bab22357a6a79e63219861b31262.jpg" alt=""><figcaption></figcaption></figure>
