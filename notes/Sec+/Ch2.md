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
- Foundational computing platform
- Complex
- Some not found vulnerabilities
#### OS update
- Windows: Patch Tuesday, 2nd Tuesday each month
#### Best practices
- Always update
- May require testing, reboot
- Fallback plan!

### SQL Injection
- Structured Query Language
- SQLi: SQL injection
- Often in a web server
- "sth ' or "1'='1"

### Cross-site scripting
- XSS
- A malicious script that execute in browser secretly to send data to attacker
#### Non-persistent/Reflected XSS attack
- Add script after website input bar
#### Persistent/Store XSS attack
- Post a meesage to a social network
- Everyone gets the payload, no specific target
- Can spread quickly
#### Protecting against XSS
- Don't click untrust links 
- Consider disabling Javascript
- Keep browser update
- Validate input
### Hardware Vulnerabilities
- Many do not have operating system
- IoT devices
#### Firmware
- Software inside hardware
- Vendors are the only ones who can fix hardware
#### End-of-life (EOL)
- Manufacturer stop selling product
- End of service life (EOSL)
    - Stop selling and supporting 
- EOSL is significant concern
#### Legacy platform
- Some devices remain installed for a long time
- Require additional security protection
    - Firewall rules, IPS signatures...
### Virtualization Security
- Appear anywhere
- Resources vary
- Complex-er than normal machine
#### VM escape protection
- Break out of the  VM and interact with the host
- Get control of the other VMs or the host
#### Resource reuse
- Hypervisor manages resources, RAM, storage, CPU...
- Sometime VMs get the datas from other VMs 
- Hypervisor should fix it
### Cloud-specific Vulnerabilities
- Sensitive data
- Not enough protection
#### Attack the service
- Denial of Service (DoS)
- Authentication bypass
    - Allow attacker get data
- Dirctory traversal
- Remote cod execution
#### Attack the application
- Web application attacks
- XSS
- Out of bounds write
- SQL injection
### Supply Chain Vulnerabilities
- Attacks infect some step along the way
#### Service providers
- Consider ongoing security audits
#### Hardware providers
- Use small supplier base
- Strict control over policies and procedures
#### Cisco?
- Switches and routers manufacturer
- Fake Cisco product concern
#### Software providers
- Installation should be signed
- Updates and patch
- Open sources
### Misconfiguration Vulnerabilities
- Open permission
#### Unsecured admin accounts
- Root, superuser
- Easy-to-hack passwords
#### Insecure protocols
- Some protocols aren't encrypted
- Packet capture
#### Default setting
- Mirai botnet: Takes adveantage of default setting
#### Ports
- Manage traffic flows
- Access the machine
### Mobile Device Security
- Small, in motion, sensitive data, constantly connected to net
#### Jailbreaking/rooting
- Gaining access
- Install custom firmware
#### Sideloading
- Malicious apps
- Manage installation sources: App store...
### Zero Day Vulnerabilities
- Many vulnerabilities not found yet
- Attack without patch or method of mitigation
- Common Vulnerabilities and Exposure (CVE)

## 2.4 Indicators of Malicious Activity
### Malware
- Malicious software
- Gather information
- Show advertising
- Viruses and worms
#### Types and methods
- Viruses, Worms, Ransomware, Trojan Horse, Rootkit...
- Control the system
#### Get malware
- Worms take advantage of a vulnerability
- Install remote access backdoors
- Computer must run some program to get malware
- Keep updated OS
#### Why malware
- Data is valuable
- Personal data
- Organization data
#### Ransomware
- Encrypted all the datas
- OS remains available
#### Protecting against Ransomware
- Backup
- Keep everything up to date
- Anti-virus
### Viruses
- Virus: Malware that can reproduce itself through file systems or the network
- May or may not cause problems
- Thousands new viruses every week
#### Virus Types
- Program Viruses: Part of the application
- Boot sector viruses: Activate when boot
- Script viruses: OS and browser-based
- Macro viruses: Microsoft Office
#### Fileless viruses
- Stealth attack
- Inside memory
### Worms
- Malware that self-replicates
- Uses the network ad transmission medium, spreads quickly
- Can take over many systems
- Firewalls and IDS/IPS can mitigate many worms
    - Doesn't help once the worm is inside
- Wannacry worm
### Spyware 
- Malware that spies on you
- Browser monitoring
- Keyloggers
#### Protecting
- Maintain Anti-virus
- Know what you're installing
- Backup
- Run some scans

### Bloatware
- New computer or phone includes applications you didn't expect
- Use storage space
- Manaually Remove
- Some may not have uninstaller
### Other types of Malware
#### Keyloggers
- Keyloggers: Catch the keystrokes inputs
- Passwords, email messages...
- Clipboard logging, screen logging...
#### Logic bomb
- Waits for a predefined event
- Time bomb, User event
- Difficult to identify and recover
- Remove OS or boot device or something
- Check the changes, monitor processes, check permission
#### Rootkits
- Modifies core system files
- Can be invisible to OS, Anti-virus...
- Anti-malware scans, Secure boot with UEFI, rootkit remover
### Physical attacks
- Old-school security
- Physical access to full access
#### Brute force
- Break windows, doors
#### RFID cloning
- Access badges
- RFID duplicators
- Duplicator takes seconds
- Use MFA
#### Environmental attacks
- To shut down everything
- Attack power
- HVAC (Heating, Ventilation, Air Conditioning)
- Humidity controls
- Fire suppression
### Denial of Service
- Force a service to fail, unavailable
#### Unintentional DoSing
- Network DoS: Layer 2 loop without STP
- Bandwidth DoS: Downloading large files
#### Distributed DoS (DDoS)
- Launch many computers to bring down a service
- Botnets
- Asymmetric threat: Attacker may have fewer resources than victim
#### DDoS reflection and amplification
- Turn small attack into big attack
- Uses protocols with little authentication or checks
    - NTP, DNS, ICMP...


## 2.5 Mitigation Techniques
