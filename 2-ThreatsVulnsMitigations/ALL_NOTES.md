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


### 2.4 - An Overview of Malware
**<u>Malware</u>**
- Malicious software
- Gather information
- Show advertising

**<u>Malware Types</u>**
- Viruses
- Ransomware
- Worms
- Trojan horse Horse
- Key logger

**<u>How do you get Malware?</u>**
- All work togethe
    - Worm takes advantage of vulnerability
    - Installs malware that includes remote acess backdoor
    - Addidtional malware installed later 
- Computer must runa. program

**<u>Data is Valuable</u>**
- Personal data
    - Family pictures and videos
    - Important documents
- Organizational data
    - Planning docs
    - Employee personally

**<u>Ransomware</u>**
- All data is encrypted until money is provided
- Malware encrypts data
    - OS remains available
- Pay attackers to obtain decryption key

**<u>Protocoling Ransomware</u>**
- Always have a backup
    - Offline backup
- Keep OS up to date
- Keep apps up to date
- Anti-virus

### 2.4 - Viruses and Worms
**Virus** --> Malware that can reproduce itself 
- Needs to execute a program
- Reproduces through file systems or network
- may or may not cause problems

**<u>Virus Types</u>**
- Program viruses
    - Part of an app
- Boot sector viruses
- Macro viruses

**<u>Fileless Virus</u>**
- Stealth attack
    - Avoids virs detection
- Operate in memory


**<u>Worms</u>**
- Malware that self replicates
- Doesn't need you to do anything
- Uses network as a transmission medium
- FW, IDS, IPS can mitigate worms

#### Summary / Things to Know
Worms and viruses can be highly detrimental to the overall security of a system and should be avoided at all costs.

- Where do these things come from
- What is the difference between a virus and a worm
- how may we identify if a virus or a worm is present


### 2.4 - Spyware and Bloatware
**Spyware** --> malware that spies on you
- Advertising, identity theft, affiliate fraud
- Can trick you into installing
- Browser monitoring
- Key loggers
    - Capture every keystroke

**Bloatware** --> Uses valuable storage space and adds to overall resource usage
- new computer or phone
- OS or other important apps

**<u>Protecting against Spyware</u>**
- Maintain anti-virus / anti-malware
    - Always have latest signatures
- Always know what you are installing
    - Watch options during installation
- Wheres the backup??
    - Might need it someday
- Run scans
    - Malware bytes

**<u>Removing Bloatware</u>**
- Identify and remove
- use built in uninstaller
- 3rd party uninstallers and cleaners as well

### 2.4 - Other Malware Types
**<u>Keyloggers</u>**
- Keystrokes can contain valuable information
    - Web-site logins, passwords, email messages
- Save all input
    - Send it to the bad guys
- Circumvents encryption protections
- Other data logging

**<u>Logic Bomb</u>**
- Wait for pre-defined event
- Time bomb
- user event
- Difficult to identify

**<u>Preventing logic bomb</u>**
- Difficult to recognize
- Processes and procedures
- Electronic monitoring
- Constant auditing

**<u>Rootkits</u>**
- Originally a unix technique
- Modifies core system files
- can be invisible to the OS

**<u>Finding and Removing Rootkits</u>**
- Look for unusual
- use a remover specific to rootkit
- Secure boot with UEFI


### 2.4 - Physical Attacks
- Old school security
    - No keyboard, no mouse, no command line
- Many diff ways to curcumvent digital security

**<u>Brute-Force</u>**
- Physical version

**<u>RFID Cloners</u>**
- Duplication is easy accessible and quick
- This is why we use MFA

**<u>Envirnment Attack</u>**
- Attack everything supporting tech
- Power monitoring
- HVAC at data centers
- Fire suppresion systems


### 2.4 - Denial of Service
- Force a system to fail
- Take advantage of design failure or vulnerability
- Overload the service
- Cause system to be unavailable

**<u>Friendly DoS</u>**
- Unintention DoSing
- Network DoS
- Layer 2 loop with STP
- Bandwidth DoS

**<u>Distributed Denial of Service</u>**
- Launch an army of computers to bring down a service
- Asymmetric threat
- Reflection and amplification
- Turn small attack into a big one
- increasingly common DDoS technique
- usses protocols with little if any authentication or checks
    - NTP, DNS, ICMP

### 2.4 - DNS Attacks
**<u>DNS Poisoning</u>**
- Modify the DNS server
    - Requires crafty hacking
- Modify the client host file
    - Host file takes precedent over DNS queries
- Send fake response to a valid DNS request

**<u>Domain Hijacking</u>**
- Get access to domain refistration and you have control where traffic flows
- Don't need to touch actual servers
- Determines DNS names and DNS IP addresses
- Many ways to get access into the account

**<u>URL hijacking</u>**
- Make money from your mistakes
- Sell badly specified domain and owner
- Redirect to a competitor

**<u>Types of URL Hijacking</u>**
- Typosquatting / brandjacking
    - take advantage of poor spelling
    - Outright misspelling
    - Different top-level domain

### 2.4 - Wireless Attacks
Wireless attacks can take many forms, a lot of them come up as a **wireless deauthentication attack** or a **wireless denial of service attack**.

**<u>802.11 Management Frames</u>**
- 802.11 wireless includes a number of management features
    - Frames that make everything work
- Important for the operation of 802.11 wireless
    - Find access points, manage QoS associate / dissasociate with access point etc.
- Original wireless standards did not add protection for management frames
    - Sent in the clear, no authentication or validation

**<u>Protecting against Deauthentication<u>**
- IEEE already addressed
- Important management frames are encrypted
- not everything is ecncrypted

**<u>Radio Frequency (RF) jamming</u>**
- DoS
- transmit interfering wireless signals
    - Decrease signal to noise ratio at receiving device
    - receiving device cant hear good signal
- Somtimes unintentional
    - Interference not jamming
- jamming is intentional

**<u>Wireless Jamming</u>**
- Constant, random bit / constant, legitamete frames
- Data sent at random times
- Reactive jamming
- needs to be somewhere close
- time to go fox hunting

#### Summary / Things to Know
Wireless attacks are varied but normally show up as deauthentication attacks or DoS attacks

- What are management frames
- What was the old standard and how was it exploited
- What is the difference between interference and jamming, why may it be bad for an organization


### 2.4 - On-path Attacks
- How can an attack watch without you knowing?
    - Formerly known as man in the middle attakcks
- Redirects traffic
    - passes it to destination
    - never know traffic is re-directed
- ARP poisoning
    - On-path attack on local IP subnet (good example in professor Messer's video on this)

**<u>On-path Browser Attack</u>**
- what if middle man was on same computer as victim
    - malware / trojan horse does all the proxy work
    - Formerly know as man-in-browser
- Huge advantages for attackers
    - Relatively easy to proxy encrypted traffic
    - Everything looks normal to victim


### 2.4 - Replay Attacks
- Useful information is transmitted over the network
    - Crafty hacker will take advantage of this
- Need access to raw network data
    - network tap, ARP poisoning
    - malware on victim computer
- Replay data to appear as someone else
- NOT an on-path attack
    - Actual replay does not require original workstation
    - Sometimes attackers will run an on-path then a replay
- Avoid passing hashes by adding salt

**<u>Browser Cookies and Session IPs</u>**
- Encrypt end-to-end
- Encrypt end-to-end somewhere (VPN concentrator)

**<u>Header Manipulation</u>**
- Information gathering
    - Wireshark, kizmet
- Explots
    - Cross-site Scrpting
- Modify headers
    - tamper, scapy etc.
- Modify cookies
    - Cookies manager +

### 2.4 - Malicious Code
**<u> Exploiting a vulnerability</u>**
- Attacker scan use many techniques
    - Social engineering, default credentials, misconfiguration etc.
- Do not require technical skills
    - "The door is already unlocked
- Still ways to get into well-secured system
    - Exploit of malicious code
    - Knock piins out of door hinge

**<u>Malicious Code</u>**
- Attackers use any opportunity
    - Types of malicious code are varied
- Many different forms
- Protection from many different sources
    - Anti-malware
    - Firewall
    - Continuous updates and patches
    - Secure computing habits

**<u>Examples</u>**
- WannaCry ransomware
    - Arbitrary code execution
    - Windows vulnerability
- British airways cross-site scripting
- Estonian Central Health Database

### 2.4 - Application Attacks
**<u>Injection Attacks</u>**
- Code injection
    - Adding own information into data stream
- Enabled because of bad programming
    - Application should properly handle input and output
- SO many different injectable data types

**<u>Buffer Overflows</u>**
- Overwriting a buffer of memory
    - Spills into other memory areas
- Devs need to perform bounds checking

**<u>Priviledge Escalation</u>**
- Gain higher level access to a system
    - Exploit vulnerability
    - Bug or design flaw
- Higher level access means more capability
- High priority vulnerability patches
- Horizontal priviledge escalation
- Use A can access User B resources

**<u>Replay Attacks</u>**
- Useful information is transmitted over network
- Need access to raw network data
- Replay data to server

**<u>Cross-site Requests</u>**
- Cross site requests are common and legitamete
- Visit a website
    - Browser loads text
    - Loads video from YouTube
    - Loads pictures from instagram

**<u>Mitigations</u>**
- Patch quickly
    - Fix vulnerability
- Updated ati-cirus / anti-malware software
- Data execution prevention

**<u>Directory Treaversal</u>**
- Read files from web-server that are outside of website file directory
- Web-server software vulnerability
- Web-app code vulnerability

**<u>client and Server</u>**
- Webpages consist of client side code and server side code
- Many moving parts

**<u>Cross Site Request Forgery</u>**
- One-click session riding
    - XSRF, CSRF 
- Takes advantage of the trust that a web-app has for the user
    - Web-site trusts browser
    - Requests are made without consent or knowledge
    - Attacker posts facebook status on account ( See the example in Professor Messer video )


### 2.4 - Cryptographic Attacks
- Data was encrypted and sent out
    - Is info really secure
    - How do you know?
- Attacker doesn't have combination
    - So they break the safe...
- Find ways to undo the security
    - Problem is often the implementation

**<u>Birthday Attack</u>**
- In classroom of 23 students what is chance of 2 students sharing the same birth month
    - ~50%
- In digital world, hash collision is same hash value for two different plain texts
- Protect yourself with large hash output size

**<u>Collisions</u>**
- Hash digests are supposed to be unique

**<u>Downgrade Attack</u>**
- Instead of using perfectly good encryption use something bad
    - Force systems to downgrade security
- SSL-stripping
    - Combines on-path with downgrade attack


### 2.4 - Password Attacks
**<u>Plaintext / Unencrypted Passwords</u>**
- Some applications store passwords "in the clear"
- No encryption, very rare
- DO NOT STORE PASSWORDS AS PLAINTEXT

**<u>Hashing a Password</u>**
- Hashing represents data a fixed length string of text
- Message digest / fingerprint
- Will not have collision hopefully
- Cannot be reverse engineered

**<u>Spraying Attack</u>**
- Attack an account with most used passwords
- If it doesn't work, move to the next account

**<u>Brute Force</u>**
- Try all possible combinations until hash is matched
- Might take some time

### 2.4 - Indicators of Compromise
**IoC** = An event that indicates an intrusion
- Confidence is high
- Calling from inside the house
Indicators:
- Unusual amount of network traffic
- Change to file hash values
- Irregular international traffic
- Changes to DNS data
- Uncommon login patterns
- Spikes of read requests to certain files
    - And many more...

**<u>Published / Documented</u>**
- Company data published online
- Entire attack goes unnoticed
    - Raw data released without context

**<u>Account Lockout</u>**
- Credentials are not working
    - It wasnt you though
- Exceeded login attempts
- Account was administratively disabled
- may be part of a larger plan
- Attacker locks account 
- Calls support line to reset password

**<u>Concurrent Session Usage</u>**
- Multiple account logins from multiple locations
- Can be difficult to track down

**<u>Blocked Content</u>**
- Attacker wants to stay as long as possible
- System unlocked, keep it open
- Security patch available? Keep away
- Blocked content
    - Auto-update connections
    - Links to security patches
    - Third party anti-malware sites
    - Removal tools

**<u>Resource Consumption</u>**
- Every attackers action has equal and opposite reaction
    - Watch carefully for significant changes
- File transfers use bandwidth
    - ex: Unusual spike at 3AM
- Firewall logs show outgoing transfer
    - Ip addresses, timeframes
- Often first real notification of an issue
    - Attacker may have been here for months

**<u>Resource Inaccessibility</u>**
- Server is down and not responding
- network disruption
- Server outage
- Encrypted data
    - Potential ransomware attack begins
- brute force attacks
    - Locks account access

**<u>Out-of-cycle logging</u>**
- Occurs at unexpected time
- OS patch logs
    - Occuring outside of normal patch day
- Firewall log activity
    - Timestamps of every traffic flow
    - protocols and applications used

**<u>Missing Logs</u>**
- Attackers will try to cover tracks by deleting logs
- logs should be secured and documented





##
