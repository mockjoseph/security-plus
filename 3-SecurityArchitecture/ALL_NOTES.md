# 3.0 - Security Architecture

### Table Of Contents

### 3.1 - Cloud Infrastructure
- IaaS, PaaS, SaaS
    - Who is responsible for security
- Security should be well documented
    - Most cloud providers provide a matrix of responsibilities
    - Everyone knows up-front
- These responsibilities can vary
    - Different cloud providers
    - Contractural argreements

**<u>Hybrid Considerations</u>**
- Hybrid Cloud
    - More than one public or private cloud
    - Adds additional complexity
- Network protection mismatches
    - Authentication across platforms
    - Firewall configurations
    - Server settings
- Different security monitoring
    - Logs are diverse and cloud specific
- Data leakage
    - Data is shared across public internet

**<u>Third Party Vendors in the Cloud</u>**
- You, cloud provider, third parties
    - Infrastructure technologies
- Ongoing vendor risk assessments
    - part of an overall vendor risk management policy
- Include thirs party impact for incident response
    - Everyone is part of process
- Constant monitoring
    - Watching for changes and unusual activity

**<u>Infrastructure as Code</u>**
- Describe an infrastructure
    - Define servers, network, and applications as code
- modify infrastructure and create versions
    - Version application code
- Use the description (code) to build other application instances
    - Build the same way every time based on the code
- Important concept in cloud computing
    - Build a perfect version everytime

**<u>Serverless Architecture</u>**
- Function as a Service (FaaS)
    - Apps separated into individual autonomous functions
    - Remove OS from the equation
- Developer still creates server side logic
    - Runs in a stateless compute container
- may be event triggered and ephemeral
    - May only run for one event
- managed by a third party
    - All OS security concerns are at third party

**<u>Microservices and APIs</u>**
- Monolithic applications
    - One big application that does everything
- Ap contains all decision making processes
    - User interfaces
    - Data input and output
    - Business logic
- Code challenges
    - Large codebase
    - Change control settings
- APIs (cloud = microservice)
- API is glue for microservice
    - Work together to act as app
- Scalable and resilient
- Outages are contained


### 3.1 - Network Infrastructure Concepts
**<u>Physical Isolation</u>**
- Devices are physically separate
    - Air gap between switch A and B
- Must be connected to provide communication
    - Direct connect or another switch / monitor
- Web services in one rack, DB services in another
- Customer A on one switch, Customer B on another switch
    - No opportunity for mixing data

**<u>Logical Segmentation with VLANs</u>**
- Virtual Local Area Network (VLAN)
    - Supported logically instead of physically
    - Cannot communicate between VLANs without a layer 3 device / router

**<u>SDN (Software Defined Networking)</u>**
- Networking devices have different functional planes of operation
    - Data, control, management planes
- Split the functions into separable logical units
    - Extend the functionality and management of a single device
    - perfectly built for the cloud
**Infrastructure / Data Plane Layer**
- Process network frames and packets
- Forward, tracking, encrypting, NAT
**Control layer / Control Plane**
- manages actions of the data plane
- Routing tables, session tables, NAT tables
- Dynamic routing protocol updates
**Application Layer / Management Plane**
- Configure and manage the device
- SSH, browser, API

### 3.1 - Other Infrastructure Concepts
**<u>Attacks can happen anywhere</u>**
- Two categories for IT security
    - On-prem, cloud based 
        - Advantages and disadvantages to both
- Cloud based is centralized, costs less
- On-prem puts security burden on owner

**<u>On-Prem Security</u>**
- Customize security posture
    - Full control when everything is in-house
- On-site IT team can manage security better
    - Local team can ensure everything is secure
    - local team can be expensive and difficult to staff
- Local team maintains uptime and availability
    - System checks can occur at anytime
    - no phone call for support
- Security changes can take time

**<u>Centralized vs. Decentralized</u>**
- most organizations are physically decentralized
    - Many locations, cloud providers, OS, etc.
- difficult to manage and protect so many diverse systems
    - Centralize the security management
- Centralized approch:
    - Correlated alert
    - Consolidated lof file analysis
    - Comprehensive system status and maintenance / patching
- It's not perfect
    - Single pint of failure, potential performance issue

**<u>Virtualization</u>**
- Run many different OS on same hardware
- Each app instance has its own OS
- Adds overhead and complexity
- Virtualization is relatively expensive

**<u>Applicaiton Containerization</u>**
- Container:
    - Contains everything needed to run an app
    - Code and dependencies
    - Standardized unit of software
- An isolated process is a sand box
    - Self contained
    - Apps cant interact with eachother
- Container image:
    - Standard for prtability
    - Lightweight, uses host kernel
    - Secure separation between apps

**<u>IoT</u>**
- Sensors
    - heating, cooling, lighting
- Smart devices
    - Home automation, video doorbells
- Vulnerabilities
- Facility automation
- Weak defaults

**<u>SCADA / ICS</u>**
- Supervisory Control and data Acquisition System (SCADA)
    - Large scale multi site Industrial Control System (ICS)
- PC manages equipment
    - Power generation, refining, manufacturing equipment
    - Facilities, industrial, energy, logistics
- Distributed control system, requires extensive segmentation

**<u>RTOS Real-Time OS</u>**
- OS with deterministic processing schedule
    - No time to wait for other processes
    - industrial equipment, automobiles
- Extremely sensitive to security issues

**<u>Embedded System</u>**
- hardware and Software designed for specific function
    - Or to operate as part of larger system
- built with only this task in mind

**<u>High Availability</u>**
- Redundancy doesn't always mean available
    - may need to be powered manually
- HA (High Availability)
    - Always on
- may include any different components working together
- Higher availability almost always means higher cost

### 3.1 - Infrastructure Considerations
**<u>Availability</u>**
- System uptime
    - Access data, complete transactions
- Releasing act with security
    - Spend a lot fo time and money on availability
- Important metric

**<u>Resillience</u>**
- Eventually something will happen
    - Can you maintain availability? Power? how quickly?
- based on many different variables
    - Root cause, replacement hardware installation
    - Software patch availability
    - Redundant Systems
- Commonly referenced as MTTR (Mean Time To Response)

**<u>Cost</u>**
- how much money is required
    - Everything ultimately comes down to cost
- Initial installation
    - Very different across platforms
- Ongoing maintenance
- Replacement / repair
- Tax implications

**<u>Responsiveness</u>**
- Request information
    - Get a response, how quickly did it happen
- Escpecially important for interactive applicaitons
- Speed isan important metric
    - All parts of application contribute, weakest link

**<u>Scalability</u>**
- how quickly can increase or decrease capacity?
    - Elasticity
- There's always resource challenge
    - Whats preventing scalability
- needs to include security monitoring
    - Increases and decreases with scale

**<u>Ease if Deployment</u>**
- Application has many moving parts
    - Web-server, database, caching, server, firewall, etc
- Might be an involved process
    - hardware resources, cloud budgets, change control
- Might be simple
    - Orchestration / Automation
- Important to consider during product engineering phase
    - One missed detail can cause deployment issues

**<u>Risk Transference</u>**
- Many methods to minimize risk
- Cybersecurity insurance
- Recover internal losses
- protect against legal issues from customers

**<u>Ease of Recovery</u>**
- Something will go wrong
    - Time is money, how easy and quickly can you recover
- malware infection
    - Reload OS from original media ~ 1 hour
    - Reload from corporate image   ~ 10 minutes
- Another important design criteria
    - May be critical to the final product

**<u>Patch Availability</u>**
- Software isn't static
- Often first task after installation
- most companies have reular updates
- Some companies rarely patch
    - Might be significant concern

**<u>Inability to Patch</u>**
- Embedded systems
- not designed for end user updates
- may need additional security controls

**<u>Power</u>**
- Foundational element
    - Can require extensive engineering
- Overall power requirements
    - Primary power
    - backup services

**<u>Compute</u>**
- Applicaitons heavy lifting
    - Morethan just single CPU
- The compute engine
- May be limited to a single processor
- use multiple CPUs across multiple clouds
- Additional complexity, enhanced scalability

**<u>Secure Infrastructures</u>**
- Every network is different
    - There are often similarities
- Firewalls
    - Separate trusted from untrusted
    - Provide additional security checks
- Other services may require their own security technologies
    - Honeypots, jump servers, load balancers, sensors

**<u>Security Zones</u>**
- Zone based security technologies
    - More flexible and secure than IP ranges
- Each area of network is associated with a zone
    - Trusted, untrusted
    - Internal, external
    - Inside, internet, sensors, databases scanned
- Simplifies security policies
    - Trusted to untrusted
    - untrusted to screened
    - Untrusted to trusted

**<u>Attack Surface</u>**
- How many ways into home
- Everything can be a vulnerability
    - App code
    - Open ports
    - Auth process
    - Human error
- Minimize the surface

**<u>Connectivity</u>**
- Everything contributes to security
    - Including network connection
- Secure network cabling
    - Protect physical drops
- Application level encryption
    - hard work has already been done
- Network level encryption
    - IPSec tunnels, VPN connections


### 3.2 - Intrusion Prevention
**<u>Intrusion Prevention System (IPS)</u>**
- Watch network traffic
- Intrusions
    - Exploits against operating systems, applications, etc.
    - Buffer overflows, cross-site scripting and other vulnerabilities
- Detection vs. prevention
    - IDS : alarm/alert
    - IPS : Prevent

**<u>Failure modes</u>**
- Hope for 100% uptime
    - Unlikely though
- Fail-open
    - When systems fail, data still flows
- Fail-cosed
    - Data doesn't flow or fail

**<u>Device Connections</u>**
- Active monitoring
    - System is connected inline
    - Data can be blocked in real-time as it passses by
    - Intrusion prevention is commonly active
- Pasive monitoring
    - Copy of network traffic is examined using tap or port monitor
    - Data cannot be blocked in real time
    - Intrusion detection is commonly passive

**<u>Active Monitoring</u>**
- IDS / IPS sits physically inline
    - All traffic passes through it
- Malicious traffic is immediately identified
    - Dropped at IPS

**<u>Passive Monitoring</u>**
- Examine copy of traffic
    - Port mirror, network tap
- No way to block (prevent) trafic


### 3.2 - Network Appliances
**<u>Jump Server</u>**
- Access secure network zones
    - provides access mechanism to a protected network
- Highly secured device
    - Hardened and monitored
- SSH / Tunnel / VPN to the jump server
    - RDP, SSH or jump from there
- Significant security concerm

**<u>Proxies</u>**
- Sit between users and external network
- Receives user requests and sends the request on their behalf (the proxy)
- useful for caching information, access control, URL filtering, content scanning
- Applications may need to know how to use the proxy (explicit)
- Some proxies are invisible (transparent)

**<u>Application Proxy</u>**
- One of simpplest "proxies" is NAT
    - Network level proxy
- most proxies in use are application proxies
    - Proxy understands the way the application works
- Proxy may know only one application (ex: HTTP)
- Many proxies are multipurpose proxies
    - HTTP, HTTPS, FTP, etc.

**<u>Forward Proxy</u>**
- An "internal proxy"
    - Commonly used to protect and control user access to the internet (within an organization)

**<u>Reverse Proxy</u>**
- inbound traffic from internet to internal service
    - Provides additional security (user doesn't communicate directly)
    - Can act as caching as well

**<u>Open Proxy</u>**
- Third party uncontrolled proxy
    - Can be significant security concern
    - Often used to circumvent existing security controls

**<u>Load Balancers</u>**
- Distribute the load
    - Multiple servers
    - invisible to end user
- Large scale implementation
    - Web server farms, database farms
- Fault tolerance
    - Server outages have no effect
    - Very fast

**<u>Active/ active load balancing</u>**
- Configurable load
    - Manage across servers
- TCP offload
    - Protocol overhead
- SSL offload
    - Encryption / Decryption
- Caching
    - fast response
- Prioritization
    - QoS, content switching

**<u>Active / Passive Load Balancing</u>**
- Some servers are active
    - Others are on standby
- If an active server fails, passive server takes its place

**<u>Sensors and Collectors</u>**
- Aggregate information from network devices
    - Built-in sensors, separate devices
    - Integrated into switches, routers, servers, firewalls, etc.
- Sensors
    - IPS, FW logs, auth, web-server access, DB transaction, email logs
- Collectors
    - Proprietary consoles (IPS, firewall) SIEM consoles, syslog servers
    - Many SIEM include correlation engine to compare diverse sensor data


### 3.2 - Port Security
- Created many auth methods through the years
    - Network admin has many choices
- Use a username and password
    - Other factors can be included
- Commonly used on wireless networks
    - Also works on wired

**<u>EAP</u>**
- Extensible Authentication Protocol (EAP)
    - Authorization framework
- Many different ways to authenticate baed on RFC sstandards
    - Manufactureers can build their own EAP methods
- EAP integrates with 802.1 X
    - Prevents access to network until authorization succeeds

**<u>IEE 802.1 X</u>**
- Port based network access control
- Don't get access to network until you authenticate
- EAP integrates wit 802.1 X
- Extensible Authentication Protocol
- 802.1 X prevents accesss to network until athentication succeeds
- Used in conjunction with authentication to database
    - RADIUS, LDAP, TACACS+, kerberos, etc.


### 3.2 - Firewall Types
**<u>Universal Security Control</u>**
- Standard Issue
    - Control the flow of network traffic
    - Everything passes through the firewall
- Corporate control of out and inbound data
    - Sensitive materials
- Control of inappropriate content
    - NSFW, parental contorls
- Protection against evil
    - Anti virus, anti malware

**<u>Network Based Firewalls</u>**
- Filter traffic by port # or application
    - OSI layer 4, OSI layer 7
    - Traditional vs. NGFW firewalls
- Encrypt traffic
    - VPN between sites
- Most firewalls can be layer 3 devices (routers)
    - Often sits on ingress / egres of network
    - Network Address Translation (NAT) functionality
    - Authenticate dynamic routing communication

**<u>UTM / All in one Security Appliance</u>**
- Unified threat management
- URL filter
- malware inspection
- Spam filter
- CSU / DSU
- Router / Switch
- FW / IDS / IPS
- Bandwidth Shaper
- VPN endpoint

**<u>NGFWs</u>**
- OSI app layer
    - All data in every packet
- Can be called different names
    - App layer gateway
    - Stateful multi-layer inspection
    - Deep packet inspection
- Requires advances decodes
    - Every packet must be analyzed and categorized vefore security decision is determined
- Network based FW
    - Control traffic flow based on app
- Intrusion Prevention Systems
- Content filtering
    - URL filters, control site by categories

**<u>Web App FW<u>**
- Not normal FW
- Allow or deny based on expected inut
- SQL injection
- Major focus on Payment Card Industry Data Security Standard (PCI DSS)


### 3.2 - Secure Communication
**<u>VPNs</u>**
- Virtual Private Network
    - Encrypts all private data traversing publicc internet
- Concentrator
    - Encryption / Decryption across device
    - Often integrated into firewall
- many deployment options
    - Specialized cryptographic hardware
    - Software based solutions

**<u>Encrypted tunnel</u>**
- Kep data private across public internet
    - Encryption is key
- Encrypt data
    - Address headers and trailers

**<u>SSL / TLS / VPN (secure sockets layer)</u>**
- Uses common SSL/TLS protocol
    - ALmost no FW issues
- No big VPN clients
    - usually remote access communication
- Authenticate users
    - no requirement for digital certificates or shared passwords (like IPSec)
- Can be run from a browser or from a (usually light) VPN client

**<u>SSL / TLS VPN</u>**
- On demand access from a remote device
    - Software connects to a VPN concentrator
- Some software can be configured as always-on

**<u>Site-to-Site IPSec VPN</u>**
- Always on or (almost)
- Firewalls often act as a VPN concentrator

**<u>SD-WAN</u>**
- Software Defined Networking in a Wide Area Network
    - WAN built for the cloud
- Data center used to be in one place
    - Cloud has changed everything
- Cloud based application communicates directly to the cloud
    - No need to hop through the central point

**<u>Secure Area Service Edge (SLSE)</u>**
- Update secure access for cloud services
    - Securely connect from different locations
- Secure access service edge (SASE)
    - "Next generation" VPN
- Security tech based in cloud
- SASE clients on all devices

**<u>Selection of Effective Controls</u>**
- Many different security options
    - Selecting right choice can be challenging
- VPN
    - SSL / TLS VPN for user access
    - IPSec tunnel for site-to-site access
- SASE
    - Coporate network and security solution
- SD-WAN
    - Manage network connectivity to cloud
    - Does not adaquately address security concerns


### 3.3 - Data Types and Classification
**<u>Data Types</u>**
- Refulated
    - Managed by third party
    - Government laws and statues
- Human readable
    - Clear, obvious
- Non-human readable
    - Encoded data, barcodes
- Some formats are hybrid
- Trade Secrets
    - An organizations secret formulas
- Intellectual property
    - Mostly public, copyright trademark
- Legal information
    - Court records/docs, judge / attorney info
    - PII other sensitive details
    - Stored in many different systems
- Financial information

**<u>Classifying Sensitive Data</u>**
- Not all data has same level of categorization
    - License tag numbers vs. health records
- Different levels require different security and handling
    - Additional permissions
    - Different process to view
    - Restricted network access

**<u>Data Classifications</u>**
- Proprietary
    - Data that is property of an organization
    - May also include trade secrets
    - Data unique to an organization
- PII - Personaly Identifiable Information
    - Data that can be used to identify an individual
    - Name, DOB, mother's maiden name, biometric information
- PHI - Protected health information
    - Health info, status
**Putting in buckets**
- Sensitive
    - intellectual, PII, PHI
- Confidential
    - Very sensitive, must be approved to view
- Public / Unclassified
    - No retrictions on viewing data
- private / Classified / Restricted
    - restricted access, may require NDA
- Critical
    - Data should always be accessible

### 3.3 - States of Data
**<u>Data at Rest</u>**
- Data is ona storage device
- Encrypt the data
    - Full-disk encryption
    - Database
    - File-based or folder
- Apply permissions
    - Access control lissts
    - Only authorized users can access the data

**<u>Data in Transit</u>**
- Data transmitted over the network
- Not much protection as it travels
    - many switches, routers, devices
- Network based protection
    - Firewall, IPS
- Provide transport encryption
    - TLS, IPSec

**<u>Data in Use</u>**
- Data is actively processing in memory
- Data is almost always decoupled
- Attackers can pick decrypted information out of RAM
    - Very attractive option

**<u>Data Sovereignty</u>**
- Data that resides ina. country is subject to laws of that country
    - Legal monitoring, court orders, etc.
- Laws may prohibit where data is stored
    - GDPR (General Data Protection Regulation)
    - Data collected on EU citizens must be stored in RU
    - Complex mesh of technology and legalites
- Where is data stored
    - Compliance lwas may prohibit moving data out of the country

**<u>Geolocation</u>**
- Location details
    - Tracks within localized area
- Many ways to determine location
    - 802.11, mobile providers, GPS
- Can be used to manage data access
    - Prevent access from other countries
- Limit administrative tasks unless secure area is used
    - Permit enhanced access when inside the building


### 3.3 - Protecting Data
**<u>Geographic Restrictions</u>**
- Network location
    - Identify based on IP subnet
    - Can be difficult with mobile devices
- Geolocation determines user's location
    - GPS - mobile devices, very accurate
    - 802.11 wireless, less accurate
    - IP address, not very accurate
- Geofencing
    - Automatically allow or restrict access when a user is in a particular location

**<u>Protecting the Data</u>**
- Data is everywhere
    - Storage, network, CPU
- Encryption security policies
- Data permissions

**<u>Encryption</u>**
- Encode information into unreadable data
- Two-way street
    - If have proper key
- Confusion
    - Encrypted data is drastically different than plain-text

**<u>Hashing</u>**
- Represent data as a string of text
    - Message digest, fingerprint
- One way trip
    - Impossible to recover original data
- Verify downloaded document is same as original
- Passwords
- Digital signature
    - Authentication, non-repudiation, integrity
- Will not have collision (hopefully)

**<u>Obfuscation</u>**
- Make something understandable into very difficult to understand
- Take perfectly readable code and turn it into nonsense

**<u>Masking</u>**
- Type of obfusaction
    - Hides some of original data
- Protects PII
- May only be hidden from view
- Many techniques

**<u>Tokenization</u>**
- Replace sensitive data with non-sensitive placeholder
- Common with credit card processing
    - Temp token during payment
- Is not encryption or hashing

**<u>Masking</u>**
- Type of obfuscation
    - hides some of original data
- Protects pII
- May only be hidden from view
- Many techniques

**<u>Segmentation</u>**
- Many organizations use single data source
- One breach puts all data at risk
- Separate the data
- Sensitive data should have stronger security

**<u>Permission Restrictions</u>**
- Control access to account
    - More than just username and password
    - Determine what policies are best for organization
- Authentication process
- Permissions after login


### 3.4 - Resiliency
**<u>High Availability</u>**
- Redundancy doesnt always mean available
    - May need to be powered on manually
- HA (high availability)
    - Always on, always available
- May invlude many different components working together
    - Active/Active can provide scalability advantages
- Higher availability almost always means higher cost

**<u>Server Clustering</u>**
- COmbine two or more servers
    - Appears and operates asa single large server
    - Users only see one device
- Easily increase capacity and availibility (add more servers to the cluster)
- Usually configured in OS
    - All devices in cluster commonly use the same OS

**<u>Load Balancing</u>**
- Load is distributed across multiple servers
    - Servers often are unaware of eachother
    - Can be different OS setups or different OS entirely
- Load balancer adds or removes devices
    - Add server to increase capacity
    - Remove any servers not responding

**<u>Site Resiliency</u>**
- Recovery site is prepped
    - Data is syncronized
- Disaster is called
    - Business processes failover to the alternate processing site
- problem is addressed
    - Can take hours, weeks, or longer
- Revert back to primary locaiton

**<u>Hot site</u>**
- Exact replica of data cluster
    - Duplicate everything
- Stocked with ahrdware
    - Constantly updated, buying two of everything
- Applications and software are constantly updated
- Flip switch, everything moves

**<u>Cold-Site</u>**
- Empty building
- No data
- No people

**<u>Warm site</u>**
- Big rooom with rack space
- Somewhere in the middle

**<u>Platform Diversity</u>**
- Every OS has potential security issues
- Specific to single OS
- Use many different platforms
- All with different uses

**<u>Geographic Dispersion</u>**
- Sited should be physically different than organization's primary location
    - Many disruptions can affect large area
        - hurricane, tornado, floods, etc.
- Can be logistical challenge
    - transporting equipment
    - Employees

**<u>Multi-Cloud options</u>**
- Many cloud providers, use them
- Plan for cloud outages
- Both geographically dispersed and cloud-service dispersed

**<u>Continuity of Operations Planning (COOP)</u>**
- Not everything goes accordingly to plan, rely on computers
- Needs to be manual alternative


### 3.4 - Capacity Planning
**Capacity Planning** --> Match supply to the demand
- Too much demand
    - App shutdowns and outages
- Too much supply, paying too much
- Requires a balanced approach

**<u>People</u>**
- Some services require human intervention
- Too few employees
    - Takes time adding new stuff
    - Too many employees

**<u>Technology</u>**
- Pick technology that can scale
- Web services
    - distribute the load
- Database services
    - Cluster SBL servers
- Cloud services
    - Services on demand

**<u>Infrastructure</u>**
- The underlying framework
    - Applicatoin servers, network services
    - CPU, newtork, storage
- Physical devices
    - Purchase, configure, install
- Cloud based
    - Easier to deploy
    - Useful for unexpected capacity


### 3.2 - Recovery Testing
**Recovery Testing** --> Test yourself before an actual event
- Scheduled update sessions (annual, semi-annual, etc.)
- Use well-defined rules of engagement
- Very specific scenario
- Evaluate response

**<u>Table-Top Excercises</u>**
- Performing full-scale disaster drill can be costly
    - Many of logistics can be determined through analysis
- Get key players together for a table-top excercise

**<u>Fail-Over</u>**
- Failure is often inevitable
    - It's a when not if
- May be able to keep running (automatic)
- Create redundant infrastructure
- I fail, go to operating unit

**<u>Simulation</u>**
- Test with simulated event
- Going phishing
    - Create phishing email attack (simulation)
    - Test internal security
    - Test users

**<u>Parallel Processing</u>**
- Split process through miltiple (parallel) CPUs
    - Single computer with multiple CPU cores, or multiple physical CPUs
    - Multiple computers
- Improved performance
- Split complex transactions across multiple processors
- Improved recovery


### 3.4 - Backups
- Incredibly important
    - Recover easily and quickly lost data
    - lots of different variables
    - storage, media, type
    - Where? When?

**<u>On-site vs. Offsite backups</u>**
- On-site
    - No internet link, data immediately available
    - Generally less expensive than offsite
- Off-site
    - Transfer data over internet / WAN link
    - Data is available after disaster
    - Restoration can be prepared from anywhere
- Organizations often use both types
- More copies and more options

**<u>Frequency</u>**
- How often to backup
    - Every week, day, hour
- may be different between systems
- Multiple backup sets
- daily, weekly, monthly
- Requires significant planning

**<u>Encryption</u>**
- history of data is on backup media
    - Some media may be off-site
- Makes it easy for an attacker
- Protect backup data using encryption
    - Recovery key required
- Especially useful for cloud storage

**<u>Snapshots</u>**
- Popular on VMs
    - Useful in cloud
- Take a snapshot
    - Instant backup of entire system
- take a snapshot every day
    - Contains changes between snapshots

**<u>Recovery Testing</u>**
- Not enough to perform backup
    - Able to restore
- Disaster recovery testing
    - Simulate disaster and restore
- Confirm restoration
- Perform periodic audits

**<u>Replication</u>**
- An ongoing almost real-time backup
    - Synchronization in multiple locations
- data is available
    - Always copy somewhere
- Data is stored locally to all users
- data is recoverable
    - Disasters can happen at anytime

**<u>Journaling</u>**
- Power goes out while writing data to storaage
    - stored data probably corrupted
- Recover can be complicated
- Before writing to storage, make a journal entry
- After journal, write data to storage
- After data write to storage, change journal


### 3.4 - Power Resiliency
- Power is foundational to technology
    - Important to properly engineer and plan for outages
- Usually don;t make our own power
    - provided by a third party
    - Way to mitigate issues

**<u>Generators</u>**
- Long-term power backup
- Power an entire building
    - Some outlets marked
    - May take a few minutes

**<u>UPS</u>**
- Uninterrupted Power Supply
    - Short term backup power
    - Blackouts, brownouts, surges
- UPS types
    - Offline/standby
    - Line - interactive
    - On-line/double conversion
- Features
    - Auto shut-down, battery capacity outlets, phone like suppression