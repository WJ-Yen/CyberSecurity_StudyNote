# CyberSecuity

## 1.1 Sec. Controls
### Control categories
1. Technical Control
    - Implemented using systems
    - OS contrtol
    - Firewwalls, anti-virus...
2. Managerial Control
    - Security designs and implementation
    - Security polices, standard operating procedures...
3. Operational Control
    - Controls implemented by people
    - Security guards, awareness programs...
4. Physical Control
    - Physical access limitation
    - Guard, fences, locks, badge readers...

### Control types
#### Preventive
- Prevent access
- Block access to a resource
- Control Cat.
    1. Technical: Firewall
    2. Managerial: On-boarding policy
    3. Operational: Guard shack
    4. Physical: Door lock
#### Deterrent
- Discourage intrusion attempts, make attacker think twice
- **Not directly prevent access**
- Control Cat.
    1. Technical: Splash screen
    2. Managerial: Demotion
    3. Operational: Reception desk 
    4. Physical: Waring signs
#### Detective
- Identify intrusion attempts
- Find the issue
- Control Cat.
    1. Technical: System logs
    2. Managerial: Review login reports
    3. Operational: Property patrols 
    4. Physical: Motion detectors
#### Corrective
- Apply control after an event has been detected
- Reverse the impact
- Continue operating with minimal downtime
- Correct the problem
- Control Cat.
    1. Technical: Backup recovery
    2. Managerial: Policies for reporting issues
    3. Operational: Contact authorities 
    4. Physical: Fire extinguisher
#### Compensating
- Control using other means
- Existing controls aren't sufficient
- May be temporary
- **Prevent the exploitation of a weakness**
- Control Cat.
    1. Technical: Block application
    2. Managerial: Separation of duties
    3. Operational: Require multiple sec. staff 
    4. Physical: Power generator
#### Directive
- direct subjects towards security compliance
- **Realtively weak control**
- "Do this, please"
- Control Cat.
    1. Technical: File storage policies
    2. Managerial: Compliance polices
    3. Operational: Security policy training
    4. Physical: Sign--Authorized Only

## 1.2 CIA Triad
- Combination of principles
1. Confidentiality
    - Prevent disclosure of information to unauthorized individuals or systems
    - Encryption. Access controls. Two-factor authorization.
2. Intergity
    - Messages can't be modified without detection
    - **Store and transfer as intended**
    - Hashing. Digital signatures. Certificates. Non-repudiation.
3. Availability
    - Systems and networks must be up and running
    - **accessible to authorized users**
    - Redundancy. Fault tolerance. Patching.

### Non-repudiation
- No taking back
- Proof of origin, Proof of integrity

#### Proof of integrity
- Verify data does not change
- Data remains accurate and consistent
- Hashing

#### Proof of origin
- Prove the message was not changed
- Prove the source
- Make sure the signature isn't fake
- private key signature

### AAA framework
1. Identification
    - Username
2. Authentication
    - Password
3. Authorization
    - Access
4. Accounting
    - Login time, data sent/received, logout time...

#### Certificate authentication
- Certificate Authority (CA)
    - A signature on the machine

#### Authorization models
1. No authorization model
    - Simple relationship
    - Issues
        - Difficult to understand why authorization may exist
        - Does not scale
2. Authorization model
    - Abstraction
    - Administration is streamlined

### Gap analysis
- where you are vs. where you want to be
#### Framework
- NIST 800-171 Rev.2
- ISO/IEC 27001
#### Evaluate
1. Compare existing systems
2. Identify weakness
3. Detailed analysis
4. Final report
    - Path to get from current security to the goal
        - Time, money, changes...
        - Formal description of current state
        - Recommendations

### Zero Trust
- Problem: many networks are open on the inside
- Zero trust: holistic approach to network security
    - Every divice, every process, every person
- "Everything must be verified"
    - **Nothing** is inherently trusted
    - Multi-factor authentication, encryption, system permissions, additional firewalls...
#### Planes of operation
1. Data plane
    - Process the frame, packets and network data
    - Processing, forwarding, trunking, encrypting...
2. Control Plane
    - Manages the action of data plane
    - Policy and rule
    - Routing tables, session tables, NAT tables...
#### Controlling trust
1. Adaptive identity
    - Consider user and requested resources
    - Risk factors, relationship to the organization, physical location, IP adress...
2. Threat scope redution
    - Decrease the number of possible entry points
3. Policy-driven access control
    - Apply different rules to adaptive identity

#### Security zones
- Where you from and where you are going

#### Policy enforcement point (PEP)
- Gatekeeper from subject/system to resources
- Allow, monitor, and terminate connections

#### Policy Decision Point (PDP)
- Making authentication decision
- Policy engine: Evaluates access decision based on policy and other information sources
    - Grant, deny, or revoke
- Policy Administrator: Communicates with PEP, generates access tokens or credentials

### Physical Security
#### Access control vestibules
- All doors normally unlocked -> opening one door causes others to lock
- All doors normally locked -> unlock one prevent others from unlock
- One door open other locked -> one open the other can't be unlocked
- Managed control through area
#### fences
- Transparent or opaque
- Robust
- Prevent climbing
#### Video surveillance
- CCTV
#### Guards and access badges
#### Lighting
- More light, more security
- Work with CCTV
#### Sensors
- Infrared
- Pressure
- Microwave
- Ultrasonic

### Deception and Disruption
#### Honeypots
- Attract bad guys and trap them
#### Honeynets
- Real network includes more than one devices
#### Honeyfiles
- Fake information files
- password.txt etc.
#### Honeytokens
- Track malicious actors
- API credentials
    - No access but sent notifications when used
- Fake email address

## 1.3 Change Management
- How to make change
    - Upgrade software, patch application...
- Most common risks, often overlooked
- Clear policies
    - Frequency, duation, process...
- Difficult to implement sometime

### Change approval process
- Formal process for changes
- Typical approval process:
    1. Complete request forms
    2. Determine purpose
    3. Identify scope
    4. Determine impact and affected systems
    5. Analyze the risk associated
    6. Get approval
    7. Get end-user acceptance
#### Roles
- Owner
- Stakeholders

#### Impact analysis
- Determine risk value
- The fix doesn't work, breaks something else, OS failures...
- Compare to **the risk WITHOUT change**
    - Security vulnerability
    - Application unavailability
    - Unexpected downtime
#### Testing environment
- Sandbox
- Use before making changes
- Confirm backout plan

#### Blackout plan
- Always have a way to revert

#### Maintenance windows
- When to update? Consider the downtime etc.

#### Standard operating procedure
- Change management is critical
- Must be documented

### Technical changes management
- Execute the plan
- "How" to change it
#### Allow list/ deny list
- Application can be dangerous
- Allow list: Nothing runs unless it's approved
    - Very restrictive
- Deny list: Nothing on the list can be executed
#### Restricted activities
- Scope of changes
- May be expanded during change windows
#### Downtime
- Prevent any downtime
    - Switch to secondary system...
- Minimize downtime
    - Automated
    - Switch back if issues appear
    - Part of the backout plan
- Notify everyone
#### Restarts
- OS, switches, services, applications...
#### Legacy applications
- No longer supported
- Fear of the unknown
    - Face your fear and document the system
#### Dependencies
- Service A needs Service B installed
#### Documentation
- Keep up with changes
- Updating diagrams (network configurations, address...)
- Updating policies/ procedures
#### Version control
- Track changes

### Public Key Infrastructure
- Policies, procedures, hardware, software, people
- CA

#### Symmetric encryption
- Single, shared key
    - En-/Decrypt with same key
- Doesn't scale
- Fast to use

#### Asymmetric encryption
- Public key cryptography
- Public key and Private key

#### Key pair
- Key generation
    - Build both public and private key at the same time
    - Randomization
    - Large Prime numbers
    - Lots of math
- Everyone have public key

#### Key escrow
- Someone else have the private key
    - 3rd party, organization...
- Can be legitimate but controversial

### Encrypting data
- Protect data, disk, files
#### Database encryption
- Transparent encryption: encrypting with symmetric key
- Record-level encryption: different keys for different column
#### Transport encryption
- Protect data traversing
- HTTPS, VPN...
#### Encryption algorithms
- Different ways to encryption
- Decide by both side
- Consider security level, speed, implementation...
- Keys determine value
#### Key length
- Larger keys tends to be more secure
- Symmetric: 128-bits or larger are common
- Asymmetric: 3072-bits or larger are common

#### Key stretching
- Make weak keys stronger by multiple processes

### Key exchange
#### Real-time encryption
- Share a symmetric session key using asymmetric encryption
- Session key: Client encrypts key with server's public key
- Need to be change often and unpredictable

#### Symmetric key from asymmetric keys
- Sender's private key + Receiver's public key

### Encryption Technologies
#### Trusted Platform Module (TPM)
- A specification for cryptographic functions
- Cryptographic processor
#### Hardware Security Modulen (HSM)
- Using in large enviornments
- Plug in card or separate hardware devices
- Key Backup
- Accelerators

#### Key management system
- Managed keys from a centralized manager
- Create keys, rotate keys...

#### Keeping data private
- Constanst race with attacker

#### Secure enclave
- Protected area for secrets
- Isolated from main processor
- Has own boot ROM
- Monitors system boots
- True random number generator
- Real-time memory encryption
- Root cryptographic keys
- Perform AES encryption
- ...

### Obfuscation
- Hide information in plain sight
#### Steganography
- Concealed writing
- Invisible message
- Covertext
#### Common techniques
- Network: Embed in TCP packets
- Use image
- Watermarks
#### Tokenization
- Replace data with placeholder
- Common with credit card Processing
    - Use one time tokens
    - No encryption needed
#### Data masking
- e.g. ********24, the asterisk is masking

### Hashes
- Data -> short string or text
- One-way
- Integrity, Authentication(digital signature)...
#### Collision
- Different input should never create the same hash
- MD5 problem
#### Practical usage
- Verify download files
- Password storage
#### Adding salt
- Random data added to password when hashing
#### Digital signatures
- Prove the source and not changed or fake
- Use private key encryption

### Blockchain
- Distributed ledger
- Everyone maintain the network
#### Process
1. Transaction requested
2. Sent to every node in the network to be verified
3. Adding new block of data containing verified transaction
4. Hash created and added to new block
5. Update all nodes in the network, transaction complete
- If any blocks be altered, the hash will not be the same, and the rest of network reject

### Certificate
- Public key certificate
- Web of trust: trust chain

#### Format
- X.509: standard format
    - Serial number
    - Signature Algorithm
    - Public key
    - ...

#### Root of trust
- How to build trust?
- 3rd party, HSA, Secure enclave, CA...

#### 3rd party CA
- Built in to browser
- Purchase web site certificate
- Additional verification information my be request by CA

#### Certificate signing requests (CSR)
1. Create key pair
2. Send public key to CA (CSR)
3. CA validates request
    - Confirms DNS emails and website ownership
4. CA signs the certificate and return

#### Private certificate authorities
- Build it in house
- Large organization needed
- Same process as external CA

#### Wildcard ceritficates
- Subject Alternatice Name (SAN)
    - Extension to X.509 
    - Support different domains in a certificate
- Wildcard domain: Certificate based on name of the server

#### Key revoaction
- Certificate Revocation List (CRL)
- CVE-2014-0160: Heartbleed. OpenSSL patched and many web server certificate replaced, Older certificate moved to CRL

#### OCSP stapling
- Online Certificate Status Protocol
- Certificate holder verify their own status
- OCSP status is "stapled" into the SSL/TLS handshake

#### Getting revocation to the browser
- Messages sent to an OCSP via HTTP, more efficient than CRL
- Not all browser support OCSP
