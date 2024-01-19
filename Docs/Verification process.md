# Verification process

### Example, verify tweets

For a company like Twitter (X) that wants to verify its tweets, the suitable actor could be:
**Content Authenticator** 
- An entity that verifies the authenticity of content posted on its platform, ensuring it originates from legitimate and verified sources. This would involve linking tweets to verified DIDs where Twitter can confidently assert the tweet's origin and possibly the identity (whether public or pseudonymous) of the person or organization behind the account.

To facilitate this kind of verification, Twitter could act as both a Credential Authority by issuing its own set of verification credentials to user DIDs, and a Content Authenticator by verifying tweets against those credentials. Therefore, Twitter would ensure that each tweet is traceable to a verified DID, adding a layer of trust and authenticity to the content shared on its platform.

### Fluent.Verification

- Social Media Identity Registrar (SMIR) - This entity registers and manages the decentralized identifiers (DIDs) for each Twitter user, ensuring that each DID is unique and corresponds to a real user or entity.

- Broadcast Authenticator - A role or system at Twitter that would sign each tweet with a unique cryptographic key, which corresponds to the DID of the user. This assures that the tweet originates from the legitimate DID owner.

- Signature Validator - A client-side component or service that verifies the signature on each tweet, confirming whether it is authentic (signed by the user's DID key) or not (unsigned or unverified).

- Key Protection Service - A security service that manages the private keys used for signing tweets, ensuring that the keys are stored securely, perhaps in hardware, and are physically accessible only to individuals with proper authorization.
 
- Authority Role Identifier - This might reflect who in the organization, based on their role, can sign official communications. For example, the CEO might have one key, the social media manager another, and so on. Each key could indicate the role of the signer.
 
- Insider Threat Mitigator - A system or set of protocols that prevents internal personnel from compromising accounts, even when they have escalated privileges.
 
- Blockchain DID Registrar (BDR) - An entity that records verified DIDs onto a blockchain, such as Cardano, providing an immutable registry of identities which can be referenced for verification.
 
- (User) Access Control Programmer - The individual user is responsible for setting up their level of access control and deciding whether to obtain a DID and how their verification processes should be managed.

For Twitter specifically, if they wanted to act as a verifier of tweets, they would take on the roles of the Broadcast Authenticator and Key Protection Service to ensure that only verified tweets carry a visible sign of authentication, similar to possessing an SSL certificate for websites that users can check to ensure the integrity and origin of communications.

The system highlighted in the document enables Twitter to empower users and organizations to communicate securely. It not only strengthens security but also enhances the credibility of communication, attributing authoritative identity verification to each broadcasted message. This is of particular importance for official communications by corporations to their stakeholders or public agencies to citizens, where non-repudiation and message integrity are critical.