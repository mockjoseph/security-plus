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


    