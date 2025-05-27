# Purpose #

The purpose of this document is to establish a standardized list of artifacts for evaluating the implementation of the Center for Internet Security’s (CIS) Critical Security Controls, in accordance with the CIS Controls Assessment Specification (CIS CAS). Derived directly from the CIS CAS, this list is provided to the assessment point of contact by Assessors prior to an assessment to allow sufficient time for the gathering of required artifacts.

# Scope #

Agency-owned information and systems, whether on-premises, in the cloud, or administered through a managed service provider. The CIS Safeguards assessed are selected from Implementation Groups 1 and 2 of Version 8 of the CIS Controls.

# Applicability #
The following requested artifacts are applicable to the CIS Version 8.0 Critical Security Controls, Implementation Group 1 (IG1), and constituent safeguards, as well as a select subset of controls and constituent safeguards from Implementation Group 2 (IG2) and Group 3 (IG3) for which there are Enterprise service offerings.

The artifacts listed below follow the guidance set forth by and applicable to the CIS CAS. The CIS CAS is intended to provide a common understanding of what should be measured to verify that CIS Safeguards are properly implemented.

# Artifact Request Guidance #

Artifacts may be submitted in any format such as Excel documents, Word documents, Visio Drawings in PDF or PNG format, screenshots, configuration files, Text files, CSV, or PDFs detailing the configuration settings of security systems.  Assessors find it very useful when agencies provide some type of narrative along with any artifacts, however this is not required.
It is important to note that if an artifact does not contain all the required information, it should still be summitted, as it will likely still have value to the assessment.

Each artifact request item below includes a section to indicate the artifact was provided or not, a text box to list the files provided to support the request, and a textbox to provide any additional details that would assist Assessors in reviewing the artifacts provided.
When submitting agency policies or procedures, please be sure the artifact contains a review date and authorized signature.

# Requested Artifacts #

## GV01: Detailed Hardware Asset Inventory ##

Maintaining an inventory of all hardware devices on the network helps to ensure that only authorized devices are permitted access to the network, and that unauthorized and unmanaged devices are located and denied access or promptly removed from the network. The purpose of the hardware asset inventory is to serve as the _*authoritative, single source of truth as the baseline against which output from active and passive discovery tools can be compared to look for deltas and to be able to efficiently identify devices that are not authorized. Output from hardware inventory tools alone does not constitute an authoritative hardware inventory. Hardware inventory tools enumerate software that is in the environment. The authorized hardware inventory defines what should be in the environment.*_

Additionally, the hardware inventory plays a critical role in configuration management, planning and executing system backup, incident response, and recovery.

The organization’s detailed inventory of all assets with the potential to receive, store, or process data. Data elements that the inventory should include, at a minimum:

- Hardware (MAC) address
- Machine name
- Asset owner
- Department
- Approval to connect to the network
- Date of last review or update to the inventory

The hardware asset inventory should include, at a minimum, the following types of devices:

- Workstations
- Servers
- Laptops
- Mobile devices (tablets, phones)
- Assets used for remote access (VPN)
- Assets used for administrative purposes (e.g. privileged-access workstations)
- Discovery/Vulnerability Scanners (i.e. Tenable.sc)

## GV03: Configuration Standards ##

Documented configuration standards will be used by assessors to validate implementation of select safeguards. For example, the CIS Controls Assessment Specification for Safeguard 1.3 – Utilize an Active Discovery Tool – requires that assessors review the configuration standard for the organization’s active discovery tool(s) to validate breadth of coverage for the tool(s) as well as to confirm that the tool(s) is / are configured to interface with the organization’s asset inventory to make automatic updates. The CIS CAS for Safeguard 4.9 requires that assessors review the organization's DNS configuration standard to validate that the organization is configuring its systems to leverage trusted DNS servers.

Examples of configuration standard submissions include, but are not limited to: Group Policy objects (GPOs), industry standard configuration baselines (CIS Benchmarks, IRS SCSEMs, DISA STIGs, USGCB, etc.), screen shots from tools that show the appropriate configuration settings, and output from command line tools or utilities.

Documented and approved Configuration Standard (e.g. Agency developed configuration standards, CIS Benchmarks, IRS SCSEMs, DISA STIGs, and USGCB) with a date of last review for the following:

- Operating systems and software
    - Workstations and servers
    - Mobile devices (Phones, Tablets, etc.)
    - Browsers
    - Microsoft 365
- Active discovery tools
    - Active discovery scan policy
    - Scan target list(s)
    - Bash script(s) used to automate discovery scan(s)
    - Nmap syntax used for discovery scan(s)
    - MASSCAN syntax used for discovery scan(s)
    - Timestamp(s) showing scan execution time
    - Any other applicable scan configuration artifacts to validate breadth and depth of scan coverage.
- Encryption software / mechanisms – for end-user devices
    - BitLocker encryption
    - Configuration standard for other encryption software in use
- DNS servers
    - Screen shot of DNS server configured forwarders showing enterprise “CAT” servers.
- Accounts on externally‐exposed applications
- Authorized remote access assets
- Account naming convention for regular, privileged and service accounts
- Administrative accounts 
- Automated patch management software / mechanisms
- Vulnerability scanners / scanning software
- Multi-factor authentication (MFA)
    - For administrative accounts (all accounts including DCS, on-premise Active Directory)
    - For remote network access

Agencies must provide documented deviations from any configuration baselines in use at the agency.

## GV05: Authorized Software Inventory ##

The purpose of the authorized software inventory is to serve as the authoritative, single source of truth as the baseline against which output from software discovery tools can be compared to look for deltas and to be able to efficiently identify software that is not authorized. Output from software inventory tools alone does not constitute an authoritative software inventory. Software inventory tools enumerate software that is in the environment. The authorized software inventory defines what should be in the environment.

Additionally, the software inventory helps to ensure that software running in the organizational environment is supported and receiving vendor updates, and that unnecessary software is not running on organizational devices, exposing the organization to unnecessary risk. The software inventory is also a necessary component for the organization to document and track exceptions for software that is beyond end-of-life and no longer supported but is necessary for the fulfilment of the organization’s mission and business purpose.

Detailed inventory of all licensed, and approved software installed on the organization’s assets. Data elements that the software inventory must document, at a minimum, include:

- Software title
-	Software publisher
-	Initial use or software approval date
-	business purpose
-	Software supported / unsupported
-	Date of last review & update

Software listed in the inventory should include, but is not limited to:

-	Authentication, Authorization, and accounting (AAA) Systems
-	Directory and SSO services
-	Authorized browsers
-	Authorized email clients
-	Authorized browser & email plugins
-	Authorized operating systems
-	Authorized anti‐malware software
-	Authorized patch management software
-	Authorized backup software
-	Authorized host‐based intrusion detection software
-	Authorized host‐based intrusion prevention software
-	802.1x authenticators
-	Application layer filtering software
-	Encryption software

## GV10: Organization's Data Management Process ##

Documented and approved process that describes how the organization ensures that data is collected, processed, stored, and disposed of in a secure and consistent manner.  This may or may not include agency information found in Oregon special records retention schedules.

The data management process must address, at a minimum:

-	Data sensitivity
-	Data ownership
-	Handling of data
-	Data retention limits
-	Disposal requirements based on data classification

## GV12: Sensitive Data Inventory ##
Documented and approved list that contains, at a minimum, all sensitive data that the organization generates, collects, or processes in pursuit of its mission and business purposes.  This may or may not include agency information found in Oregon special records retention schedules.

The organization’s inventory of sensitive information must include, at a minimum:

-	Date of last review and update to the data inventory
-	Data classification / sensitivity levels for each data set in the inventory (_Classification / sensitivity levels should be consistent with the organization’s data management process._)
-	Applicable data retention timeframes, consistent with the organization's data management process
-	Data owner(s) for each data set in the inventory
-	For each data set, mapping to assets storing the data (data storage location)

## GV18: Enterprise Assets Storing Sensitive Data ##

Provide an inventory of any system, applications, or databases within the agency that processes, transmits or stores sensitive data. Sensitive Data at minimum would be data classified at Level 3 or higher

## GV20: Unique Password Policy ##

The organization’s official policy dictating the minimum password construction and complexity requirements to be employed for password creation and use.

The unique password policy must address, at a minimum:

-	Prescriptive requirements for managing default accounts (e.g. disabling, changing default passwords for, etc.)
-	Strength of mechanism requirements for accounts (i.e. Password length, minimum and maximum password age, and password history)

## GV22: Inventory of Accounts ##

The purpose of the inventory of accounts is to serve as the authoritative, _*single source of truth as the baseline against which output from account inventory and management tools (e.g. Active Directory, PowerShell, etc.) can be compared to look for deltas*_ and to be able to efficiently identify accounts that are not authorized, accounts that are no longer necessary, and accounts that are no longer in use. _*Account inventory and management tools enumerate accounts that are in the environment. The account inventory defines what should be in the environment.*_ 

Documented inventory of all accounts authorized to access agency systems and components. 

The organization’s inventory of accounts must contain, at a minimum, all standard, service, and administrator accounts:
-	Account owner’s full name
-	Username
-	Start date
-	Stop date
-	Department
-	Date of last review and update to the inventory of accounts

Account types should include, but are not limited to:
- Domain account
    - Standard User
    - Administrator
    - Service Accounts
-	Local system user and or admin accounts
-	Database accounts
-	Internal application accounts
-	External application accounts

_*Output from account inventory and management tools alone does not constitute an authoritative inventory of accounts.*_

## GV24: Authorized Automated Patch Management Software ##

A list of all automated patch management software that the organization uses to perform application updates on organization software. Will be a subset of GV05 – Authorized Software Inventory and GV03 – Configuration Standards.

### GV25: List of Vulnerability Scanning Software ###

A list of all vulnerability scanning software that the organization uses to perform automated vulnerability scans of internal and external assets. Will be a subset of GV05 – Authorized Software Inventory and GV03 – Configuration Standards.

## GV26: Agency Audit Log Management Process ##

Documented and approved process that defines the enterprise’s logging requirements. The audit log management process must address, at a minimum:

-	Instructions for the collection of audit logs
-	Instructions for review of audit logs
-	Instructions for retention of audit logs
-	The date of last review and update to the audit log management process

## GV31: List of Authorized Anti‐malware Software ##

A list of all anti-malware software that the organization deploys on organization assets. Will be a subset of GV05 – Authorized Software Inventory and GV03 – Configuration Standards.

## GV43: List of Workforce Members ##

Organization’s list of current workforce members including all staff, volunteers, vendors, partners, etc.  Agencies may want to reach out to their local Workday coordinator to assist in obtaining this list.  The list should include at a minimum:

-	Full Name
-	Position
-	Start Date
-	Employee Classification (Full and Part Time Staff, Contractors, Vendors, Volunteers, etc.)

## GV44: Service Provider Inventory List ##

Formal, approved list of all external service providers, including vendors, suppliers, contractors, cloud service providers, and other third-party partners that the organization leverages for the maintenance and operation of the information technology that it uses in the fulfilment of its mission and business purpose.

The service provider inventory list should include, at a minimum, the following information:

-	Name of service provider
-	Security classification of the service provider
-	Agency contact for the service provider
-	Service Provider contact for the agency
-	The date of last review and update to the service provider inventory list

## GV51: Agency Incident Response Documentation ##

Organization’s approved, documented incident response plan or other incident response documentation that provides direction to organization personnel for incident response and recovery efforts.

Incident response documentation should include, at a minimum, the following information:

-	Documents dedicated personnel to manage incident handling:
    - Primary personnel
    - Backup personnel
    - Roles & responsibilities for primary personnel
    - Roles & responsibilities for backup personnel
-	Contact information for reporting security incidents
-	Process for reporting security incidents
    - Reporting timeframe
    - Personnel to report to
    - Mechanism for reporting
    - Minimum information to be reported in the event of a security incident
-	Date of last review & update to the incident response documentation

## GV54: Most Recent External Penetration Test Report for the Organization ##

Penetration testing is a security exercise where a cyber-security expert attempts to find and exploit vulnerabilities in a computer system. The purpose of this simulated attack is to identify any weaknesses in a system’s defenses which attackers could exploit.  Agencies may redact any information they do not wish to share with this assessment.

Penetration testing program characteristics include scope, such as network, web application, Application Programming Interface (API), hosted services, and physical premise controls; frequency; limitations, such as acceptable hours, and excluded attack types; point of contact information; remediation, such as how findings will be routed internally; and retrospective requirements.

