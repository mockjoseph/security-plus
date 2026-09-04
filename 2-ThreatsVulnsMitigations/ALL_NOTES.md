# 2.0 - Threats, Vulnerabilities, Mitigations

### Table of Contents

### 2.1 - Threat Actors
**Threat Actor**: Entity responsible for an event that has an impact on the safety of another entity. Sometimes also referred to as a malicious actor. Important to gather information and categorize them to structure how to handle them.

**<u>Attributes</u>**
- Internal / External
- Resources / funding
- Level of sophistication / capability

**<u>Motivations</u>**
- Data exfiltrations
- Espionage, service disruption
- Blackmail - Financial gain
- Philisophical / Political beliefs
- Eithical
- Revenge
- Disruption or chaos, war

**<u>Nation States</u>**
- External entitiy
    - government and national security
- Many motivations
- Constant attacks, massive resources
- Highest sophistication
    - Stuxnet worm
        > "Stuxnet is a malicious computer worm first uncovered on 17 June 2010[2] and thought to have been in development since at least 2005. Stuxnet targets supervisory control and data acquisition (SCADA) systems and is believed to be responsible for causing substantial damage to the Iran nuclear program after it was first installed on a computer at the Natanz Nuclear Facility in 2009" (Wikipedia)

**<u>Unskilled Attackers</u>**
- Runs pre made scripts without knowing what is happening
- Can be internal or external
- Motivated by the hunt

**<u>Hacktivists</u>**
- hacker with a purpose
- Often an external party
- usually remarkable sophisticated
- funding may be limited

**<u>Insider Threat</u>**
- Extensive Resources
- Internal entity
- Medium sophistaction but usually deep understanding of where to attack

**<u>Organized Crime</u>**
- Professional criminals
    - Usually motivated by money
- Very sophisticated
- Can be structured like an organization

**<u>Shadoiw IT</u>**
- Building own infrastructure
- Limited resources
- Going rogue

#### Sumamry / Things To Know
There are a vast number of threat actors that we need to consider when building out Security Architecture and taking into account different threats and vulnerabilities. When considering what different threat actors that we may be dealing with, we also need to consider what qualities that they may possess.

- What motivates different threat actos
- What different systems or vulnerabilities may different threat actors target
- How can we use this knowledge to protect against different threat actors


### 2.2 - Common Threat Vectors
**Threat Vector** --> Method used by attacker to get access to or target

**<u>Message Based Vector</u>**
- Biggest and most successful
- Email through clickable links
- SMS (text message based attacks)
- Phishing Attacks
- Deliver malware
- Social Engineering attacks

**<u>Image basd Vectors</u>**
- More difficult to identify
- SVG format (mathematical image representation)
- Signigicant Security concerns
- XSS attacks and XMC embedding
- XMC embedding

**<u>File based vecots</u>**
- More than just executables
- Adobe PDF
- ZIP, RAR, other compression types
- Microsoft Office
    - docs with macros

**<u>Voice Call Vectors</u>**
- Vishing
- Spam over IP
- War dialing
- Call tampering

**<u>Removable Device Vectors</u>**
- Get around firewall
    - USB interface
- Malicious software on USB or flash drives
- USB can act as a keyboard
- Data exfiltration

**<u>Vulnerable Software Vectors</u>**
- Client based
    - Infected executable
    - Known or unknown vulnerabilities
    - May require constant updates
- Agentless
    - No installed executable
    - Compromised software on server can affect all clients

**<u>Unsupported System Vectors</u>**
- Patching important prevention tool
    - Unsupported systems aren't patched
- Outdated OS
- Singe system could be an entry

**<u>Unsecure Network Vectors</u>**
- Network connects everything
    - Ease of access for attackers
- Wireless
    - Outdated security protocols (WSP, WDA, WPA2)
    - Open or rogue wireless networds
- Wired
    - Unsecure interfaces. No 802.1x
- Bluetooth
    - Recon, implementation vulnerabilities

**<u>Supply Chain Vulnerabilities</u>**
- Tamper with underlying infrastructure
- Manages service provider (MSP)
    - 2013 Target credit card breach

#### Summary / Things To Know
This section goes into all of the common threat vectors, it should be noted that there are a lot more threat vector that threat actors can take advantage of, but securing these vectors will lead to a good security posture and should be an ongoing assessment in an organization

- Know each of the vector types
- Gain an understanding of where in the organization the vectors can be taken advantage of, what are some examples of weaknesses at each of these vectors and how threat actors may take advantage of that.


### 2.2 - Phishing
**Phishing** --> Social Engineering with a touch of spoofing. Can be remarkable when done well

**<u>Business Email Compromise</u>**
- Trust email sources?
- Supported email addresses
    - Not really a legitamete email address
- Financial fraud
    - Send emails with updated bank info

**<u>Tricks and misdirection</u>**
- digital sleight of hand
- Typosquatiing
    - URL hijacking
- Pretexting
    - Lying to get info

**<u>Phishing with different bait</u>**
- Vishing (Voice phising)
- SMS phishing (smishing)
- Variations on a theme



### 2.2. - Impersonation
**Impersonation** --> Attackers pretending to be somebody that they are not


**<u>Pretext</u>**
- Before attack, trap is set
    - Actor and a story

**<u>Identity Fraud</u>**
- Identity can be used by others
- Credit card fraud
- bank fraud
- Loan fraud
- government benefits fraud

**<u>Protect against Impoersonation</u>**
- never volunteer info
- Don't disclose personal details
- Verify before revealing info



### 2.2 - Watering Hole Attacks
What if the network was very secure
- Didn't even plug that USB in from the parking lot?
- Attackers can't get in
- Go to someone else and poison to the org gets attacked from there
- Requires research
    - Determine which website victim group uses
    - Infect a third party website
    - Infect all visitors

**<u>Watching Watering hole</u>**
- Defense in depth
    - layered defense
- Firewalls and IPS
- Anti-virus/anti-malware updates

### 2.2 - Other Social Engineering Attacks
**<u>Misinformation / Disinformation</u>**
- Disseminate factually correct infor
    - Create confusion and division
- Influence campaigns
- Nation state actors
- Advertising is an option

**<u>Brand Impersonation</u>**
- Pretend to be a well-known brand
- Create a bunch of impoersonated sites
- Visitors presented with pop-ups
- Malware infection generated

### 2.3 - Buffer Overflows
**Buffer Overflow** --> A more technical memory attack that overwrites a buffer of memory. Spills into other memory areas, devs need to perform bounds checking. Not a simple exploit, but can be dangerous as buffer overflow is repeatable.

### 2.3 - Race Conditions
**Race Conditions** --> Programming conundrum where things happen at the same time and can be bad if not planned for. Time of check to time of use attack (TOCTOU). Something might happen between the time of check of a system and the time of use of a system.

### 2.3 - Malicious Updates
