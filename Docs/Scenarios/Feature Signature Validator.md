## Feature: Signature Validator
The scenarios address signature validation upon content submission, real-time verification on the client side, integrity maintenance of posts, public key management for new users, and processes related to key revocation. The actors involved include users (both content creators and consumers), the Signature Validator, and potentially other security services for managing compromised keys.

### Scenario: Validating the authenticity of a new post
**Given** a user submits a new post to the social media platform
**When** the Signature Validator receives the post to check its authenticity
**Then** it verifies the signature against the user's public key from the database
And if the signature matches, the post is marked as authentic and published
Else the post is flagged as potentially unauthentic and withheld from publication

### Scenario: Real-time verification of posts within a client-side application
**Given** a user is scrolling through their social media feed
**When** the client-side application presents a new post
**Then** the Signature Validator seamlessly verifies the authenticity in real-time
If the post is authentic, it displays a verified badge
Else it displays a warning to the user indicating unverified content

### Scenario: Ensuring the integrity of posts by cross-checking signatures
**Given** a post has been flagged for potential integrity issues
**When** a concerned user requests a verification of the post's authenticity
**Then** the Signature Validator cross-references the signature with the associated public key
And it confirms that the post has not been altered from its original signed state
Providing the user with assurance of the post's non-malleability

### Scenario: Managing a public key for a new user's content
**Given** a new user has registered and needs to generate a public key
**When** the user creates a key pair and submits the public key to the platform
**Then** the Signature Validator adds the public key to the database
And ensures it is securely stored and readily available for signature verification

### Scenario: Interaction with key revocation for compromised security
**Given** a user's security has been compromised and their private key needs to be revoked
**When** the compromised key is reported and deactivated
**Then** the Signature Validator updates the public key database to ensure no further content is signed with the old key
And any content signed with the revoked key is flagged and reassessed for authenticity