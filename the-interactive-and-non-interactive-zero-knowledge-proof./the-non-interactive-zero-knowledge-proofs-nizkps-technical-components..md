# The Non-interactive zero-knowledge proofs (NIZKPs) technical components.

#### Commitment scheme

A commitment scheme is used to allow the prover to commit to their witness in a way that cannot be changed later. This allows the verifier to check the prover’s claim without revealing the witness.

#### Hash functions

Hash functions are used to generate a random seed for the commitment scheme and to compress the size of the proof.

#### Public parameters&#x20;

NIZKP schemes typically require a set of public parameters, which are generated during a one-time setup phase. These parameters are used in the verification process to ensure that the proof is valid.

#### Trapdoor function&#x20;

A trapdoor function is used to ensure that the prover cannot generate false proof without knowing a secret key. This allows the verifier to trust that the proof is valid even if the prover is trying to cheat.

#### Fiat-Shamir heuristic&#x20;

The Fiat-Shamir heuristic is used to convert an interactive proof into a non-interactive proof. This involves using a hash function to generate a random value from the verifier’s challenges, which the prover can use to complete the proof without interacting with the verifier.

#### Public reference string or common setup&#x20;

A set of public parameters generated through a trusted setup process that is used by all parties to generate and verify proofs. This enables NIZKPs to achieve highly efficient proofs while still providing a high degree of security.

\
