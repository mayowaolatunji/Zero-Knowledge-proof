# How Do Zero-Knowledge Proofs Work?

A zero-knowledge proof operates through the verifier posing a set of actions for the prover to perform that can only be executed correctly if the prover has knowledge of the underlying information. Should the prover merely guesses at the result of these actions, the verifier's test will ultimately demonstrate the inaccuracy with a high probability.\
\
Beyond the innate features (soundness, completeness & Zero-knowledge) of zero-knowledge-proof, the primary form of a ZKP consists of three elements: witness, challenge, and response.

The witness is the secret information that the prover wants to prove knowledge of. This information is the basis for the set of questions that the verifier will ask the prover. The prover begins the proving process by randomly selecting a question from the set, calculating the answer based on their assumed knowledge of the witness, and sending it to the verifier.



The verifier then randomly selects another question from the set and asks the prover to answer it. The prover accepts the question, calculates the answer based on their assumed knowledge of the witness, and returns it to the verifier. This process of challenge and response continues, with the verifier selecting additional questions from the set and the prover providing answers until the verifier is satisfied that the prover truly has knowledge of the witness.



To ensure that the prover isn't just guessing blindly and getting the correct answers by chance, the verifier selects more questions to ask. By repeating this interaction many times, the possibility of the prover faking knowledge of the witness drops significantly until the verifier is satisfied.

\

## Concealing Knowledge in ZKP

One of the key techniques used by ZKPs to conceal information is "**blinding**." Blinding is a method of obscuring the details of the knowledge being shared by multiplying it with a random number. For example, suppose the prover wants to prove that they know a particular secret number, but they don't want to reveal the number itself. To achieve this, they can multiply the secret number by a random value, producing a new "blinded" number that can be safely shared with the verifier. The verifier can then use the blinded number to verify the proof without learning anything about the original secret number.

Another way that ZKPs conceal information is through the use of "**commitment schemes.**" A commitment scheme is a method for committing to a piece of information without revealing anything about the information itself. This is achieved through the use of a cryptographic function that takes the original information and produces a "commitment" to that information. The commitment can be shared with the verifier and later used to prove that the prover knew the original information without revealing the information itself.

