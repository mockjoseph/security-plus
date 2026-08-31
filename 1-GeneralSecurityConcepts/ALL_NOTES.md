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





