# 1.0 - General Security Concepts

### Table Of Contents



### 1.1 - Security Controls
**Goal**: Protect assets, minimize risk, deal with breaches etc.
__There are many different types of security controls (data, physical properties, computer systems__)

**Security Contol Domains**
1) Technical Controls
- Controls implemented using systems
- Operating Systems controls
- Firewalls, anti-virus software

2) Managerial Controls
- Administrative controls associated with security design and implementation
- Security plicies, standard operating procedures

3) Operational Controls
- Controls implemented by people instead of systems

4) Physical Controls
- Limit Physical Access
- Fences, locks, badge access

**Control Types**
1) Preventative Control Types
- Block access to a resource
**Technical** --> Firewall
**Managerial** --> On-board policy
**Operational** --> Guard-shack
**Physical** --> Door Locks

2) Deterrent Control Types
- Discourage an intrusion attempt
- Make an attacker think twice
**Technical** --> Splash Screen
**Managerial** --> Demotion
**Operational** --> Reception Desk
**Physical** --> Warning signs

3) Detective Control Types
- Identify and log an intrusion attempt
- Find an issue
**Technical** --> System logs
**Managerial** --> Review Log in reports
**Operational** --> Property patrols
**Physical** --> Motion detectors

4) Corrective Control Tyoes
- Occurs after an event has happened
- Reverse impact
- Continue with minimal operational downtime
- Correct the position
**Technical** --> Recovering backup
**Managerial** --> Policies for reporting issues
**Operational** --> Contact authorities
**Physical** --> Fire extinguisher

5) Compensating Control Types
- Control using other means
- Prevent the expllitation of a weakness
**Technical** --> Block instead of patch
**Managerial** --> Separation of duties
**Operational** --> Require multiple security staff
**Physical** --> Power generator

6) Directive Control Type
- Direct a subject towards security compliance
- Relatively weak security control
**Technical** --> file storage policies
**Managerial** --> compliance policies
**Operational** --> security policy training
**Physical** --> Sign authorized personnel only

#### 1.1 - Summary / Things to Know
- Be able to breakdown different security controls and domains
- Provide examples for each type and domain
- The goal is to implement security across multiple different domains, and be able to categorize security into different types so that we know the depth of our control
- There are 4 main domains, technical, managerial, operational, and physical
- There are 6 main security types: preventative, deterrent, detective, corrective, compensating, and directive


### 1.2 - The CIA Triad
The CIA triad is a concept that we use in security to outline how security posture is upheld and maintained, and it works on the three pillars of security
- **Confidentiality**: Prevent disclosure of information to unauthorized individuals or systems
    - Encryption: Encoding messags so only certain people can see them
    - Access control: Selectively restric access to a resource
    - Two-factor Authentication: Additional confirmation provides more confidentiality
- **Integrity**: Messages can't be modified withough detection
    - Data is stored and transferred as intended
    - hashing: Map data of an arbitrary length to data of a fixed length
    - Digital Signatures: Mathematical scheme to verify integrity of data
    - Certificates: Combine with digital signatures to verify an individual
- **Availability**: Systems and networks must be up and running
    - Information is available to authorized users
    - Redundancy: Build services that are always available
    - Fault Tolerance: System will continue to run, even when a failure occurs
    - Patching: Stability and close security holes
Upholding these 3 pillars is the essential menaing behind upkeeping a good security posture and we should always think in these concepts when implmenting different security controls.

<u>Combination of principles</u>
- The fundamentals of security
- Sometimes referred to as AIC triad

#### Summary / Things to Know
- CIA triad is a philosophy to keep in mind when inplementing security onto a system or designing security objectives
- What does CIA triad stand for
- Why do we use it
- What processes/controls fit under each component of the triad


### 1.2 - Non-Repudiation
Non-Repudiation: You cant deny what you said

<u>Sign a contract</u>
- Signature adds non-repudiation
- You really did sign a contract
- Others can see your signature

<u>Adds a different perspective for **Cryptography**</u>
- Proof of Integrity
- Proof of origin, high assurance of authenticity

<u>Proof of Integrity</u>
- Verify data does not change
- Data remains accurate and consistent
- In cryptography we use a hash
    - Message digest or fingerprint
    - If data changes, hash changes
    - Does not associate with an individual though

<u>Proof of Origin</u>
- Prove the data was not changed (Integrity)
- Prove the source of message (Authentication)
- Make sure the signature isn't fake (Non-repudiation)
- Sign with the private key
    - Message doesn't need to be encrypted
    - Nobody else can sign this
    - Verify with public key

#### Summary / Things to know
- What is non-repudiation
- How is non-repudiation implemented
- What is a hash and why is it useful
- What is a digital signature
- Replicate the hashing lab


### 1.2 - Authentication, Authorization, Accounting

**AAA Framework** (The process of logging in)
- Identification
    - Who you claim to be

**Authentication**
- Proving you are who you say to be
- Password or other auth factors

**Authorization**
- Based on identification and authentication what access do you have

**Accounting**
- Resources used, login time, data send/received, logout time

<u>Authenticating Systems</u>
- How to manage many devices
- System can't type password
- How to authenticate a device?
    - Put digitally signed certificate on device
- Other business processes rely on certificate too
    - Access to VPN
    - Management software can validate the end device

<u>Certificate Authentication</u>
- Organization has a trusted CA (Certificate Authority)
- Organization creates a certificate for a device
    - Digitally signs cert with CA
- Cert is now included on device as an authentication factor

<u>Authorization Models</u>
- user or device now authenticated, what can they access?
- Users and Services --> Data and applications
    - Associating individual users to access rights does not scale well
- Put an authorization model in the middle
    - Define by roles, organizations, attributes, etc.
- Add an abstraction
    - Clear relationship between user and resource
- Administration is streamlined
    - Create groups or roles

#### Summary / Things to know
- Go over the AAA framework, what it is, what its used for.
- based on authentication user needs to be able to access certain resources


### 1.2 - Gap Analysis
**Gap Analysis**: Where are you compared with where you want to be?
- The "gap" between the two
- Verify complex processes to get to or bridge the gap
    - Emails, data gathering, research

**The steps**
1) Choosing a framework
- Work towards a known baseline
    - Internal set of goals
    - Some orgs use formal standards
- Determine end goal
    - NIST special Publication 800-171 Revision 2: Protecting Controlled Unclassified Information in Nonfederal Systems and Organizations
    - ISO/IEC 27001 Information Security Management Systems
2) Evaluate People and Processes
- Get a baseline of employees
    - Formal experience, current training
    - Knowledge of security policies and procedures
- Examine the current processes
    - Research existing IT systems
    - Evalluate existing security policies
3) Compare and Contrast
- Comparison --> Evaluate existing systems
- Identify weaknesses --> Along with most effective processes
- Detailed Analysis --> Examine broad security categories and break into smaller segments
4) Analysis and Report
- The final comparison
    - Detailed baseline objectives
    - Clear view of current state
- Need path to get from current security to the goal
    - Time, money, change control
- Create a Gap Analysis Report
    - Formal description of current state
    - Reccomendation for meething the baseline

#### Summary / Things to Know
- Goes over all aspects of a Gap Analysis
- Understand the steps in conducting a Gap Analysis


### 1.2 - Zero Trust
Many networks are relatively open on the inside and once through there are generally few security controls

Zero trust is a holistic approach to Network Security, every device, every process, every person

Everything must be verified
Nothings is inherently trusted

<u>Controlling Trust</u>
- Adaptive Identity
    - Conside source and requested resources
    - Multiple risk indicators - relationship to org, location, connection etc.
    - Make authentication stronger if needed
- Threat scope reduction
    - Decrease number of possible entry points
- Policy driven access control
    - Combine adaptive identity with pre-defined set of rules

<u>Policy Enforcement Point</u>
- Subjects and systems
    - End-users, applications, non-human entities
- PEP (the bookkeeper)
    - Does not make a decision
    - Policy decision point does that
    - Process for making an authentication decision
- Policy Engine
    - Grants, denies, revokes resources based on policy and other information sources
- Policy Administrator
    - Communicates with Policy Enforcement Point
    - Generates access tokens or credentials
    - Tells PEP to allow access or not

<u>Planes of Operation</u>
- Split Network into functional planes
- **Data Plane**
    - Process frames, packets, network data
    - Processing forwarding, trunking, encryption, NAT
- **Control Plane**
    - manages actions of the data plane
    - Define policies and rules
    - Determines how packes should be forwarded
    - ROuting tables, session tables, NAT tables

<u>Security Zones</u>
- Security is more than a one-to-one relationship
    - broad categorization provides security related foundation
    - Where you are comign from and wehere you are going
        - Trusted Untrused, internal external, VPN 1 5 11, Department of business
- Some zones may be enough to deny access
- Some zones are implizitly trusted


#### Summary / Things to Know
- Zero trust is a policy that we use to ensure that nobody is accessing systems that we shouldnt and keeps things in check at everyb step of the way.
- What are the planes of operation
- What are the ways to enforce zero trst and why is it a big goal in security


### 1.2 - Physical Security
<u>Barricades / Ballards</u>



### 1.2 - Deception and Disruption
<u>Honeypot</u>
- Attract the bad guys
    - Trap them
- Attacker is likely a machine
    - makes interesting recon
- Many open source packages
- Constant battle real vs. fake

<u>Honeynets</u>
- Build larger deception network with more than one hoenypot

<u>Honeyfiles</u>
- Attract attackers with more honey
    - File with fake information
- Alert sent if file is accessd

<u>Honeytokens</u>
- Track malicious actors
    - Add traceable data to honeypot
    - API credentials
    - Fake email addresses
    - Many other examples


### 1.3 Change Management
How to make a change? Upgrade software? Patch an application? Making changes is often one of the most common risks in an enterprise and is often overlooked or ignored need to have clear policies for frequency, install porcess, rollback, and other procedures for handling

**<u>Ownership</u>**
- An individual or entity needs to make a change
    - They own the process
    - Dont perform actual change
- Owner manages process
    - Process updates are provided to the owner
    - Ensures process is followed and acceptable
- Addtess label printer needs to be upgraded
    - Shipping and receiving department owens the process
    - IT handles the actual change

**<u>Change Approval Process</u>**
- Formal process for managing change
    - Avoid downtime, confusion, mistakes
- Typical approval process
    - Complete request forms
    - Determine purpose of change
    - Identify scope of change
    - Schedule a date and time of change
    - Determine affected systems and impact
    - Analyze risk associated with change
    - Get approval from change control board

**<u>Stakeholders</u>**
- Who is impacted by change
    - They'll want to have input on the change management process
- May not be as obvious as you think
    - Simple change can include on individual or entire company
- Upgrade software used for shipping labels
    - Shipping/receiving
    - Accounting
    - Product delivery
    - Revenue recognition

**<u>Test Results</u>**
- Sandbox testing environment
    - No connections to real server or prod system
    - Technological safe space
- use before making prod change

**<u>Maintenance window</u>**
- When is change happening
    - Most difficult part of process
- Overnight or during workday?


#### Summary / Things to Know
- Making changes is often overlooked as people consistently see the benefits in making the change without thinking about the impact
- How do we implement a good change management process
- What are the things that we need to consider when making a change and how to we ensure we are minimizing risk



### 1.3 - Technical Change Management
**Technical Change Management** : Putting the change management process into action
__There is no such thing as a simple upgrade__

**<u>Allow / Deny list</u>**
- Any application can be dangerous
    - Vulnerabilities, Trojan Horse, malware
    - Security policy can control app execution
- Allo List: Nothing can be run unless approved
    - Very restrictive
- Deny List: Nothing on bad list can be executed
    - Anti-virus, anti-malware

**<u>Restricted Activities</u>**
- Scope of a change is important
    - Defines exactly which components are covered
- A change approval isn't permission to make a change
    - Change control approval is very specific
- Scope may need to be changed during change window

**<u>Downtime</u>**
- Services will eventually be unavailable
    - Change process can be disruptive
    - Usually scheduled during non-prod hours
- Minimize downtime or even prevent any downtime if possible
- Need to inform people about downtime (when to expect, for how long, affected systems)

**<u>Restarts</u>**
- It's common to require a restart
    - Implement a new config
    - Reboot OS
- Services
    - Stop and restart service or daemon
- Applications
    - Close app completely, launch new app instance

**<u>Legacy Applications</u>**
- Apps that have been around awhile
- No longer supported by developer
    - Document system
    - Create specific processes and procedures

**<u>Dependencies</u>**
- "To complete A you must complete B"
- Changing one component will require others

**<u>Documentation</u>**
- Require with change management process
- Update diagrams
- Update policies / procedures

**<u>Version Control</u>**
- Track changes to a file or config data over time
- Revert to previous settings
- Many opportunites to manage versions

#### Summary / Things to Know
"Technical Change Management" is exactly what it sounds like, the technical side of going through change management and the takeaway from this section should be that you need a good overview of the types of things that you will encounter when going through a change.

- What is downtime
- How do we implement version control (GitHub) and why is it so important
- What is an allow or a deny list?
- If you have programming background where do you see this type of stuff pop up?



### 1.4 - Public Key Infrastructure
Public key infrastructure is all about the management of an organizations public keys, Policies, procedures, Hardware, software, people, Digital certificate creation, distribution, management, storing, revoking

This is a huge endeavor to take on and takes a lot of planning, there will be binding of public keys to people or devices involving a Certifiate Authority and other factors. The entire basis of this is about establishing trust within a network / organization.

**<u>Symmetric Encruption</u>**
- Single shared key
    - Encrypt with a key
    - Decrypt with the same key
    - Need abother key if it gets out
- Secret key algorithm
    - Shared secret
- Doesn't scale very well
    - Challenging to distribute
- Very fast to use
    - Less overhead

**<u>Asymmetric Encruption</u>**
- Public key cryptography
    - Two or more mathematically related keys
- Private key kept private
- Public key anone can use
- Private key is only key that can be used to decrypt data from public key
    - Cannot derive public key from private key

**<u>The key pair gpg and pgp</u>**
- Asymmetric encryption
    - PKI
- Key generation
    - Build both public and private key at the same time
    - Lots of randomization
    - Large prime numbers

**<u>Key Escrow</u>**
- Someone else holds decryption keys
    - Private keys are in hands of third party
    - May be within organization
- Can be legitamete business arrangement
    - Access to employee ingo
    - Government agencies need to view data
    - Maybe controversial but might be required in certain cases

#### Summary / Things to Know
PKI is the basis of how we build out the use of keys. Keys are crucial for establishing trust within a organization or a network. There are many different ways to do this, but there needs to be an infrastructure in place so that keys cannot be transferred and used at whatever will.
- What is PKI
- Public Keys vs. private keys
- Symmetric vs. Asymmetric encryption
    - Pros and cons of each
    - When may a 3rd party be needed


### 1.4 - Encrypting data
Encrypting data is all about protecting data at multiple stages of its use, without encryption your data is readable by anyone that may be able to view or access it. Think about how bad this could be if using important data like financial records or credit card numbers.

**<u>Database Encryption</u>**
- Protecting stored data
    - Transmission
- Transparent encryption
    - Encrypt all database information with symmetric key
- Record level encryption
    - Encrypt individual columns
    - Use separate symmetric key for each column
        - Overhead, decryption time, standards

**<u>Transport Encryption</u>**
- Protect data traversing network
- Encrypting in the application
- VPN
    - Encrypts all data trasmitted over the network regardless of the application
    - Client based VPN using SSL / TLS
    - Site-to-site VPN using IPSec

**<u>Encryption Algorithms</u>**
- Many many different ways to encrypt data
- Proper "formula" must be used during encryption and descryption
- Both sides decide on the algorithm before encrypting the data
    - Details are often hidden from the end user
- Advantages and disadvantages between algorithms
    - Security level, speed, complexity of implementation, etc.

**<u>Cryptographic keys</u>**
- Very little that isn't know about cryptographic process
    - Just dont know the key
- The key determines the output

**<u>Key Lengths</u>**
- Larger keys tend to be more secure
    - Prevents brute force attacks
- Symmetric encryption
    - 128 bit or larger symmetric keys are common
    - Numbers get larger and larger as time goes on
- Asymmetric encryption
    - Complex calculations of prime numbers
    - Larger than symmetric
    - Common to see key lengths of 3072 bits or larger

**<u>Key Stretching</u>**
- Make weak key stronger by adding more processes
    - Keep hashing over and over


#### Sumamry / Things to Know
Encrypting data is huge when it comes to protecting data, it is one of the primary lines of defense to ensure that not data is being leaked to people that should not be able to view or read the data.

- Know different ways encryption needs to be used
- In waht different cases may we use different types of encryption
- Pros and cons of using different types of encryption



### 1.4 - Key Exchange

**<u>Logistical Challenge</u>**
- how to share an encryption key across insecure mediums without physically transferring the key?
- Out of band key exchange
    - Telephone, counter, in-person etc.
- In hand key exchange
    - Use asymmetric encryption

**<u>Real time encryption/decryption</u>**
- Share symmetric session key ising asymmtric encryption
    - Client encrypts a random (symmetric) key with a server's public key
    - Server decrypts the shared key and uses it to encrypt data "Session key"
    - Needs to be changed often

#### Summary / Things to Know
Exchanging keys creates a big logistical challenge becuase if the keys are leaked then there is a huge breach in security, so we need to be very careful when considering how it will be done.

- What is out of hand and in hand key exchange, what are some examples.
- What is real time encryption / decryption, what are session keys?



### 1.4 - Encryption Technologies

**<u>Trusted Platform Module (TPM)</u>**
- Specification for cryptographic functions
    - Cryptographic hardware on a device
- Cryptographic porcessor
- Persistent Memory - Unique keys burned in during manufacturing
- Versatile Memory - storage keys, hardware configuration information
- Password Protected, no dictionary attacks

**<u>Hardware Security Module (HSM)</u>**
- Used in large devices
    - Clusters, redundant power
    - Securely store thousands of cryptographic keys
- High-end cryptographic hardware
- Key backups
- Cryptographic connectors

**<u>Key Management System</u>**
- Services are everywhere
    - On-prem or cloud based options exist
    - Many different keys for many different purposes
- Manage keys from centralized manager
    - Often 3rd-party, separate keys from data

**<u>Security Enclave</u>**
- Protectd area for all our secrets
- Implemented as hardware processor
- Provides extensive security features
    - Boot ROM, Root keys, Monitors system boot

#### Summary / Things to Know
There is a lot of enryption technologies out there, the biggest thing to note is that they are used a little different from other storage or data management technologies because they need to be more secure than generic technologies because of the use of keys.

- What is HSM and TPM, what is the difference, how are they used in practice?
- Why do we need a Key Management System or a security enclave?


### 1.4 - Obfuscation
**Obfuscation** --> Process of making something unclear, but not impossible to understand
Might be hiding info in plain sight, can understand if you know how to read it.

**<u>Steganography</u>**
- Security Through Obscurity
    - But its not really security
**Techniques:**
- Network based: Embed messages in TCP packets
- Use an image: Embed message in image itself
- Audio and Video options as well

**<u>Tokenization</u>**
- Data obfuscation
    - hide some of original data
- Protects PII
- Just hidden from view

#### Summary / Things to Know
Obfuscation is the process of making something unclear and the only way to understand it is if you know how to read the unclear data.

- What is tokenization, why is it used over hashing in certain cases
- How does tokenization work? (can see professor messers video on this for the credit card tokenization example)


### 1.4 - Hashing and Digital Signatures
**<u>Hashes</u>**
- Represent data as a short string of text
    - Message digest or a fingerprint
- One way trip
    - Impossible to recover original message from a hash (No decryption)
    - Used to store passwords / configurations
- Verify downloaded document is same as original
    - Integrity
- Can be a digital signature
    - Authentication, Non-repudiation, integrity

**<u>Hash Examples</u>**
- SHA256 Hash
    - 256 bit / 64 hexadecimal characters
- Can create two very different hashes for one small character change

**<u>Practical Hashing</u>**
- Verify a downloaded file
    - hashes may be provided on a downloaded site
    > Adding Salt : Random data added to apassword when hashing. Every user gets their own random salt.
- Password storage
    - Store salted hash
    - Compare hashes at auth process

**<u>Collision</u>**
- Hash functions
    - Take an input of any size
    - Create a fixed size string
    - Message digest, checksum
- Hash should be unique
    - Different inputs should never create same hash, if so, then we call that a collision
- MD5 algorithm saw collision problems so we dont use MD5
    - __Just an example of a case where this has happened__

**<u>Digital Signatures<u>**
- Prove the message was not changes
    - Integrity
- Prove source
    - Authentication
- Make sure signature isn't fake
    - Non-repudiation
- Sign with private key
    - Message doesn't need to be encrypted
- verify with the public key
    - Any change in message will invalidate the signatures

#### Summary / Things to Know
Hashing is all about turning data into an encrypted form, but unlike encryption using asymmetric or symmetric keys, the goal is to make this unrecoverable. However, we cna use the representation for a number of things like authentication factors and ensuring integrity and non-repudiation in many cases.

- What is hashing and wy is it used
- how do we use hashing with storing passwords, how do we use salt in this case
- what are collisions and why must they be avoided? What are some real world examaples where collisions will cause lots of problems for people.



### 1.4 - Blockchain Technology
**Blockchain Technology**: A distributed ledger (everyone has a copy and everyone maintains it) that is used for a number of applications.
Applications:
- Payments
- Digital identification
- Supply chain monitoring
- Digital voting


### 1.4 - Certificates
**<u>Digital Certificates</u>**
- Public key certificate
    - binds a public key with a digital certificate
    - And other details about the key holder
- Digital signature adds trust
    - PKI uses CAs for additional trust
    - Web of trust adds other users for additional trust
- Certificate creation can be built into an OS

**<u>Root Of Trust</u>**
- Everything associated with IT security requires trust
    - Foundational characteristic
- Refer to root of trust to build trust of something unknown
    - Inherently trusted component
    - Hardware, software, firmware, or other components
    - Hardware security module (HSM), Secure enclave, Certificate Authority, etc..

**<u>Certificate Authorities</u>**
- Connect to unkown website
    - Should we trust it?
- need a good way to trst an known entity
    - CA signed certificates can establish that trust ( valid certificate and website/entity)

**<u>3rd Party Trustued CA</u>**
- Built into browsers
- You can purchase a web certificate
    - CA is responsible for vetting the request

**<u>Certificate Signing Request (CSR)</u>**
- Create a key pair, send public key to be CA signed
- CA validates the request
    - COnfirms DNS, emails, and website ownership
- CA digitally signs cert and returns it to applicant

**<u>Private CAs</u>**
- This is where you are your own CA
    - Built in-house
    Devices must trust the internal CA
- Needed for medium to large organizations
- Should be implemented as overall computing stratey

**<u>Self-Signed Certs</u>**
- Internal
- Build your own CA
- Install CA cert/trustued chain on all devices

**<u>Wildcard Certs</u>**
- Subject Alternative Names (SAN)
    - Extension of an X.509 certificate
    - Lists additional identification information
    - Allows certificate to support many different domains
- Wildcard domain
    - Certificate are based on name server
    - Wildcard domain will apply to all server names in a domain

**<u>Key Revocation</u>**
- Certificate Revocation List (CRL)
    - Monitored by CA
    - Can contain many revocations in large file

**<u>OCSP Stapling</u>**
- Online Certificate Status Protocol 
    - Provides scalability to OCSP checks
- CA is responsible for responding to all client OCSP requests, but does not scale will
- have certificate holder verify their own status
    - Status information is stored on certificate holder's server
- OCSP status is "staples" into SSL/TLS handshake
    - DIgitally signed by CA

**<u>Revocation Details</u>**
- Browser can check cert revocation
- not all browsers support


#### Summary / Things to Know
Digital certificates can come in many form, but the basic idea behind using them is establishing digital trust, we are almost never just communicating with another person over the internet, we are almost always connecting and communicating with a number of systems that have nobody monitoring them so we use digital certificate to establish trust.

- How are certifiactes handled on the web
- What is the certificate lifecycle process
- what is the role of the CA











