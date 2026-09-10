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
**<u>Software Updates</u>**
- Always keep OS and applications updated
    - Both bug fixes and security patches
- Process has its own security concerns
    - Not every update is equally secure
- Follow best practices
    - Always have a good known backup
    - Installl from trusted sources

**<u>Downloading and Updating</u>**
- Install updates from downloaded files
    - Always consider actions
    - Every installation could be dangerous
- Confirm source
- Visit developers site directly
- Many OS will only allow signed apps
    - Don't disable security controls

**<u>Automatic Updates</u>**
- The app updates itself
    - Often includes security checks (digital signatures and such)
- Relatively trustworthy

#### Summary / Things To Know
Updates and patches are somehthings that should be a standard practice when upholding a good security posture. We still need to consider the implications of doing these updates however

- Updates can be malicious
- What do we need to consider when going through an update or patch process
- What are the best practices of doing these things

### 2.3 - Operating Systems Vulnerabilites
**<u>Overview</u>**
- Foundationsal computing platform
    - Everyone has one
    - Makes OS a big target
- Remarkably complex
    - Millions of lines o code
    - More code = More opportunity for attacks

**<u>Month of OS updates</u>**
- Patch Tuesday
- Other ocmpanies often have similar schedules

**<u>Best Practices</u>**
- Always updates
    - Monthly or on-demand updates
    - Race between you and the attackers
- May require testing beore deployment
- May require a reboot
    - Save all data
- Have a fallback plan
    - Where is the backup


### 2 - 3 Code Injection
**Code Injection** --> Adding own information into data stream
- Enabled because of bad programming
- A lot of different types

**<u>SQL Injection</u>**
- Put own SQL requests into an existing application
- Applicatin shouldn't allow this
- Can often be executed in aweb browser
- Inject into a form or field


### 2.3 - Cross-Site Scripting (XSS)
- Not like Cascading Style Sheets (CSS)
- Originally called cross-site because of browser security flaws
    - Information from one site can be shared with another
- One of the most common web-app vulnerabillities
    - Takes advantage of the trusst a user has for a site
- Complex and varied
- XSS commonly uses JavaScript

**<u>Non-persistent (reflected) XSS attacks</u>**
- Website allows scripts to run in user input
    - Search box is a common source
- Attacker emails a link that takes advantage of this vulnerability
    - runs a script that sends credentials / session ID / cookies to attacker
- Script embedded in URL executed in victims browser
- Attacker uses credds / session IDs / cookies to steal information form victims without their knowledge

**<u>Persistent (stored) XSS attacks</u>**
- Be careful when clicking untrusted lilnks
- Disable JS?
- Keep browsers updated

**<u>Hacking a Subaru</u>**
- When authenticating with Subaru user gets a token
    - Token never expires (bad)
- Valid token allowed any service request
    - Even adding email address to someone elses account
    - Now you have full access to someone elses car

#### Summary / Things To Know
Cross-Site scripting is a widely used attack that is fairly involved from a techncial standpoint. It can be varied and show up in different ways. It is often a code vulnerability, but we can protect against t by only clicking trusted links and constantly keeping browsers and systems up to date


### 2.3 - hardware Vulnerabilites
Many devices do not have accessible operating systems
- Devices are potential security issues
- Everything is connecting to the network
- Security landscape has grown

**<u>Firmware</u>**
- Software inside of hardware
    - OS of hardware device
- Vendors are only ones who can fix hardware

**<u>End of Life</u>**
- Manufacturer stops selling product
    - may continue supporting product
 
End of service life:
- Support is no longer available for the product
- In tech, EOSL is a significant concern

**<u>Legacy Platform</u>**
- Some devices that are installed for a long time
- Older OS, applications, middleware
- Risk compared to return at EL
- Add firewall rules, IPS signatures

### 2.3 - Virtualization Vulnerabilities
**<u>Virtualization Security</u>**
- Different from non-virtual machines
    - Can appear anywhere
- Quantity of resources vary between VMs
    - CPU, memory, storage
- Can be similar to physical machines
    - Complexity adds opportunity for attackers

**<u>VM escape protection</u>**
- VM is self containeed (mostly)
- VM escape
    - Break out of VM and interact with host operating system or hardware
- ONce escaped VM, lots of power

**<u>Resource use</u>**
- Hypervisor manages relationship between physical and virtual resources
- Resources can be reused between VMs
- Data can be inadvertently shared between VMs


### 2.3 - Cloud Specific Vulnerabilites
**<u>Security in the Cloud</u>**
- Putting sensitive data in cloud
- Not putting right protections
- 63% code unpatched
- 76% of orgs don't use MFA

**<u>Attack the Service</u>**
- DoS (denial of service)
- Authentication bypass
    - Take advantage of weak or faulty authentication
- Directory traversal
- Remote code execution

**<u>Attack the Application</u>**
- Web application attacks have increased
    - Easy to exploit rewards are expensive
- Cross-site scripting (XSS)
- Out of bounds write
    - Write to unauthorized memory access

### 2.3 - Supply Chain Vulnerabilities
**Supply chain** --> Entire flow from raw materials to the consumer
- Chain contains many moving parts
- Attackers can attack at any point in the chain
- One exploit can affect entrie chain

**<u>Secure Providers</u>**
- Can control own security posture
    - Can't always control service provider
- Often have access to internal services
    - Opportunity for attacker
- many different types of providers
- consider ongoing security audits of all providers

**<u>Hardware Providers</u>**
- Can you trust new server / routing / switch / fw / sw
- strict controls over policies and procedures

**<u>Cisco or not Cisco?</u>**
- All network traffic flows through switches or routers

**<u>Software Providers</u>**
- Trust is a foundation of security
- Initial installation
- Updates and patches


### 2.3 - Misconfiguration Vulnerabilities
**<u>Open permissions</u>**
- Very easy to leave a door open
- hackers will always find it
- Increasingly common with cloud storage

**<u>Unsecured Admin Accounts</u>**
- Linuzx root, win admin
- Can be misconfiguration
- Disable direct login to root account
- protect accounts with root or admin access

**<u>Insecure Protocols</u>**
- Some protocol aren't encrypted
    - Telnet, FTP, SMTP, IMAP
- Verify with packet capture
- Use encrypted versions

**<u>Default Settings</u>**
- Every app, and network device has a default login
- Mirai botnet
    - Takes advantage of default ocnfig
    - Open-source

**<u>Open ports and services</u>**
- Services with open ports
- Often managed witha. firewall
- Firewall rulesets can be complex
- Always test and audit

### 2.3 - Mobile Device Vulnerabilities
Mobile devices can be very challenging to secure and they need additional security policies and systems
- Relatively small almost invisible
- Almost always in motion
- Packed with sensitive data

**<u>Jailbreaking / Rooting</u>**
- Purpose built systems
    - Don't have access to the OS
Android = Rooting
Apple iOS = Jailbreaking
- Replaces existing OS
- Untrusted aaccess

**<u>Sideloading</u>**
- Malicious appcs can be significant security concern
- Manage instlalation sources
- Sideloading cicurcumvents security 
    - Apps can be installed manually


### 2.3 - Zero Day Vulnerabilities
- Many applications have vulnerabilities
- Just haven't found them yet
- People always working to find vulnerabilities

**<u>Zero Day Attacks</u>**
- Attackers search for unknown vulnerabilities
- Vendor has no idea it exists
- Zero-day attacks
    - Attack without a patch or method of mitigations

    
