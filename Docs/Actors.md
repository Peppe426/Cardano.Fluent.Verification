 # Actors
 These actors work together to provide a system where passwords are unnecessary, and security is enhanced using fresh, one-time challenge responses sent over encrypted channels. Additionally, the possibility of configuring multi-user access with policy attachments allows for more robust security measures such as multisig authorizations
 
 ### Identity Owner 
- An individual who holds a DID and manages their own identity credentials.

Individuals who create DIDs to establish a self-sovereign identity. They control their identity without depending on any centralized authority.

### Identity Verifier 
- A party or system responsible for validating the authenticity of DIDs and associated credentials.

Verifiers who verify the DID and its associated real-life human identity. Verification can include checking the authenticity of the individual’s cryptographic credentials.

### Credential Authority 
- Entities that issue cryptographic credentials to DIDs, serving as trusted authorities in the verification process.

Credential Issuers who issue cryptographic credentials associated with the DID which can include standards like X.509, PGP, or public keys from various cryptographic systems like Bitcoin's ECDSA (elliptic curve digital signature algorithm) or Cardano's Twisted Edward curves.

### Access Manager 
A system or protocol that manages access control through the use of hardware devices or key management systems, ensuring secure user interactions.

Entities setting Access Control, such as using hardware devices, PGP, or other key management systems to ensure that only those with the correct keys can perform challenge-response protocols for secure interactions.


### Authorization Coordinator 
- An entity responsible for coordinating multisig authorizations and policy enforcement for user access.

Administrators assigning Multi-signature (multisig) authentication where, for instance, every time a user attempts to sign in, another party may receive a notification to authorize the sign-in, attaching policies to the keys as needed.


