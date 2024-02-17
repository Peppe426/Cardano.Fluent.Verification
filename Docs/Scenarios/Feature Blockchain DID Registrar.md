## Feature: Blockchain DID Registrar (BDR)
The scenarios describe the core functionalities of the Blockchain DID Registrar, such as recording and maintaining DID records on a blockchain, facilitating identity verification, providing API access for cross-referencing DIDs, updating DID records, and supporting regulatory audit requirements. The actors involved include users who require DIDs, verifiers, external systems that interface with the BDR, and regulatory authorities.

### Scenario: Registering a new user's DID on the blockchain
**Given** a new user has signed up and requires a unique decentralized identifier (DID)
**When** the user submits their registration request to the platform
**Then** the Blockchain DID Registrar records and maintains the DID record on the blockchain
And provides the user with a verifiable, immutable history for their identity

### Scenario: Verifying a user's identity with blockchain-stored DID
**Given** a verifier needs to confirm a user's identity for a transaction
**When** they request access to the user’s DID record
**Then** the Blockchain DID Registrar facilitates the verification through the distributed ledger
Providing an immutable proof of the user’s identity for the transaction

### Scenario: Accessing blockchain-based DIDs via APIs
**Given** an external system requires cross-referencing for user identities
**When** it calls the APIs provided by the Blockchain DID Registrar
**Then** it retrieves the necessary DID records from the blockchain
And successfully cross-references the DIDs with the internal user data

### Scenario: Updating a DID record upon user's request
**Given** a user has undergone a significant change affecting their identity verification
**When** they submit a request to update their DID record
**Then** the Blockchain DID Registrar ensures the change is recorded on the blockchain
Maintaining the continuity and integrity of the user’s identity record

### Scenario: Auditing the use of DIDs for regulatory compliance
**Given** regulatory authorities require an audit trail for identity use in transactions
**When** they conduct an audit
**Then** the Blockchain DID Registrar provides an immutable log of all DID transactions on the blockchain
Assisting the authorities in their regulatory compliance checks