# CH2: Threats, Vulnerabilities, and Mitigations
## 2.1 Threat Actors
### Threat Actors
- Malicious actor
- Responsible for the attack
- Useful to categorize the motivation
#### Attributes
- Internal/ external
- Resource/ funding
- Level of sophistication/ capability
#### Motivations
- Data exfiltration
- Espionage
- Financial gain
- Polical beliefs
- ...
#### Nation states
- External entity
- Massive resources and constant attacks
    - Advanced Persistent Threat (APT)
- Highest sophistication
- War, data exfiltration...
#### Unskilled attackers
- Run pre-made scripts
- Internal or External (usually external)
- No formal funding
- Not sophisticated
- Disruption, data exfiltration...
#### Hacktivist
- Hacker with a purpose: philosophy, revenge...
- Often external
- Can be sophisticated
- Limited funding
#### Insider Threat
- Internal
- Medium level sophistication
- Extensive resources
    - Using organization's resources against themselves
- Revenge, finacial gain...
#### Organized crime
- Professional criminals
- External
- Very sophisticated
- Lots of capital to fund hacking efforts
- Financial mainly
#### Shadow IT
- Working around the internal IT organization
- Internal
- Medium sophisticated
- Limited to many resources
## 2.2 Threat Vectors and Attack Surfaces
### Threat vectors
- Attack vectors
- A method used by the attacker to gain access/ infect
#### Message-based vectors
- Biggest threat vectors
- In email, SMS...
- Malicious links to malicious site
- Phishing attacks
- Deliver malware
- Social engineering
#### Image-based vectors
- Difficult to identify than text
- SVG, XML format can be threat
- HTML injection, Javascript attack code
- Browser provide input validation to avoid malicious code
#### File-based vectors
- PDF, ZIP, Office...
#### Voice call vectors
- Vishing (Phising over phone)
- Spam over IP 
- War dialing
- Call tampering
#### Removable device vectors
- USB interface
- Get around the firewall
- Data exfiltration...
#### Vulnerable software vectors
- Client-based
    - Infected executable
    - May require constant updates
- Agentless
    - No installed
    - Compromised software on the server to affect all users
    - Client run new instance
#### Unsupported systems vectors
- Patching prevent security problem
- Unsupported systems aren't patch 
- Single system could be an entry
#### Unsecure network vectors
- Ease of access for attackers
- View all non-encrypted data
- Outdated wireless protocols (WEP, WPA, WPA2)
- Unsecure interface (No 802.1X)
- Bluetooth reconnaissance or implementation vulnerabilities
#### Open service ports
- Every port is an opportunity
- More services, more port needed
- Firewall rules to control traffic
#### Default Credentials
- Default usernames and passwords
- Right credentials provide full control
#### Supply chain vectors
- Tamper the underlying infrastructure
- Managed service providers (MSPs)
- Gain access to network using a vendor
- Counterfeit networking equipment
- Install backdoors, substandard performance and availability

### Phishing
- Social engineering with touch of spoofing
- Check URL
- People trust email sources
- Finacial fruad
- Typosquatting, pretexting
#### Vishing
- Voice phishing
#### Smishing
- SMS phishing

### Impersonation
- Pretend to be someone
- Extracting information
- Psycological techniques
#### Identity fraud
- Credit card fraud
- Bank fraud
- Loan fraud
- Government benefit
#### Protect against impersonation
1. Never volunteer information
2. Don't disclose personal details
3. Verify before giving info

### Watering Hole Attack
- "Attacker poisoned the water hole waiting for you to visit"
- Need research: third-party sites etc.
#### Defense-in-depth
- Layered defense
- Firewalls, IPS: Stop network traffic
- Anti-virus, Anti-malware: Block malicious software

### Misinformation
- Create confusion and division
- Political and social issues
- Through social media

#### Process of misinformation
1. Fake users
2. Create content
3. Post on social media
4. Amplify message
5. Real users share
6. Mass media picks up the story

#### Brand Impersonation
- Pretend to be well-known brand: Google, Facebook, etc.

### Memory Injection
#### Finding malware
- Malware runs in memory
- DLLs, Threads, Buffers...
#### Memory injection
- Add code to memory of an existing process
- Get access to the data in the process
#### DLL injection
- Inject a path to a malicious DLL
- Get process reference the DLL

### Buffer Overflow
- Overwriting a buffer of memory
- Not simple exploit
- Useful buffer overflow is repeatable

### Race Condition
- Process happen at the same time
- Time-of-check to time-of-use attack (TOCTOU)
    - Use before you check

### Malicious Updates
- Some update is not secure
- Best practices
    - Always backup
    - Install from trusted sources
- Confirm the source
- Automatic updates
    - Relatively trustworthy
    - Supply chain attack: attack developer first

## 2.3 Types of Vulnerabilities
### OS Vulnerabilities


## 2.4 Indicators of Malicious Activity



## 2.5 Mitigation Techniques
