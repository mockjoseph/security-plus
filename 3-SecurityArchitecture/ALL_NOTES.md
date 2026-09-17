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



