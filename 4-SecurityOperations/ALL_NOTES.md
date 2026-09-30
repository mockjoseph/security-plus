# 4.0 - Security Operations

### Table of Contents

### 4.1 - Secure Baselines
- Security of an application environment should be well defined
    - All application instances must follow this baseline
    - Firewall setting, patch level, OS file versions
    - May require constant updates
- Integrity measurements check for the secure baseline
    - Performed often
    - Check against well-documented baselines
    - Failure requires an immediate correction

**<u>Deploy Baselines</u>**
- Now have established detailed security baselines
    - Put those baselines into action?
- Deploy the baselines
    - Usually managaed through a centrally administered console
- may require multiple deployment options
    - AD group policy, MDM etc.
- Automation is the key
    - Deploy to hundreds or thousands of devices

**<u>Establish baselines</u>**
- Create series of baselines
    - Foundational security baselines
- Security baselines are often available from the manufacturer
    - Application developer
    - Operating system manufacturer
    - Appliance manufacturer
- Many OS have extensive option
    - Over 3,000 group policy settings in Windows 10
    - Only some of those are associated with security

**<u>Maintain Baselines</u>**
- Many of these are best practices
- Other baselines may require ongoing updates
    - New vulnerability discovered
    - Updated app deployed
    - New OS installed
- test and measure to avoid conflict
    - Some aselines may contradict
    - Enterprise environments are complex


### 4.1 - hardening Targets
- No system is secure with default configurations
    - Need guidelines to keep everything safe
- Hardening guides are specific to application or platform
    - Feedback from maufacturer or internet interest group
    - Other general purpose guides can be found online

**<u>Workstations</u>**
- User desktops and laptops
    - Windows MacOS, linux
- Constant monitoring and updates
- Automate the monthly updates
- Connect to policy management system
- Remove unnecessary software
- Limit threats

**<u>Mobile Devices</u>**
- Always connected mobile technologies
    - Phones, tablets
- Updates are critical
    - Bug fixes, security patches
    - Prevent any known vulnerabilites
- Segmentation can protect data
- Company and user data are seperated
- Control with MDM
    - (Mobile Device Mangaer)

**<u>Network Infrastrucute Devices</u>**
- Switches, routers, etc.
    - Never see them but they're always there
- Prupose built devices
    - Embedded OS, limited OS access
- Configure authentication
- Check with manufacturer
    - Security opdates
    - Not usually updated frequently
    - Updates are usually important

**<u>Cloud Infrastructure</u>**
- Secure the cloud management workstation
    - The keys to the kingdom
- Least priviledge
    - All services, network settings, application rights and permissions
- Congigure endpoint detection and response
    - All devices accessing cloud should be secure
- Always have backups
    - Cloud to cloud (C2C)

**<u>Servers</u>**
- Many and varied
    - Windows, linux, etc.
- updates
    - Operating system updates / servies packs, security patches
- user accounts
    - Minimum password lengths and complexity
    - Account limitations
- Network access and security
    - limit network access
- Monitor and secure
    - Client based security tech

**<u>SCADA / ICS</u>**
- Supervisory control and data acquisition system
    - large scale, multi site, industrial contol system
- PC manages equipment
    - Power generation, refining, manufacturing equipment
    - Facilites, industrial, energy, logistics
- Distributed control systems
    - Requires extensive segmentation

**<u>Embedded Systems</u>**
- Hardware and Software designed for specific function
- Can be difficult to upgrade
- Correct vulnerabilities
- Good to segment into own network and firewall accordingly

**<u>RTOS (Root-time Operating System)</u>**
- An OS with deterministic processing schedule
    - no time to wait for other processes 
    - Industrial equipment, automobile, military environments
- Isolate the system
    - Prevent access from other areas
- Run with the minimum servies
    - prevent the potentioal for exploit
- use secure communicaiton
    - Protect with host-based firewall

**<u>IoT Devices</u>**
- Heating, cooling, lighting, home automation, wearable tech
- Weak defaults
    - IoT manufacturers are not security professionals
    - Change passwords!
- Deploy updated quicly
    - Can be significant security concern
- Segmentation
    - Put IoT devices on their own VLAN


### 4.1 - Securing Wireless and Mobile
**<u>Site surveys</u>**
- Determining existing wireless landscape
    - Sample the existing wireless spectrum
- identify access points
    - May not control all of them
- Work around existing frequencies
    - Layout and plan for interference
- Plan for ongoing site surveys
    - Things will certaintly change
- Heat maps
    - Identify wireless signal strengths

**<u>Wireless Survey Tools</u>**
- Signal coverage
- Potential interference
- Built in tools
- Third party tools
- Spectrum analyzer

**<u>MDM</u>**
- Manage company and user mobile devices
- Centralized management of the mobile devices
    - Specialized functionality
- Set policies on apps, data, camera
    - Control remote devices
- Entire device or a "partition"
- Mangae access control
    - Force screen tacks, PINs

**<u>BYOD (Bring Your Own Device)</u>**
- Employee owns device
    - Meet company's requirements
- difficult to secure
    - Both home device and a work device
    - How is data protected
    - What happens to the data when a device is sold or traded in

**<u>Cellular Networks</u>**
- Mobile devices
    - "Cell" phones
    - 4G, 5G
- Separate land into "cells"
    - Antenna coverages a cell with a certain frequency
- Security concerns
    - Traffic monitoring
    - Location tracking
    - Worlwide access to a mobile device

**<u>COPE</u>**
- Corporate Owned, Personally Enabled
    - Company buys device
    - Used as both personal and corporate device
- Organization maintains full control of device
    - Similar to company owned laptops and desktops
- information is protected using corportate policies
    - Information can be delted at any time
- CYOD - choose your own device
    - Similar to COPE but with users choice of device

**<u>Wi-Fi</u>**
- Full access to internet
- Data-capture
    - Encrypt!!
- DoS attack
- On-path attack
    - Modify / monitor data

**<u>Bluetooth</u>**
- High speed short distances (PAN)
- Do not connect to unknown devices

### 4.1 - Wireless Security Settings
**<u>Securing Wireless Network</u>**
- Wireless network can contain confidential information
    - Authenticate user's before providing access
    - Ensure all communication is confidential
    - Encrypt wireless data
- Verify integrity
    - essage integrity check

**<u>WPA2 PSK problem</u>**
- Brute Force problem
    - Listen to four-way handshake
        - Some methods can derive PSK hash without handshake
    - Capture hash
    - With hash, attackers can brute force the pre-shared key
    - This has become easier as technology improves
    - Once you have PSK, you have everyones wireless key
    - No forward secrecy

**<u>WPA3 and GCMP</u>**
- Wi-fi prtected Access 3 (2018)
- GCMP block cipher mode
    - GaloisCOunter mode protocol
    - Stronger encryption than WPA2
- GCMP security servies
    - Data confidentiality with AES
    - Message Integrity check with Galois Message Authentication Code (GMAC)

**<u>SAE</u>**
- WPA3 changes pSK auth process
    - mutual authenticaiton
    - Creates share session key without sending key across network
    - No foour-way handshake, no hashes, no brute force
- Simultaneous Authentication of Equals
    - __Diffie-Helman__ derived key exchange with an authentication component
    - Everyone uses different session key even with same PSK
    - IEEE standard-dragonfly handshake

**<u>Wireless Security Modes</u>**
- Configure the authentication on your wireless access point / wireless router
- Open system / None
    - No auth password required
- WPA3 - Personal / WPA3-PSK
    - WPA3 with preshared key
    - Everyone uses same 256-bytes
- WPA3 Enterprise / WPA3-802.1X
    - Authenticates user individually with authentication server (ie RADIUS)

**<u>AAA Framework</u>**
- Identification
    - This is who you claim to be (username)
- Authentication
    - Prove who you say you are
    - Password and other authenitcation factors
- Authorization
    - Based on identification and authentication, what access do you have
- Accounting
    - Resources used, ligin time, data sent and received, logout time

**<u>RADIUS</u>**
- Remote Authentication Dial In User Service
- ONe of more common AAA protocols
    - Supported on a wide variety of platforms and devices
    - Not just for dial in
- Centralize authentication for users
- Routers, switches, firewalls
- Server authentication
- Remote VPN access
- 802.1x network access
- RADIUS services available on almost any server operating system

**<u>IEE 802.1X</u>**
- Port ased Network accesscontrol 
- Dont gt access to network until you authenticate
- Used in conjuntion with AAA server
- RADIUS, LDAP, TACACS+

**<u>EAP</u>**
- Extensible Authenticatino Protocol
    - An authentication framework
- Many different ways to authenticate based on RFC standards
    - Manufactureres can build own EAP methods
- EAP integrats with 802.1X
    - prevents access to network until authentication succeeds

**<u>IEE 802.1X and EAP</u>**
- Supplicant - The Client
- Authenticatory Device that provides access
- Authentication server - Validates client credentials

### 4.2 - Application Security
**<u>Secure COding Concepts</u>**
- Balance between time and quality
    - Programming with security in minds is often secondary
- Test and QA process
- Vulnerabilities will eventually be found (and exploited)

**<u>Input Validation</u>**
- Unexpected inputs will not be interpreted by application
- Document all input methods
    - Forms, fields, types
- Check and correct all input (normalization)
- Fuzzers will finds what you missed

**<u>Secure Cookies</u>**
- Cookies
    - Information stored on computer by browser
- Used for tracking, personalization, session management
- Not executable so not generally a risk unless someone gets access to them
- Secure cookies have secure attribute set
    - Browser will only send it over HTTPS
- Sensitive information should not be saved ina. cookie

**<u>Static Code Analyzers</u>**
- SAST
    - Help identify security flaws
- Not everything can be identified through analysis
- Still have to verify each finding

**<u>Sandboxing</u>**
- Applicaitons cannot access unrelated servers
- Commonly used during development
- Used in many different deployments
    - VMs, mobile devices, browser frames
    - Windows user account control

**<u>Code Signing</u>**
- Application is deployed
- Security questions
    - has app been modified
    - App was indeed written by secure dev
- App code can be digitally signe by developer

**<u>Application Security Monitoring</u>**
- Real-time information (app-usage, access demographics)
- View blocked attacks (SQL injection, patched vulnerabilities)
- Audit the logs (Find information gathering and hidden attacks)
- Anamoly detection

### 4.2 - Asset Management
**<u>Acquisition / Procurement Process</u>**
- The purchasing process
    - Multi-step process for requesing and obtaining goods and services
    - Start with request from the user
    - usually includes budgeting information and formal approvals
- Negotiate with suppliers
    - Terms and conditions
- Purchase, invoice, payments
    - The money part

**<u>Assignment / Accounting</u>**
- Central asset tracking system
    - Used y different parts of the organization
- Ownership
    - Associate a person with an asset
    - Useful for tracking system
- Classification
    - Type of asset
    - Hardware (capital expenditure)
    - Software (operating expenditure)

**<u>Monitoring / Asset tracking</u>**
- Inventory every asset
- Associate a support ticker wtih a device make and model
- Enumeration
    - List all parts of asset
- Asset tag
    - Barcode, RFID, tracking number

**<u>Media Sanitization</u>**
- System disposal or decommissiioning
    - Completely remove data
- Different use cases
    - Clean Hard Drive or delte a single file
- One way trip
    - No recovery whatsoever
- Reuse storage media
    - Ensure nothing is left behind

**<u>Physical Destruction</u>**
- Shredder / Pulverizer
- Drill / Hammer
- Electromagnetic (degaussing)

**<u>Certificate of Destruction</u>**
- Destruction done by third party
- Need confirmation of destruction

**<u>Data Retention</u>**
- Backup data
    - How much and where
    - Copies and versions
- Regulatory compliance
    - Certain amount of data backup may be required
- Operational needs (accidental deletion, disaster recovery)
- Differentiate by type and application
    - Recover data needed when needed

### 4.3 - Vulnerability Scanning
- Usually minimally intrusive
    - Unlike pen test
- Port scan
    - Poke around see whats open
- Identify systems
    - And security devices
- Test from the outside and inside
- Don't dismiss insider threats
- Gather as mich information as possible

**<u>Static code analyzers</u>**
- SAST
- Review source code for vulns
- Verify each finding

**<u>Dynamic Analysis</u>**
- Send random input to an app
- Looking for something out of the ordinary

**<u>Fuzzing Engines and Frameworks</u>**
- Many different fuzzing options
    - Platform specific, language specific
- Very time and processor resource beavy
    - Many many different iterations to try
    - Many fuzzing engines use high-probability tests

**<u>Package Monitoring</u>**
- Some applications are distributed in a package
    - Escpecially open source
    - Supply chain integrity
- COnfirm package is legitamete
    - Trusted source
    - No added malware
    - No embedded vulnerabilities


### 4.3 - Threat Intelligence
- Research the threat and threat actors
- Data is everywhere
    - hacker group profiles, tools used by attackers and much more
- Make decisions based on the intelligence
    - Invest in best prevention
- Used by researchers, security operations teams and others

**<u>Open Source Intelligence (OSINT)</u>**
- Open source
    - Public sources, groups etc.
- Internet
- Government data
- Commercial data

**<u>Information sharing Organization</u>**
- Public threat intelligence
    - Often classified information
- Private threat intelligence
    - Private companies have extensive resources
- Need to share critical security details
    - Real time high quality cyber-threat information sharing
- Cyber threat alliance (CTA)
    - Members updates specifically formatted threat intelligence
    - CTA scores each submission are validates across other submissions
    - Other members can extract the validated data

**<u>Dark Web Intelligence</u>**
- Dark web
    - Overlay networks that use internet
    - Requires specific software and configuration to access
- hacking groups and services
    - Activities, tools and techniques, credit card saled
    - Accounts and passwords
- monitor forums for activity
    - Company names, executive names

### 4.3 - Penetration Testing
**Pen Test** --> simulate an attack
- Similar to vuln scan process
    - Actually try to exploit though
- Often compliance mandate
    - regular pen-testing by third party
- National Institute of Standards and Technology (NIST) Technical Guide to Information Security and Assessment

**<u>Rules of Engagement</u>**
- Important document
    - Defines purpose and scope
    - Makes everyone aware of test parameters
- Type of testing and schedule
    - On-site physical breack internal and external test
    - Normal working hours, after 6PM only etc.
- Rules
    - IP address ranges, emergency contacts, handling sensitive information, in-scope and out of scope devices and apps

**<u>Exploiting Vulnerabilities</u>**
- Try to break into system
    - Can assure DoS on loss of data
    - Buffer overflows can cause instability
    - Gain priviledge escalation
- May need to try different vulnerability types
- Only be sure or vulnerable if you can bypass security

**<u>Responsible Disclosure Program</u>**
- Takes time to fix a vulnerability
    - Software changes, testing, deployment etc.
- Bug bounty programs
    - Reward for discovering vulnerabilities
    - Earn money for hacking a system
    - Document vulnerability to earn cash
- Controlled info release
    - Report vulnerability
    - Fix and make public

**<u>Process</u>**
- Initial exploitation
    - Get into network
- Lateral movement 
    - Move system to system
    - Inside network is relatively unprotected
- persistence
    - Need to be sure of getting back in
- Pivot
    - Gain access to not normally accessible ones
    - use vulnerable system as proxy or relay


### 4.3 - Analyzing Vulnerabilities
**<u>Dealing with False Info</u>**
- False positives
- Different than low-security vulnerabilities
    - Real but may not be highest priority
- False negatives
    - Much more dangerous
- Update to latest signatures
- Work with vulnerability management manufacturer

**<u>Prioritizing Vulnerabilities</u>**
- Not every vulnerability shares some priority
    - Some may not be significant others critical
- Difficult to determine
- Refer to public disclosures and vulnerability databases

**<u>CVSS</u>**
- National vulnerability database http://nvd.nist.gov/
- Synchronized with CVE list
- Enhanced search functionality
- Comon Vulnerability Scoring System (CVSS)
    - Quantitative scoring of a vuln 0 - 10
    - Scoring standards change over time
- Industry collab

**<u>CVE (Common Vulnerabilities and Exposures)</u>**
- Vulns can be across referenced online
- Many databases and places to search
- Some cannot be definitevely identified

**<u>Classification</u>**
- Scanner looks for everything
    - Signatures are key
- App scans, web app scans
- Network scans

**<u>Environment Variables</u>**
- Prioritization and patching frequency
- Where located? Environment type?
    - Everyone is different

**<u>Exposre Factor</u>**
- Loss of value or business activity if vulnerability is exploited
    - Expressed as percentage
- Limit acces? 50%
- Disable? 100%

**<u>Industry / Organizational Impact</u>**
- Some exploits have significant consequences
- Hospital / Healthcare impacts

**<u>Risk Tolerance</u>**
- Amount of risk acceptable to organization
    - can't remove all risk
- Timeing of security patches
- Testing takes time
    - Middle ground


### 4.3 - Vulnerability Remediation
**<u>Patching</u>**
- Most common mitigation technique
    - Know vulnerability exists
    - patch file to install
- Scheduled vulnerability / patch notices
    - Monthly, quarterly
- Unscheduled can
    - Zero day
- Ongoing process

**<u>Insurance</u>**
- Cybersecurity insurance coverage
    - Lost revenue, data, recovery costs, money lost to phishing
    - Privacy lawsuit costs
- Doesn't cover everything
    - Intentional acts funds transfers
- Ransomware increased popularity of cybersecurity liability insurance
    - Applies to every organization

**<u>Segmentation</u>**
- Limit the scope of an exploit
    - Seperate devices into their own networks / VLANs
- Breach would have limited scope
- Can't patch?
    - Disconnect from the world, air gaps may e required
- use internal NGFW
    - Block unwanted / unnecessary traffic between VLANs
    - Identify malicious trafic on the inside

**<u>Physical Segmentation</u>**
- Seperate devices
    - Multiple units, seperate infrastructure
- Virtual Local Area Networks (VLANs)
    - Seperated logically instead of physically
    - Cannot communicate between VLANs without a layer 3 device/router

**<u>Compensating Controls</u>**
- Optimal security methods may not be available
- Compensate in other ways
    - Disable service, revoke access, limit access
    - Modify internal security controls and software firewalls
- Provide coverage until patch deployed

**<u>Exceptions and Exemptions</u>**
- Removing vulnerability is optimal
    - Not everything can be patched though
- Balancing act
    - Provide the service, but also protect the data and systems
- Not all vulnerabilities share the same severity
    - may reqiire local login, physical access, other criteria
- Exception may be an option

**<u>Validation of Remediation</u>**
- Vulnerability now patched
    - Does the patch really stop the exploit?
    - Did all systems receive patch?
- rescanning
- Audit (check systems, verify competition)
- Verification

**<u>Reporting</u>**
- Ongoing checks are required
- new vulnerabilities continuously discovered
- Difficult / impossible to manage without automation
- Continuous reporting
    - Number of vulnerabilities, patched vs. unpatched
    - new threat notifications


### 4.4 - Security Monitoring
- Attackers don't sleep
- Monitor all entry points 247/365
- React to security events
- Status dashboards

**<u>Log Aggregation</u>**
- SIEM or SEM toos ( security information and event manager)
    - Consolidate many logs to central database
    - Servers, firewalls, VPN concentrators, SANs, cloud services
- Centralized reporting
    - All info in one place
- Correlation between diverse systems
    - View authentication and access
    - track application access
    - Measure and report data transfers

**<u>Monitoring Computing Resources</u>**
- Systems
    - Authentications - logins from strange places
    - Server monitoring - service activity, backups, software versions
- Applications
    - Availability, Data Transfers, Security notifications
- Infrastructure
    - Remote access systems, firewallsm and IPS reports

**<u>Scanning</u>**
- Constantly changing threat landscape
    - New vulnerabilities are discovered daily
    - many different business apps and services
    - Systems and people are always moving
- Actively check systems and devices
    - OS system types and versions
    - Device driver versions, installed appliactions
    - potential anomalies
- Gather the raw details

**<u>Reporting</u>**
- Analyze collected data
    - Create "actionable" reports
    - Status information
    - Determine the best next steps
    - Ad hoc information sumamries

**<u>Archiving</u>**
- Takes an average of 9 moths for company to identify and contain a breach
    - IBM security report 2022
- Access to data is critical
    - Archive over extended period
- May have a mandate

**<u>Alerting</u>**
- Real-time notifications of security events
    - Increase in auth errors
- Actionable data
    - keep people informed
- Notification methods
    - SMS / Text, email, security console

**<u>Alert Response and Remediation</u>**
- Quarantine
    - prevent potential security issue from spreading
- Alert tuning
    - Balancing out, prevent false positives and negaitves
- An alert should be accurate
    - Ongoing process, tuning gets better as time goes on


## 4.4 - Security Tools
**<u>Security Content Automation Protocol (SCAP)</u>**
- Many different security tools on market
- NGFWs, IPS, vuln scanners, etc.
- All have their own way of evaluating threat
- Managed by NIST
- Allows tools to identify and act on same criteria
- Vallidate security config, confirm patch installs, scan for secrity breaches

**<u>Using SCAP</u>**
- SCAP content can be shared between tools
    - Focused on config compliance
    - Detect applications with known vulnerabilities
- Especially useful in large environments
    - Many different OS and applications
- Specification standard enable automation
- Automation types
    - Ongoing monitoring notifications, alerting, patching

**<u>Benchmarks</u>**
- Apply security best practices to everything
    - Operating systems, cloud providers, mobile devices
    - Popular: Center for Internet Security

**<u>Agents / Agentless</u>**
- Check to see if device is in compiance
    - Install software onto device
    - Run an on-demand gent check
- Agents can usually provide more detail
    - Monitoring for real-time notifications
    - Must be maintained and updated
- Agentless runs without formal install
    - Persorms check, then disappears

**<u>SIEM</u>**
- Logs security events and information
- Log collection of security alerts
- Log aggregation and long-term storage
    - Include advanced reporting
- Data correlation
    - link diversse data types

**<u>Anti-virus and Anti-malware</u>**
- Anti-virus is popular teerm
    - Trojans, worms, macro viruses
- Malware refers to broad malicious software
- Terms are effectively same these days

**<u>DLP</u>**
- Wheres the sensitive data
- Stop data before attackser gets it
- Many sources, many destinations

**<u>SNMP</u>**
- Simple Network Management Protocol
- Database of data (MIB): management Information base
- Database contains OIDs: Object Identifiers
- Poll devices over udp/161
- Request statistics of device
- Poll devices at fixed intervals

**<u>SNMP traps</u>**
- Most operations expect poll
    - Devices respond to the request
- SNMP traps can be configured on monitored device
    - Communicates over udp / 162
- Set threshold for alerts
    - CRC error threshold, send trap
    - Monitoring station can react immediately

**<u>NetFlow</u>**
- Gather traffic statistics from all fraffic flows
    - Shared communication between devices
- NetFlow --> standard colelction method
    - Probe and collector setups
    - usually searate reportin app

**<u>Vulnerability Scanners</u>**
- Minimally invasive
- Port scan
    - identify systems
    - Test from outside and inside
    - Gather as much info as possible



