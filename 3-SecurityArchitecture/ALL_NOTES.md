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




