---
title: Indicator templates for controls
description: The Technology Controls Monitoring Accelerator includes 273 indicator templates \(94 Basic, 174 Manual, and 5 Scripted\) for CIS v7 and includes new 67 indicator templates \(64 Basic and 3 Scripted\) for CIS v8.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 61
breadcrumb: [Technology Controls Monitoring Accelerator, GRC use case accelerators, Common GRC features, Governance, Risk, and Compliance]
---

# Indicator templates for controls

The Technology Controls Monitoring Accelerator includes 273 indicator templates \(94 Basic, 174 Manual, and 5 Scripted\) for CIS v7 and includes new 67 indicator templates \(64 Basic and 3 Scripted\) for CIS v8.

When the Technology Controls Monitoring Accelerator is used along with the Cybersecurity Controls Accelerator application, you can manage indicator templates within the Cybersecurity Controls Accelerator application.

When Technology Controls Monitoring Accelerator is run as a standalone application; however, it can be run with the Policy and Compliance Management application. You can also [map UCF controls to indicator templates](../../grc-cybersec-controls/concept/cybersecurity-controls-accelerator.md#) from with the Policy and Compliance Management application.

**Note:** For information on the different types of indicator templates, see [Using indicator templates](../../grc-cybersec-controls/concept/using-indicator-templates.md).

## Indicator templates for CIS v8 Controls

The following table lists the indicator templates for CIS v8 Controls.

**Note:** Controls currently not covered by either basic or scripted indicator templates have manual indicator templates defined for the purposes of compliance validation. For more information on CIS v8 indicator templates, see [KB0555526](https://support.servicenow.com/nav_to.do?uri=/kb%3Fid=kb_article_view&sysparm_article=KB0555526).

<table id="table_d2"><thead><tr><th>

Control

</th><th>

Name/Description

</th><th>

Type

</th><th>

Compliance validated by

</th><th>

Source table

</th><th>

Related control objectives

</th></tr></thead><tbody><tr><td>

CIS Control V8 1.1

</td><td>

Establish and Maintain Detailed Enterprise Asset Inventory:

 Establish and maintain an accurate, detailed, and up-to-date inventory of all enterprise assets with the potential to store or process data, to include: end-user devices \(including portable and mobile\), network devices, non-computing/IoT devices, and servers. Ensure the inventory records the network address \(if static\), hardware address, machine name, data asset owner, department for each asset, and whether the asset has been approved to connect to the network. For mobile end-user devices, MDM type tools can support this process, where appropriate. This inventory includes assets connected to the infrastructure physically, virtually, remotely, and those within cloud environments. Additionally, it includes assets that are regularly connected to the enterprise’s network infrastructure, even if they are not under control of the enterprise. Review and update the inventory of all enterprise assets bi-annually, or more frequently.

</td><td>

BASIC

</td><td>

HAM

</td><td>

cmdb\_ci\_hardware

</td><td>

CIS v8 \(1.1\) CSF \(ID.AM-1, PR.DS-3\) ISO 27002 \(5.9, 8.8\) PCI \(9.5.1, 9.5.1.1, 11.2, 11.2.1, 11.2.2, 12.5, 12.5.1\) CCM \(UEM-04\)

</td></tr><tr><td>

CIS Control V8 1.2

</td><td>

Address Unauthorized Assets:

 Ensure that a process exists to address unauthorized assets on a weekly basis. The enterprise may choose to remove the asset from the network, deny the asset from connecting remotely to the network, or quarantine the asset.

</td><td>

BASIC

</td><td>

CMDB

</td><td>

cmdb\_ci

</td><td>

CIS v8 \(1.2\) NIST \(CM-8\) PCI \(11.2.1\)

</td></tr><tr><td>

CIS Control V8 1.3

</td><td>

Utilize an Active Discovery Tool:

 Utilize an active discovery tool to identify assets connected to the enterprise’s network. Configure the active discovery tool to execute daily, or more frequently.

</td><td>

BASIC

</td><td>

Discovery

</td><td>

cmdb\_discovery

</td><td>

CIS v8 \(1.3\) CSF \(DE.CM-7\) NIST \(CM-8\(1\)\) CCM \(UEM-05\)

</td></tr><tr><td>

CIS Control V8 1.4

</td><td>

Use Dynamic Host Configuration Protocol \(DHCP\) Logging to Update Enterprise Asset Inventory:

 Use DHCP logging on all DHCP servers or Internet Protocol \(IP\) address management tools to update the enterprise’s asset inventory. Review and use logs to update the enterprise’s asset inventory weekly, or more frequently.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 1.5

</td><td>

Use a Passive Asset Discovery Tool:

 Use a passive discovery tool to identify assets connected to the enterprise’s network. Review and use scans to update the enterprise’s asset inventory at least weekly, or more frequently.

</td><td>

BASIC

</td><td>

Discovery

</td><td>

discovery\_network\_track

</td><td>

CIS v8 \(1.5\) CSF \(DE.CM-7\) NIST \(CM-8\(3\)\)

</td></tr><tr><td>

CIS Control V8 2.1

</td><td>

Establish and Maintain a Software Inventory:

 Establish and maintain a detailed inventory of all licensed software installed on enterprise assets. The software inventory must document the title, publisher, initial install/use date, and business purpose for each entry; where appropriate, include the Uniform Resource Locator \(URL\), app store\(s\), version\(s\), deployment mechanism, and decommission date. Review and update the software inventory bi-annually, or more frequently.

</td><td>

BASIC

</td><td>

SAM

</td><td>

cmdb\_ci\_application\_software

</td><td>

CIS v8 \(2.1\) CSF \(ID.AM-2\) ISO \(5.9\) NIST \(SI-4\) PCI \(1.2.5, 6.3.2\) CCM \(UEM-02\)

</td></tr><tr><td>

CIS Control V8 2.2

</td><td>

Ensure Authorized Software is Currently Supported

 Ensure that only currently supported software is designated as authorized in the software inventory for enterprise assets. If software is unsupported, yet necessary for the fulfillment of the enterprise’s mission, document an exception detailing mitigating controls and residual risk acceptance. For any unsupported software without an exception documentation, designate as unauthorized. Review the software list to verify software support at least monthly, or more frequently.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 2.3

</td><td>

Address Unauthorized Software:

 Ensure that unauthorized software is either removed from use on enterprise assets or receives a documented exception. Review monthly, or more frequently.

</td><td>

SCRIPTED

</td><td>

SAM

</td><td>

cmdb\_sam\_sw\_install

</td><td>

CIS v8 \(2.3\) CSF \(DE.CM-7\) ISO \(8.7\) NIST \(CM-8\(3\)\) PCI \(12.3.4\)

</td></tr><tr><td>

CIS Control V8 2.4

</td><td>

Utilize Automated Software Inventory Tools:

 Utilize software inventory tools, when possible, throughout the enterprise to automate the discovery and documentation of installed software.

</td><td>

BASIC

</td><td>

SAM

</td><td>

cmdb\_ci\_application\_software

</td><td>

CIS v8 \(2.4\) CSF \(DE.CM-7\) NIST \(SI-4\)

</td></tr><tr><td>

CIS Control V8 2.5

</td><td>

Allowlist Authorized Software:

 Use technical controls, such as application allowlisting, to ensure that only authorized software can execute or be accessed. Reassess bi-annually, or more frequently.

</td><td>

SCRIPTED

</td><td>

SAM

</td><td>

cmdb\_sam\_sw\_install

</td><td>

CIS v8 \(2.5\) CSF \(DE.CM-7\) ISO \(8.7, 8.17\) PCI \(1.2.5, 2.2.4\)

</td></tr><tr><td>

CIS Control V8 2.6

</td><td>

Allowlist Authorized Libraries:

 Use technical controls to ensure that only authorized software libraries, such as specific .dll, .ocx, .so, etc., files, are allowed to load into a system process. Block unauthorized libraries from loading into a system process. Reassess bi-annually, or more frequently.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vulc\_result

</td><td>

CIS v8 \(2.6\) CSF \(DE.CM-7\) ISO \(8.19\) PCI \(1.2.5, 2.2.4\)

</td></tr><tr><td>

CIS Control V8 2.7

</td><td>

Allowlist Authorized Scripts:

 Use technical controls, such as digital signatures and version control, to ensure that only authorized scripts, such as specific .ps1, .py, etc., files, are allowed to execute. Block unauthorized scripts from executing. Reassess bi-annually, or more frequently.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vulc\_result

</td><td>

CIS v8 \(2.7\) CSF \(PR.IP-1, PR.PT-3\) NIST \(CM-8\) PCI \(1.2.5, 2.2.4, 6.4.3\)

</td></tr><tr><td>

CIS Control V8 3.1

</td><td>

Establish and Maintain a Data Management Process:

 Establish and maintain a data management process. In the process, address data sensitivity, data owner, handling of data, data retention limits, and disposal requirements, based on sensitivity and retention standards for the enterprise. Review and update documentation annually, or when significant enterprise changes occur that could impact this Safeguard.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 3.10

</td><td>

Encrypt Sensitive Data in Transit:

 Encrypt sensitive data in transit. Example implementations can include, Transport Layer Security \(TLS\) and Open Secure Shell \(OpenSSH\).

</td><td>

BASIC

</td><td>

Discovery

</td><td>

sn\_disco\_certmgmt\_cmdb\_installed\_certificate

</td><td>

CIS v8 \(3.10\) CSF \(PR.IP-6, PR.DS-2\) ISO \(5.1, 5.9, 8.1, 5.14\) NIST \(CM-7\(1\), CM-10\) PCI \(9.4, 9.4.2, 2.2.7, 4.1.1, 4.2.1, 4.2.1.2, 4.2.2, 8.3.2\) CCM \(DSP-01, DSP-06, GRC-03, CEK-03\)

</td></tr><tr><td>

CIS Control V8 3.11

</td><td>

Encrypt Sensitive Data At Rest:

 Encrypt sensitive data at rest on servers, applications, and databases containing sensitive data. Storage-layer encryption, also known as server-side encryption, meets the minimum requirement of this Safeguard. Additional encryption methods may include application-layer encryption, also known as client-side encryption, where access to the data storage device\(s\) does not permit access to the plain-text data.

</td><td>

BASIC

</td><td>

CMDB

</td><td>

cmdb\_rel\_ci

</td><td>

CIS v8 \(3.11\) CSF \(PR.DS-1\) ISO \(5.33\) NIST \(CM-7\) PCI \(3.1.1, 3.3.2, 3.3.3, 3.5.1, 3.5.1.2, 3.5.1.3, 8.3.2\) CCM \(DSP-10, CEK-03\)

</td></tr><tr><td>

CIS Control V8 3.12

</td><td>

Segment Data Processing and Storage Based on Sensitivity:

 Segment data processing and storage based on the sensitivity of the data. Do not process sensitive data on enterprise assets intended for lower sensitivity data.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 3.13

</td><td>

Deploy a Data Loss Prevention Solution:

 Implement an automated tool, such as a host-based Data Loss Prevention \(DLP\) tool to identify all sensitive data stored, processed, or transmitted through enterprise assets, including those located onsite or at a remote service provider, and update the enterprise's sensitive data inventory.

</td><td>

BASIC

</td><td>

CMDB

</td><td>

cmdb\_rel\_ci

</td><td>

CIS v8 \(3.13\) CSF \(PR.DS-5\) ISO \(5.13, 8.12\) NIST \(CM-7\) CCM \(DSP-10, UEM-11\)

</td></tr><tr><td>

CIS Control V8 3.14

</td><td>

Log Sensitive Data Access:

 Log sensitive data access, including modification and disposal.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vulc\_result

</td><td>

CIS v8 \(3.14\) ISO \(-8.15\) NIST \(CM-7\(1\)\) PCI \(10.2.1, 10.2.1.1\) CCM \(DSP-17, IAM-12, LOG-04\)

</td></tr><tr><td>

CIS Control V8 3.2

</td><td>

Establish and Maintain a Data Inventory:

 Establish and maintain a data inventory, based on the enterprise’s data management process. Inventory sensitive data, at a minimum. Review and update inventory annually, at a minimum, with a priority on sensitive data.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 3.3

</td><td>

Configure Data Access Control Lists:

 Configure data access control lists based on a user’s need to know. Apply data access control lists, also known as access permissions, to local and remote file systems, databases, and applications.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vulc\_result

</td><td>

CIS v8 \(3.3\) CSF \(PR.AC-4\) ISO \(5.1, 5.15, 8.3, 8.4\) NIST \(SA-22\) PCI \(1.3. 1, 7.1\) CCM \(DSP-17, IAM-05\)

</td></tr><tr><td>

CIS Control V8 3.4

</td><td>

Enforce Data Retention:

 Retain data according to the enterprise’s data management process. Data retention must include both minimum and maximum timelines.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 3.5

</td><td>

Securely Dispose of Data:

 Securely dispose of data as outlined in the enterprise’s data management process. Ensure the disposal process and method are commensurate with the data sensitivity.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 3.6

</td><td>

Encrypt Data on End-User Devices:

 Encrypt data on end-user devices containing sensitive data. Example implementations can include Windows BitLocker™, Apple FileVault™ , Linux dm-crypt™.

</td><td>

BASIC

</td><td>

CMDB

</td><td>

cmdb\_rel\_ci

</td><td>

CIS v8 \(3.6\) ISO \(6.7, 7.1, 8.1\) NIST \(CM-100\) CCM \(CEK-03, UEM-08\)

</td></tr><tr><td>

CIS Control V8 3.7

</td><td>

Establish and Maintain a Data Classification Scheme:

 Establish and maintain an overall data classification scheme for the enterprise. Enterprises may use labels, such as “Sensitive,” “Confidential,” and “Public,” and classify their data according to those labels. Review and update the classification scheme annually, or when significant enterprise changes occur that could impact this Safeguard.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 3.8

</td><td>

Document Data Flows:

 Document data flows. Data flow documentation includes service provider data flows and should be based on the enterprise’s data management process. Review and update documentation annually, or when significant enterprise changes occur that could impact this Safeguard.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 3.9

</td><td>

Encrypt Data on Removable Media:

 Encrypt data on removable media.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 4.1

</td><td>

Establish and Maintain a Secure Configuration Process:

 Establish and maintain a secure configuration process for enterprise assets \(end-user devices, including portable and mobile; non-computing/IoT devices; and servers\) and software \(operating systems and applications\). Review and update documentation annually, or when significant enterprise changes occur that could impact this Safeguard.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 4.10

</td><td>

Enforce Automatic Device Lockout on Portable End-User Devices:

 Enforce automatic device lockout following a predetermined threshold of local failed authentication attempts on portable end-user devices, where supported. For laptops, do not allow more than 20 failed authentication attempts; for tablets and smartphones, no more than 10 failed authentication attempts. Example implementations include Microsoft InTune Device Lock and Apple Configuration Profile maxFailedAttempts.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vulc\_result

</td><td>

CIS v8 \(4.10\) CSF \(PR.IP-1\) ISO \(8.1, 8.5, 8.9\) NIST \(SI-7, PM-5\(1\)\) PCI \(1.1.1, 1.2.1, 1.2.6, 1.5.1, 1.2.7, 2.1.1, 2.2.1, 8.3.4\) CCM \(CCC-01, GRC-03, IVS-04\)

</td></tr><tr><td>

CIS Control V8 4.11

</td><td>

Enforce Remote Wipe Capability on Portable End-User Devices:

 Remotely wipe enterprise data from enterprise-owned portable end-user devices when deemed appropriate such as lost or stolen devices, or when an individual no longer supports the enterprise.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 4.12

</td><td>

Separate Enterprise Workspaces on Mobile End-User Devices:

 Ensure separate enterprise workspaces are used on mobile end-user devices, where supported. Example implementations include using an Apple Configuration Profile or Android Work Profile to separate enterprise applications and data from personal applications and data.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 4.2

</td><td>

Establish and Maintain a Secure Configuration Process for Network Infrastructure:

 Establish and maintain a secure configuration process for network devices. Review and update documentation annually, or when significant enterprise changes occur that could impact this Safeguard.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 4.3

</td><td>

Configure Automatic Session Locking on Enterprise Assets:

 Configure automatic session locking on enterprise assets after a defined period of inactivity. For general purpose operating systems, the period must not exceed 15 minutes. For mobile end-user devices, the period must not exceed 2 minutes.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vulc\_result

</td><td>

CIS v8 \(4.3\) CSF \(PR.IP-1\) ISO \(8.5, 8.9\) PCI \(8.2.8\) CCM \(UEM-06\)

</td></tr><tr><td>

CIS Control V8 4.4

</td><td>

Implement and Manage a Firewall on Servers:

 Implement and manage a firewall on servers, where supported. Example implementations include a virtual firewall, operating system firewall, or a third-party firewall agent.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vulc\_result

</td><td>

CIS v8 \(4.4\) PCI \(1.2.1, 1.4.1\)

</td></tr><tr><td>

CIS Control V8 4.5

</td><td>

Implement and Manage a Firewall on End-User Devices:

 Implement and manage a host-based firewall or port-filtering tool on end-user devices, with a default-deny rule that drops all traffic except those services and ports that are explicitly allowed.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 4.6

</td><td>

Securely Manage Enterprise Assets and Software:

 Securely manage enterprise assets and software. Example implementations include managing configuration through version-controlled-infrastructure-as-code and accessing administrative interfaces over secure network protocols, such as Secure Shell \(SSH\) and Hypertext Transfer Protocol Secure \(HTTPS\). Do not use insecure management protocols, such as Telnet \(Teletype Network\) and HTTP, unless operationally essential.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 4.7

</td><td>

Manage Default Accounts on Enterprise Assets and Software:

 Manage default accounts on enterprise assets and software, such as root, administrator, and other pre-configured vendor accounts. Example implementations can include: disabling default accounts or making them unusable.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vulc\_result

</td><td>

CIS v8 \(4.7\) CSF \(PR.AC-1\) ISO \(8.2, 8.9\) NIST \(SI-12\) PCI \(2.2.2, 2.3.1\)

</td></tr><tr><td>

CIS Control V8 4.8

</td><td>

Uninstall or Disable Unnecessary Services on Enterprise Assets and Software:

 Uninstall or disable unnecessary services on enterprise assets and software, such as an unused file sharing service, web application module, or service function.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 4.9

</td><td>

Configure Trusted DNS Servers on Enterprise Assets:

 Configure trusted DNS servers on enterprise assets. Example implementations include: configuring assets to use enterprise-controlled DNS servers and/or reputable externally accessible DNS servers.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vulc\_result

</td><td>

CIS v8 \(4.9\) NIST \(PM-5\(1\)\)

</td></tr><tr><td>

CIS Control V8 5.1

</td><td>

Establish and Maintain an Inventory of Accounts:

 Establish and maintain an inventory of all accounts managed in the enterprise. The inventory must include both user and administrator accounts. The inventory, at a minimum, should contain the person’s name, username, start/stop dates, and department. Validate that all active accounts are authorized, on a recurring schedule at a minimum quarterly, or more frequently.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 5.2

</td><td>

Use Unique Passwords:

 Use unique passwords for all enterprise assets. Best practice implementation includes, at a minimum, an 8-character password for accounts using MFA and a 14-character password for accounts not using MFA.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vulc\_result

</td><td>

CIS v8 \(5.2\) ISO \(5.17\) NIST \(AC-5\) PCI \(2.2.2, 8.3.5, 8.5.6, 8.6.3\) CCM \(IAM-02\)

</td></tr><tr><td>

CIS Control V8 5.3

</td><td>

Disable Dormant Accounts:

 Delete or disable any dormant accounts after a period of 45 days of inactivity, where supported.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 5.4

</td><td>

Restrict Administrator Privileges to Dedicated Administrator Accounts:

 Restrict administrator privileges to dedicated administrator accounts on enterprise assets. Conduct general computing activities, such as internet browsing, email, and productivity suite use, from the user’s primary, non-privileged account.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 5.5

</td><td>

Establish and Maintain an Inventory of Service Accounts:

 Establish and maintain an inventory of service accounts. The inventory, at a minimum, must contain department owner, review date, and purpose. Perform service account reviews to validate all active accounts are authorized, on a recurring schedule at a minimum quarterly, or more frequently.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 5.6

</td><td>

Centralize Account Management:

 Centralize account management through a directory or identity service.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 6.1

</td><td>

Establish an Access Granting Process:

 Establish and follow a process, preferably automated, for granting access to enterprise assets upon new hire, rights grant, or role change of a user.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 6.2

</td><td>

Establish an Access Revoking Process:

 Establish and follow a process, preferably automated, for revoking access to enterprise assets, through disabling accounts immediately upon termination, rights revocation, or role change of a user. Disabling accounts, instead of deleting accounts, may be necessary to preserve audit trails.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 6.3

</td><td>

Require MFA for Externally-Exposed Applications:

 Require all externally-exposed enterprise or third-party applications to enforce MFA, where supported. Enforcing MFA through a directory service or SSO provider is a satisfactory implementation of this Safeguard.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 6.4

</td><td>

Require MFA for Remote Network Access:

 Require MFA for remote network access.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 6.5

</td><td>

Require MFA for Administrative Access:

 Require MFA for all administrative access accounts, where supported, on all enterprise assets, whether managed on-site or through a third-party provider.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 6.6

</td><td>

Establish and Maintain an Inventory of Authentication and Authorization Systems:

 Establish and maintain an inventory of the enterprise’s authentication and authorization systems, including those hosted on-site or at a remote service provider. Review and update the inventory, at a minimum, annually, or more frequently.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 6.7

</td><td>

Centralize Access Control:

 Centralize access control for all enterprise assets through a directory service or SSO provider, where supported.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 6.8

</td><td>

Define and Maintain Role-Based Access Control:

 Define and maintain role-based access control, through determining and documenting the access rights necessary for each role within the enterprise to successfully carry out its assigned duties. Perform access control reviews of enterprise assets to validate that all privileges are authorized, on a recurring schedule at a minimum annually, or more frequently.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 7.1

</td><td>

Establish and Maintain a Vulnerability Management Process:

 Establish and maintain a documented vulnerability management process for enterprise assets. Review and update documentation annually, or when significant enterprise changes occur that could impact this Safeguard.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 7.2

</td><td>

Establish and Maintain a Remediation Process:

 Establish and maintain a risk-based remediation strategy documented in a remediation process, with monthly, or more frequent, reviews.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vul\_m2m\_ttr\_status

</td><td>

CIS v8 \(7.2\) CSF \(ID.RA-1\) ISO \(8.8\) NIST \(IA-5\) PCI \(6.3.1, 6.4.1\) CCM \(A&amp;A-03, TVM-08, TVM-10\)

</td></tr><tr><td>

CIS Control V8 7.3

</td><td>

Perform Automated Operating System Patch Management:

 Perform operating system updates on enterprise assets through automated patch management on a monthly, or more frequent, basis.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 7.4

</td><td>

Perform Automated Application Patch Management:

 Perform application updates on enterprise assets through automated patch management on a monthly, or more frequent, basis.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 7.5

</td><td>

Perform Automated Vulnerability Scans of Internal Enterprise Assets:

 Perform automated vulnerability scans of internal enterprise assets on a quarterly, or more frequent, basis. Conduct both authenticated and unauthenticated scans, using a SCAP-compliant vulnerability scanning tool.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vul\_ds\_import\_q\_entry

</td><td>

CIS v8 \(7.5\) CSF \(DE.CM-8\) ISO \(8.8\) NIST \(SC-8\(1\)\) PCI \(11.3.1, 11.3.1.1, 11.3.1.2, 11.3.1.3\) CCM \(TVM-07\)

</td></tr><tr><td>

CIS Control V8 7.6

</td><td>

Perform Automated Vulnerability Scans of Externally-Exposed Enterprise Assets:

 Perform automated vulnerability scans of externally-exposed enterprise assets using a SCAP-compliant vulnerability scanning tool. Perform scans on a monthly, or more frequent, basis.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vul\_ds\_import\_q\_entry

</td><td>

 

</td></tr><tr><td>

CIS Control V8 7.7

</td><td>

Remediate Detected Vulnerabilities:

 Remediate detected vulnerabilities in software through processes and tooling on a monthly, or more frequent, basis, based on the remediation process.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vul\_app\_vulnerability

</td><td>

CIS v8 \(7.7\) ISO \(8.8\) NIST \(SC-28\) PCI \(11.3.1, 11.3.2, 11.3.2.1\) CCM \(TVM-03\)

</td></tr><tr><td>

CIS Control V8 8.1

</td><td>

Establish and Maintain an Audit Log Management Process:

 Establish and maintain an audit log management process that defines the enterprise’s logging requirements. At a minimum, address the collection, review, and retention of audit logs for enterprise assets. Review and update documentation annually, or when significant enterprise changes occur that could impact this Safeguard.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 8.1

</td><td>

Retain Audit Logs:

 Retain audit logs across enterprise assets for a minimum of 90 days.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 8.11

</td><td>

Conduct Audit Log Reviews:

 Conduct reviews of audit logs to detect anomalies or abnormal events that could indicate a potential threat. Conduct reviews on a weekly, or more frequent, basis.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 8.12

</td><td>

Collect Service Provider Logs:

 Collect service provider logs, where supported. Example implementations include collecting authentication and authorization events, data creation and disposal events, and user management events.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 8.2

</td><td>

Collect Audit Logs:

 Collect audit logs. Ensure that logging, per the enterprise’s audit log management process, has been enabled across enterprise assets.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vulc\_result

</td><td>

CIS v8 \(8.2\) CSF \(PR.PT-1, DE.AE-3\) ISO \(8.15, 8.2\) PCI \(5.3.4, 6.4.1, 6.4.2, 10.2.1, 10.2.1.1, 10.2.1.2, 10.2.1.3, 10.2.1.4, 10.2.1.5, 10.2.1.6, 10.2.1.7, 10.2.2\) CCM \(LOG-08\)

</td></tr><tr><td>

CIS Control V8 8.3

</td><td>

Ensure Adequate Audit Log Storage:

 Ensure that logging destinations maintain adequate storage to comply with the enterprise’s audit log management process.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 8.4

</td><td>

Standardize Time Synchronization:

 Standardize time synchronization. Configure at least two synchronized time sources across enterprise assets, where supported.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 8.5

</td><td>

Collect Detailed Audit Logs:

 Configure detailed audit logging for enterprise assets containing sensitive data. Include event source, date, username, timestamp, source addresses, destination addresses, and other useful elements that could assist in a forensic investigation.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 8.6

</td><td>

Collect DNS Query Audit Logs:

 Collect DNS query audit logs on enterprise assets, where appropriate and supported.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 8.7

</td><td>

Collect URL Request Audit Logs:

 Collect URL request audit logs on enterprise assets, where appropriate and supported.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 8.8

</td><td>

Collect Command-Line Audit Logs:

 Collect command-line audit logs. Example implementations include collecting audit logs from PowerShell™, BASH™, and remote administrative terminals.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 8.9

</td><td>

Centralize Audit Logs:

 Centralize, to the extent possible, audit log collection and retention across enterprise assets.

</td><td>

BASIC

</td><td>

CMDB

</td><td>

cmdb\_ci

</td><td>

CIS v8 \(8.9\) NIST \(AU-12\) PCI \(10.3.3\)

</td></tr><tr><td>

CIS Control V8 9.1

</td><td>

Ensure Use of Only Fully Supported Browsers and Email Clients:

 Ensure only fully supported browsers and email clients are allowed to execute in the enterprise, only using the latest version of browsers and email clients provided through the vendor.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vulc\_result

</td><td>

CIS v8 \(9.1\) CSF \(PR.IP-1\) ISO \(8.1\) NIST \(CM-2\)

</td></tr><tr><td>

CIS Control V8 9.2

</td><td>

Use DNS Filtering Services:

 Use DNS filtering services on all enterprise assets to block access to known malicious domains.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 9.3

</td><td>

Maintain and Enforce Network-Based URL Filters:

 Enforce and update network-based URL filters to limit an enterprise asset from connecting to potentially malicious or unapproved websites. Example implementations include category-based filtering, reputation-based filtering, or through the use of block lists. Enforce filters for all enterprise assets.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vulc\_result

</td><td>

CIS v8 \(9.3\) CSF \(PR.AC-5\) ISO \(8.7, 8.23\) NIST \(CM-7\) PCI \(1.2.6, 1.4.2\)

</td></tr><tr><td>

CIS Control V8 9.4

</td><td>

Restrict Unnecessary or Unauthorized Browser and Email Client Extensions:

 Restrict, either through uninstalling or disabling, any unauthorized or unnecessary browser or email client plugins, extensions, and add-on applications.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vulc\_result

</td><td>

CIS v8 \(9.4\) CSF \(PR.IP-1\) NIST \(CM-7\(1\)\) PCI \(2.2.4\)

</td></tr><tr><td>

CIS Control V8 9.5

</td><td>

Implement DMARC:

 To lower the chance of spoofed or modified emails from valid domains, implement DMARC policy and verification, starting with implementing the Sender Policy Framework \(SPF\) and the DomainKeys Identified Mail \(DKIM\) standards.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 9.6

</td><td>

Block Unnecessary File Types:

 Block unnecessary file types attempting to enter the enterprise’s email gateway.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 9.7

</td><td>

Deploy and Maintain Email Server Anti-Malware Protections:

 Deploy and maintain email server anti-malware protections, such as attachment scanning and/or sandboxing.

</td><td>

BASIC

</td><td>

CMDB

</td><td>

cmdb\_rel\_ci

</td><td>

CIS v8 \(9.7\) CSF \(DE.CM-4\) ISO \(8.7\) NIST \(SA-80\) PCI \(5.2.1, 5.4.1\) CCM \(TVM-02\)

</td></tr><tr><td>

CIS Control V8 10.1

</td><td>

Deploy and Maintain Anti-Malware Software:

 Deploy and maintain anti-malware software on all enterprise assets.

</td><td>

BASIC

</td><td>

CMDB

</td><td>

cmdb\_ci

</td><td>

CIS v8 \(10.1\) CSF \(DE.CM-4\) ISO \(8.1, 8.7\) NIST \(SA-10\) PCI \(5.1.1, 5.2.1, 5.2.2, 5.3.2\) CCM \(TVM-02, UEM-09\)

</td></tr><tr><td>

CIS Control V8 10.2

</td><td>

Configure Automatic Anti-Malware Signature Updates:

 Configure automatic updates for anti-malware signature files on all enterprise assets.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 10.3

</td><td>

Disable Autorun and Autoplay for Removable Media:

 Disable autorun and autoplay auto-execute functionality for removable media.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vulc\_result

</td><td>

CIS v8 \(10.3\) CSF \(PR.PT-2\) ISO \(7.1\) NIST \(AC-18\(1\)\)

</td></tr><tr><td>

CIS Control V8 10.4

</td><td>

Configure Automatic Anti-Malware Scanning of Removable Media:

 Configure anti-malware software to automatically scan removable media.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vulc\_result

</td><td>

CIS v8 \(10.4\) CSF \(DE.CM-4\) ISO \(7.1, 8.7\) NIST \(AC-18\(3\)\) PCI \(5.3.3\)

</td></tr><tr><td>

CIS Control V8 10.5

</td><td>

Enable Anti-Exploitation Features:

 Enable anti-exploitation features on enterprise assets and software, where possible, such as Microsoft Data Execution Prevention \(DEP\), Windows Defender Exploit Guard \(WDEG\), or Apple System Integrity Protection \(SIP\) and Gatekeeper™.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vulc\_result

</td><td>

CIS v8 \(10.5\) CSF \(DE.CM-4\) ISO \(8.7\) NIST \(CM-2\)

</td></tr><tr><td>

CIS Control V8 10.6

</td><td>

Centrally Manage Anti-Malware Software:

 Centrally manage anti-malware software.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 10.7

</td><td>

Use Behavior-Based Anti-Malware Software:

 Use behavior-based anti-malware software.

</td><td>

BASIC

</td><td>

CMDB

</td><td>

cmdb\_rel\_ci

</td><td>

CIS v8 \(10.7\) CSF \(DE.CM-4\) ISO \(8.1, 8.7\) NIST \(CM-7\) PCI \(5.3.2\)

</td></tr><tr><td>

CIS Control V8 11.1

</td><td>

Establish and Maintain a Data Recovery Process :

 Establish and maintain a data recovery process. In the process, address the scope of data recovery activities, recovery prioritization, and the security of backup data. Review and update documentation annually, or when significant enterprise changes occur that could impact this Safeguard.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 11.2

</td><td>

Perform Automated Backups :

 Perform automated backups of in-scope enterprise assets. Run backups weekly, or more frequently, based on the sensitivity of the data.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 11.3

</td><td>

Protect Recovery Data:

 Protect recovery data with equivalent controls to the original data. Reference encryption or data separation, based on requirements.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 11.4

</td><td>

Establish and Maintain an Isolated Instance of Recovery Data :

 Establish and maintain an isolated instance of recovery data. Example implementations include version controlling backup destinations through offline, cloud, or off-site systems or services.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 11.5

</td><td>

Test Data Recovery:

 Test backup recovery quarterly, or more frequently, for a sampling of in-scope enterprise assets.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 12.1

</td><td>

Ensure Network Infrastructure is Up-to-Date:

 Ensure network infrastructure is kept up-to-date. Example implementations include running the latest stable release of software and/or using currently supported network-as-a-service \(NaaS\) offerings. Review software versions monthly, or more frequently, to verify software support.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 12.2

</td><td>

Establish and Maintain a Secure Network Architecture:

 Establish and maintain a secure network architecture. A secure network architecture must address segmentation, least privilege, and availability, at a minimum.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 12.3

</td><td>

Securely Manage Network Infrastructure:

 Securely manage network infrastructure. Example implementations include version-controlled-infrastructure-as-code, and the use of secure network protocols, such as SSH and HTTPS.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 12.4

</td><td>

Establish and Maintain Architecture Diagram\(s\):

 Establish and maintain architecture diagram\(s\) and/or other network system documentation. Review and update documentation annually, or when significant enterprise changes occur that could impact this Safeguard.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 12.5

</td><td>

Centralize Network Authentication, Authorization, and Auditing \(AAA\):

 Centralize network AAA.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 12.6

</td><td>

Use of Secure Network Management and Communication Protocols :

 Use secure network management and communication protocols \(e.g., 802.1X, Wi-Fi Protected Access 2 \(WPA2\) Enterprise or greater\).

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vulc\_result

</td><td>

CIS v8 \(12.6\) CSF \(PR.AC-7, PR.DS-2\) ISO \(8.21\) NIST \(SC-7\(5\)\)

</td></tr><tr><td>

CIS Control V8 12.7

</td><td>

Ensure Remote Devices Utilize a VPN and are Connecting to an Enterprise’s AAA Infrastructure:

 Require users to authenticate to enterprise-managed VPN and authentication services prior to accessing enterprise resources on end-user devices.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 12.8

</td><td>

Establish and Maintain Dedicated Computing Resources for All Administrative Work:

 Establish and maintain dedicated computing resources, either physically or logically separated, for all administrative tasks or tasks requiring administrative access. The computing resources should be segmented from the enterprise's primary network and not be allowed internet access.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 13.1

</td><td>

Centralize Security Event Alerting:

 Centralize security event alerting across enterprise assets for log correlation and analysis. Best practice implementation requires the use of a SIEM, which includes vendor-defined event correlation alerts. A log analytics platform configured with security-relevant correlation alerts also satisfies this Safeguard.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 13.1

</td><td>

Perform Application Layer Filtering:

 Perform application layer filtering. Example implementations include a filtering proxy, application layer firewall, or gateway.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 13.11

</td><td>

Tune Security Event Alerting Thresholds:

 Tune security event alerting thresholds monthly, or more frequently.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 13.2

</td><td>

Deploy a Host-Based Intrusion Detection Solution:

 Deploy a host-based intrusion detection solution on enterprise assets, where appropriate and/or supported.

</td><td>

BASIC

</td><td>

CMDB

</td><td>

cmdb\_rel\_ci

</td><td>

CIS v8 \(13.2\) CSF \(DE.CM-1\) ISO \(8.16\) NIST \(CM-6\) PCI \(6.4.2\)

</td></tr><tr><td>

CIS Control V8 13.3

</td><td>

Deploy a Network Intrusion Detection Solution:

 Deploy a network intrusion detection solution on enterprise assets, where appropriate. Example implementations include the use of a Network Intrusion Detection System \(NIDS\) or equivalent cloud service provider \(CSP\) service.

</td><td>

BASIC

</td><td>

CMDB

</td><td>

cmdb\_ci

</td><td>

CIS v8 \(13.3\) CSF \(DE.CM-1\) ISO \(8.16, 8.21\) NIST \(CM-7\) PCI \(11.5.1, 12.10.5\) CCM \(IVS-09\)

</td></tr><tr><td>

CIS Control V8 13.4

</td><td>

Perform Traffic Filtering Between Network Segments:

 Perform traffic filtering between network segments, where appropriate.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 13.5

</td><td>

Manage Access Control for Remote Assets:

 Manage access control for assets remotely connecting to enterprise resources. Determine amount of access to enterprise resources based on: up-to-date anti-malware software installed; configuration compliance with the enterprise’s secure configuration process; and ensuring the operating system and applications are up-to-date.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 13.6

</td><td>

Collect Network Traffic Flow Logs:

 Collect network traffic flow logs and/or network traffic to review and alert upon from network devices.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 13.7

</td><td>

Deploy a Host-Based Intrusion Prevention Solution:

 Deploy a host-based intrusion prevention solution on enterprise assets, where appropriate and/or supported. Example implementations include use of an Endpoint Detection and Response \(EDR\) client or host-based IPS agent.

</td><td>

BASIC

</td><td>

CMDB

</td><td>

cmdb\_ci

</td><td>

CIS v8 \(13.7\) CSF \(DE.CM-1\) ISO \(8.8\) NIST \(AC-7\)

</td></tr><tr><td>

CIS Control V8 13.8

</td><td>

Deploy a Network Intrusion Prevention Solution:

 Deploy a network intrusion prevention solution, where appropriate. Example implementations include the use of a Network Intrusion Prevention System \(NIPS\) or equivalent CSP service.

</td><td>

BASIC

</td><td>

CMDB

</td><td>

cmdb\_ci

</td><td>

CIS v8 \(13.8\) CSF \(DE.CM-1\) ISO \(8.8\) NIST \(AC-19\) PCI \(6.4.2, 11.5.1, 12.10.5\) CCM \(IVS-09\)

</td></tr><tr><td>

CIS Control V8 13.9

</td><td>

Deploy Port-Level Access Control:

 Deploy port-level access control. Port-level access control utilizes 802.1x, or similar network access control protocols, such as certificates, and may incorporate user and/or device authentication.

</td><td>

BASIC

</td><td>

CMDB

</td><td>

cmdb\_ci\_endpoint\_acl

</td><td>

CIS v8 \(13.9\) CSF \(PR.AC-1\) ISO \(8.8\) NIST \(AC-19\) PCI \(1.2.1, 1.2.5, 1.2.6, 2.2.4\) CCM \(IVS-03\)

</td></tr><tr><td>

CIS Control V8 14.1

</td><td>

Establish and Maintain a Security Awareness Program:

 Establish and maintain a security awareness program. The purpose of a security awareness program is to educate the enterprise’s workforce on how to interact with enterprise assets and data in a secure manner. Conduct training at hire and, at a minimum, annually. Review and update content annually, or when significant enterprise changes occur that could impact this Safeguard.

</td><td>

BASIC

</td><td>

Learning Core

</td><td>

sn\_lc\_user\_course\_activity

</td><td>

CIS v8 \(14.1\) CSF \(ID.AM-6, ID.GV-1, PR.AT-1\) ISO \(6.3\) NIST \(SC-39\) PCI \(12.6, 12.6.1, 12.6.2, 12.6.3, 12.6.3.2\) CCM \(GRC-05, HRS-11, GRC-03\)

</td></tr><tr><td>

CIS Control V8 14.2

</td><td>

Train Workforce Members to Recognize Social Engineering Attacks:

 Train workforce members to recognize social engineering attacks, such as phishing, pre-texting, and tailgating. 

</td><td>

BASIC

</td><td>

Learning Core

</td><td>

sn\_lc\_user\_course\_activity

</td><td>

CIS v8 \(14.2\) CSF \(PR.AT-1\) ISO \(8.7\) PCI \(12.6.3.1\) CCM \(HRS-11\)

</td></tr><tr><td>

CIS Control V8 14.3

</td><td>

Train Workforce Members on Authentication Best Practices:

 Train workforce members on authentication best practices. Example topics include MFA, password composition, and credential management.

</td><td>

BASIC

</td><td>

Learning Core

</td><td>

sn\_lc\_user\_course\_activity

</td><td>

CIS v8 \(14.3\) CSF \(PR.AT-1\) ISO \(6.3\) PCI \(8.3.8\) CCM \(GRC-05, HRS-11\)

</td></tr><tr><td>

CIS Control V8 14.4

</td><td>

Train Workforce on Data Handling Best Practices:

 Train workforce members on how to identify and properly store, transfer, archive, and destroy sensitive data. This also includes training workforce members on clear screen and desk best practices, such as locking their screen when they step away from their enterprise asset, erasing physical and virtual whiteboards at the end of meetings, and storing data and assets securely.

</td><td>

BASIC

</td><td>

Learning Core

</td><td>

sn\_lc\_user\_course\_activity

</td><td>

CIS v8 \(14.4\) CSF \(PR.AT-1\) ISO \(5.1\) NIST \(AC-2\) CCM \(DSP-17, GRC-01, HRS-03, HRS-12\)

</td></tr><tr><td>

CIS Control V8 14.5

</td><td>

Train Workforce Members on Causes of Unintentional Data Exposure:

 Train workforce members to be aware of causes for unintentional data exposure. Example topics include mis-delivery of sensitive data, losing a portable end-user device, or publishing data to unintended audiences.

</td><td>

BASIC

</td><td>

Learning Core

</td><td>

sn\_lc\_user\_course\_activity

</td><td>

CIS v8 \(14.5\) CSF \(PR.AT-1\) ISO \(6.3\) NIST \(IA-5\(1\)\) CCM \(GRC-01, HRS-11\)

</td></tr><tr><td>

CIS Control V8 14.6

</td><td>

Train Workforce Members on Recognizing and Reporting Security Incidents:

 Train workforce members to be able to recognize a potential incident and be able to report such an incident. 

</td><td>

BASIC

</td><td>

Learning Core

</td><td>

sn\_lc\_user\_course\_activity

</td><td>

CIS v8 \(14.6\) CSF \(PR.AT-1\) ISO \(6.8\) NIST \(AC-2\(3\)\) CCM \(HRS-11\)

</td></tr><tr><td>

CIS Control V8 14.7

</td><td>

Train Workforce on How to Identify and Report if Their Enterprise Assets are Missing Security Updates:

 Train workforce to understand how to verify and report out-of-date software patches or any failures in automated processes and tools. Part of this training should include notifying IT personnel of any failures in automated processes and tools.

</td><td>

BASIC

</td><td>

Learning Core

</td><td>

sn\_lc\_user\_course\_activity

</td><td>

CIS v8 \(14.7\) CSF \(PR.AT-1\) ISO \(6.3\) NIST \(AC-6\(2\)\) CCM \(HRS-11\)

</td></tr><tr><td>

CIS Control V8 14.8

</td><td>

Train Workforce on the Dangers of Connecting to and Transmitting Enterprise Data Over Insecure Networks:

 Train workforce members on the dangers of connecting to, and transmitting data over, insecure networks for enterprise activities. If the enterprise has remote workers, training must include guidance to ensure that all users securely configure their home network infrastructure.

</td><td>

BASIC

</td><td>

Learning Core

</td><td>

sn\_lc\_user\_course\_activity

</td><td>

CIS v8 \(14.8\) CSF \(PR.AT-1\) ISO \(6.3\) NIST \(AC-6\(5\)\) PCI \(12.6.3.2\) CCM \(GRC-01, HRS-04\)

</td></tr><tr><td>

CIS Control V8 14.9

</td><td>

Conduct Role-Specific Security Awareness and Skills Training:

 Conduct role-specific security awareness and skills training. Example implementations include secure system administration courses for IT professionals, \(OWASP ™ Top 10 vulnerability awareness and prevention training for web application developers, and advanced social engineering awareness training for high-profile roles.

</td><td>

BASIC

</td><td>

Learning Core

</td><td>

sn\_lc\_user\_course\_activity

</td><td>

CIS v8 \(14.9\) CSF \(PR.AT-1, PR.AT-2, R.AT-4, PR.AT-5\) ISO \(6.3\) NIST \(AC-2\) PCI \(9.5.1, 9.5.1.3, 12.10.40 CCM \(HRS-09, HRS-12\)

</td></tr><tr><td>

CIS Control V8 15.1

</td><td>

Establish and Maintain an Inventory of Service Providers:

 Establish and maintain an inventory of service providers. The inventory is to list all known service providers, include classification\(s\), and designate an enterprise contact for each service provider. Review and update the inventory annually, or when significant enterprise changes occur that could impact this Safeguard.

</td><td>

BASIC

</td><td>

VRM

</td><td>

core\_company

</td><td>

CIS v8 \(15.1\) CSF \(ID.SC-2\) ISO \(5.19\) NIST \(AC-2\(1\)\) PCI \(12.8.1\) CCM \(STA-07\)

</td></tr><tr><td>

CIS Control V8 15.2

</td><td>

Establish and Maintain a Service Provider Management Policy:

 Establish and maintain a service provider management policy. Ensure the policy addresses the classification, inventory, assessment, monitoring, and decommissioning of service providers. Review and update the policy annually, or when significant enterprise changes occur that could impact this Safeguard.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 15.3

</td><td>

Classify Service Providers:

 Classify service providers. Classification consideration may include one or more characteristics, such as data sensitivity, data volume, availability requirements, applicable regulations, inherent risk, and mitigated risk. Update and review classifications annually, or when significant enterprise changes occur that could impact this Safeguard.

</td><td>

BASIC

</td><td>

VRM

</td><td>

core\_company

</td><td>

CIS v8 \(15.3\) CSF \(ID.SC-2\) ISO \(5.19\) PCI \(12.8.5\) CCM \(GRC-02, STA-08\)

</td></tr><tr><td>

CIS Control V8 15.4

</td><td>

Ensure Service Provider Contracts Include Security Requirements:

 Ensure service provider contracts include security requirements. Example requirements may include minimum security program requirements, security incident and/or data breach notification and response, data encryption requirements, and data disposal commitments. These security requirements must be consistent with the enterprise’s service provider management policy. Review service provider contracts annually to ensure contracts are not missing security requirements.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 15.5

</td><td>

Assess Service Providers:

 Assess service providers consistent with the enterprise’s service provider management policy. Assessment scope may vary based on classification\(s\), and may include review of standardized assessment reports, such as Service Organization Control 2 \(SOC 2\) and Payment Card Industry \(PCI\) Attestation of Compliance \(AoC\), customized questionnaires, or other appropriately rigorous processes. Reassess service providers annually, at a minimum, or with new and renewed contracts.

</td><td>

BASIC

</td><td>

VRM

</td><td>

core\_company

</td><td>

CIS v8 \(15.5\) CSF \(ID.SC-4, ID.SC-2\) ISO \(5.19\) NIST \(IA-5\) PCI \(12.8.3\) CCM \(STA-12, STA-13\)

</td></tr><tr><td>

CIS Control V8 15.5

</td><td>

Assess Service Providers:

 Assess service providers consistent with the enterprise’s service provider management policy. Assessment scope may vary based on classification\(s\), and may include review of standardized assessment reports, such as Service Organization Control 2 \(SOC 2\) and Payment Card Industry \(PCI\) Attestation of Compliance \(AoC\), customized questionnaires, or other appropriately rigorous processes. Reassess service providers annually, at a minimum, or with new and renewed contracts.

</td><td>

BASIC

</td><td>

VRM

</td><td>

core\_company

</td><td>

CIS v8 \(15.5\) CSF \(ID.SC-4, ID.SC-2\) ISO \(5.22, 5.23\) NIST \(IA-5\) PCI \(12.8.30\) CCM \(STA-12, STA-13\)

</td></tr><tr><td>

CIS Control V8 15.6

</td><td>

Monitor Service Providers:

 Monitor service providers consistent with the enterprise’s service provider management policy. Monitoring may include periodic reassessment of service provider compliance, monitoring service provider release notes, and dark web monitoring.

</td><td>

BASIC

</td><td>

VRM

</td><td>

core\_company

</td><td>

CIS v8 \(15.6\) CSF \(DE.CM-6\) ISO \(5.2, 5.19, 5.21, 5.22\) NIST \(AC-1\) PCI \(8.2.7, 12.4.2, 12.4.2.1, 12.8.4 CCM \(STA-14\)

</td></tr><tr><td>

CIS Control V8 15.7

</td><td>

Securely Decommission Service Providers:

 Securely decommission service providers. Example considerations include user and service account deactivation, termination of data flows, and secure disposal of enterprise data within service provider systems.

</td><td>

BASIC

</td><td>

VRM

</td><td>

core\_company

</td><td>

CIS v8 \(15.7\) CSF \(PR.AC-1\) ISO \(5.19, 5.2\) NIST \(AC-2, AC-2\(1\)\)

</td></tr><tr><td>

CIS Control V8 16.1

</td><td>

Establish and Maintain a Secure Application Development Process:

 Establish and maintain a secure application development process. In the process, address such items as: secure application design standards, secure coding practices, developer training, vulnerability management, security of third-party code, and application security testing procedures. Review and update documentation annually, or when significant enterprise changes occur that could impact this Safeguard.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 16.1

</td><td>

Apply Secure Design Principles in Application Architectures:

 Apply secure design principles in application architectures. Secure design principles include the concept of least privilege and enforcing mediation to validate every operation that the user makes, promoting the concept of "never trust user input." Examples include ensuring that explicit error checking is performed and documented for all input, including for size, data type, and acceptable ranges or formats. Secure design also means minimizing the application infrastructure attack surface, such as turning off unprotected ports and services, removing unnecessary programs and files, and renaming or removing default accounts.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 16.11

</td><td>

Leverage Vetted Modules or Services for Application Security Components:

 Leverage vetted modules or services for application security components, such as identity management, encryption, and auditing and logging. Using platform features in critical security functions will reduce developers’ workload and minimize the likelihood of design or implementation errors. Modern operating systems provide effective mechanisms for identification, authentication, and authorization and make those mechanisms available to applications. Use only standardized, currently accepted, and extensively reviewed encryption algorithms. Operating systems also provide mechanisms to create and maintain secure audit logs.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 16.12

</td><td>

Implement Code-Level Security Checks:

 Apply static and dynamic analysis tools within the application lifecycle to verify that secure coding practices are being followed.

</td><td>

Manual

</td><td>

NA

</td><td>

 

</td><td>

 

</td></tr><tr><td>

CIS Control V8 16.13

</td><td>

Conduct Application Penetration Testing:

 Conduct application penetration testing. For critical applications, authenticated penetration testing is better suited to finding business logic vulnerabilities than code scanning and automated security testing. Penetration testing relies on the skill of the tester to manually manipulate an application as an authenticated and unauthenticated user. 

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 16.14

</td><td>

Conduct Threat Modeling:

 Conduct threat modeling. Threat modeling is the process of identifying and addressing application security design flaws within a design, before code is created. It is conducted through specially trained individuals who evaluate the application design and gauge security risks for each entry point and access level. The goal is to map out the application, architecture, and infrastructure in a structured way to understand its weaknesses.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 16.2

</td><td>

Establish and Maintain a Process to Accept and Address Software Vulnerabilities:

 Establish and maintain a process to accept and address reports of software vulnerabilities, including providing a means for external entities to report. The process is to include such items as: a vulnerability handling policy that identifies reporting process, responsible party for handling vulnerability reports, and a process for intake, assignment, remediation, and remediation testing. As part of the process, use a vulnerability tracking system that includes severity ratings, and metrics for measuring timing for identification, analysis, and remediation of vulnerabilities. Review and update documentation annually, or when significant enterprise changes occur that could impact this Safeguard.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vul\_remediation\_task

</td><td>

CIS v8 \(16.2\) CSF \(RS.AN-5\) ISO \(8.8\) NIST \(AC-2\) PCI \(6.3.1\) CCM \(AIS-07, AIS-03\)

</td></tr><tr><td>

CIS Control V8 16.3

</td><td>

Perform Root Cause Analysis on Security Vulnerabilities:

 Perform root cause analysis on security vulnerabilities. When reviewing vulnerabilities, root cause analysis is the task of evaluating underlying issues that create vulnerabilities in code, and allows development teams to move beyond just fixing individual vulnerabilities as they arise.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 16.4

</td><td>

Establish and Manage an Inventory of Third-Party Software Components:

 Establish and manage an updated inventory of third-party components used in development, often referred to as a “bill of materials,” as well as components slated for future use. This inventory is to include any risks that each third-party component could pose. Evaluate the list at least monthly to identify any changes or updates to these components, and validate the component is still supported. 

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 16.5

</td><td>

Use Up-to-Date and Trusted Third-Party Software Components:

 Use up-to-date and trusted third-party software components. When possible, choose established and proven frameworks and libraries that provide adequate security. Acquire these components from trusted sources or evaluate the software for vulnerabilities before use.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 16.6

</td><td>

Establish and Maintain a Severity Rating System and Process for Application Vulnerabilities:

 Establish and maintain a severity rating system and process for application vulnerabilities that facilitates prioritizing the order in which discovered vulnerabilities are fixed. This process includes setting a minimum level of security acceptability for releasing code or applications. Severity ratings bring a systematic way of triaging vulnerabilities that improves risk management and helps ensure the most severe bugs are fixed first. Review and update the system and process annually.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vul\_vulnerable\_item

</td><td>

CIS v8 \(16.6\) CSF \(RS.AN-1\) ISO \(8.8\) NIST \(AC-19\) PCI \(6.3.1\) CCM \(AIS-07, TVM-08\)

</td></tr><tr><td>

CIS Control V8 16.7

</td><td>

Use Standard Hardening Configuration Templates for Application Infrastructure:

 Use standard, industry-recommended hardening configuration templates for application infrastructure components. This includes underlying servers, databases, and web servers, and applies to cloud containers, Platform as a Service \(PaaS\) components, and SaaS components. Do not allow in-house developed software to weaken configuration hardening.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 16.8

</td><td>

Separate Production and Non-Production Systems:

 Maintain separate environments for production and non-production systems.

</td><td>

SCRIPTED

</td><td>

CMDB

</td><td>

cmdb\_ci

</td><td>

CIS v8 \(16.8\) CSF \(PR.DS-7\) ISO \(8.31\) NIST \(IA-2\(2\)\) PCI \(6.5.3\) CCM \(IVS-05\)

</td></tr><tr><td>

CIS Control V8 16.9

</td><td>

Train Developers in Application Security Concepts and Secure Coding:

 Ensure that all software development personnel receive training in writing secure code for their specific development environment and responsibilities. Training can include general security principles and application security standard practices. Conduct training at least annually and design in a way to promote security within the development team, and build a culture of security among the developers.

</td><td>

BASIC

</td><td>

Learning Core

</td><td>

sn\_lc\_user\_course\_activity

</td><td>

CIS v8 \(16.9\) CSF \(PR.AT-1, PR.AT-2\) ISO \(8.28\) NIST \(IA-2\(1\)\) PCI \(6.2.2\)

</td></tr><tr><td>

CIS Control V8 17.1

</td><td>

Designate Personnel to Manage Incident Handling:

 Designate one key person, and at least one backup, who will manage the enterprise’s incident handling process. Management personnel are responsible for the coordination and documentation of incident response and recovery efforts and can consist of employees internal to the enterprise, third-party vendors, or a hybrid approach. If using a third-party vendor, designate at least one person internal to the enterprise to oversee any third-party work. Review annually, or when significant enterprise changes occur that could impact this Safeguard.

</td><td>

BASIC

</td><td>

SIR

</td><td>

sys\_user\_has\_role

</td><td>

CIS v8 \(17.1\) CSF \(PR.IP-9, DE.DP-1\) ISO \(5.24\) NIST \(AC-5\) PCI \(12.10.3, 12.10.4\) CCM \(BCR-01, SEF-03\)

</td></tr><tr><td>

CIS Control V8 17.2

</td><td>

Establish and Maintain Contact Information for Reporting Security Incidents:

 Establish and maintain contact information for parties that need to be informed of security incidents. Contacts may include internal staff, third-party vendors, law enforcement, cyber insurance providers, relevant government agencies, Information Sharing and Analysis Center \(ISAC\) partners, or other stakeholders. Verify contacts annually to ensure that information is up-to-date.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 17.3

</td><td>

Establish and Maintain an Enterprise Process for Reporting Incidents:

 Establish and maintain an enterprise process for the workforce to report security incidents. The process includes reporting timeframe, personnel to report to, mechanism for reporting, and the minimum information to be reported. Ensure the process is publicly available to all of the workforce. Review annually, or when significant enterprise changes occur that could impact this Safeguard.

</td><td>

BASIC

</td><td>

SIR

</td><td>

kb\_knowledge

</td><td>

CIS v8 \(17.3\) CSF \(PR.IP-9, PR.AT-1\) ISO \(6.8\) NIST \(AC-6\(1\)\) PCI \(12.10\)

</td></tr><tr><td>

CIS Control V8 17.4

</td><td>

Establish and Maintain an Incident Response Process:

 Establish and maintain an incident response process that addresses roles and responsibilities, compliance requirements, and a communication plan. Review annually, or when significant enterprise changes occur that could impact this Safeguard.

</td><td>

Manual

</td><td>

SIR

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 17.5

</td><td>

Assign Key Roles and Responsibilities:

 Assign key roles and responsibilities for incident response, including staff from legal, IT, information security, facilities, public relations, human resources, incident responders, and analysts, as applicable. Review annually, or when significant enterprise changes occur that could impact this Safeguard.

</td><td>

BASIC

</td><td>

SIR

</td><td>

sys\_user\_has\_role

</td><td>

CIS v8 \(17.5\) CSF \(DE.DP-4, RS.CO-2, RS.CO-3, RS.CO-4\) ISO \(5.2, 5.24\) NIST \(AU-9\(4\)\) PCI \(12.10.3\) CCM \(SEF-03\)

</td></tr><tr><td>

CIS Control V8 17.6

</td><td>

Define Mechanisms for Communicating During Incident Response:

 Determine which primary and secondary mechanisms will be used to communicate and report during a security incident. Mechanisms can include phone calls, emails, or letters. Keep in mind that certain mechanisms, such as emails, can be affected during a security incident. Review annually, or when significant enterprise changes occur that could impact this Safeguard.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 17.7

</td><td>

Conduct Routine Incident Response Exercises:

 Plan and conduct routine incident response exercises and scenarios for key personnel involved in the incident response process to prepare for responding to real-world incidents. Exercises need to test communication channels, decision making, and workflows. Conduct testing on an annual basis, at a minimum.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 17.8

</td><td>

Conduct Post-Incident Reviews:

 Conduct post-incident reviews. Post-incident reviews help prevent incident recurrence through identifying lessons learned and follow-up action.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 17.9

</td><td>

Establish and Maintain Security Incident Thresholds:

 Establish and maintain security incident thresholds, including, at a minimum, differentiating between an incident and an event. Examples can include: abnormal activity, security vulnerability, security weakness, data breach, privacy incident, etc. Review annually, or when significant enterprise changes occur that could impact this Safeguard.

</td><td>

BASIC

</td><td>

SIR

</td><td>

sn\_si\_calculator

</td><td>

CIS v8 \(17.9\) CSF \(RS.AN-5\) ISO \(5.24, 5.25\) NIST \(RA-5\) PCI \(12.10.5\) CCM \(SEF-05\)

</td></tr><tr><td>

CIS Control V8 18.1

</td><td>

Establish and Maintain a Penetration Testing Program:

 Establish and maintain a penetration testing program appropriate to the size, complexity, and maturity of the enterprise. Penetration testing program characteristics include scope, such as network, web application, Application Programming Interface \(API\), hosted services, and physical premise controls; frequency; limitations, such as acceptable hours, and excluded attack types; point of contact information; remediation, such as how findings will be routed internally; and retrospective requirements.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 18.2

</td><td>

Perform Periodic External Penetration Tests:

 Perform periodic external penetration tests based on program requirements, no less than annually. External penetration testing must include enterprise and environmental reconnaissance to detect exploitable information. Penetration testing requires specialized skills and experience and must be conducted through a qualified party. The testing may be clear box or opaque box.

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vul\_remediation\_task

</td><td>

CIS v8 \(18.2\) ISO \(8.8\) NIST \(RA-7\) PCI \(11.4.3\)

</td></tr><tr><td>

CIS Control V8 18.3

</td><td>

Remediate Penetration Test Findings:

 Remediate penetration test findings based on the enterprise’s policy for remediation scope and prioritization.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 18.4

</td><td>

Validate Security Measures:

 Validate security measures after each penetration test. If deemed necessary, modify rulesets and capabilities to detect the techniques used during testing.

</td><td>

Manual

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr><tr><td>

CIS Control V8 18.5

</td><td>

Perform Periodic Internal Penetration Tests:

 NA

</td><td>

BASIC

</td><td>

VR

</td><td>

sn\_vul\_remediation\_task

</td><td>

CIS v8 \(18.5\) ISO \(8.8\) NIST \(RA-5\) PCI \(11.4.2\)

</td></tr></tbody>
</table>## Indicator templates for CIS v7 Controls

The following tables list the Basic and Script indicator templates for CIS v7 Controls.

**Note:** Controls currently not covered by either basic or scripted indicator templates have manual indicator templates defined for the purposes of compliance validation.

<table id="table_pj1_ysx_54b"><thead><tr><th>

Control

</th><th>

Name/Description

</th><th>

Compliance validated by

</th><th>

Source table

</th><th>

Related UCF IDs

</th></tr></thead><tbody><tr><td>

CIS Control 1.1

</td><td>

Utilize an Active Discovery Tool:Utilize an active discovery tool to identify devices connected to the organization's network and update the hardware asset inventory.

</td><td>

Configuration Management \(CMDB\)

</td><td>

CMDB Discovery \[cmdb\_discovery\]

</td><td>

07054

 00693

</td></tr><tr><td>

CIS Control 1.2

</td><td>

Use a Passive Asset Discovery Tool: Utilize a passive discovery tool to identify devices connected to the organization's network and automatically update the organization's hardware asset inventory.

</td><td>

Discovery

</td><td>

Network Discovery Tracking \[discovery\_network\_track\]

</td><td>

01472

</td></tr><tr><td>

CIS Control 1.4

</td><td>

Maintain Detailed Asset Inventory:Maintain an accurate and up-to-date inventory of all technology assets with the potential to store or process information. This inventory shall include all hardware assets, whether connected to the organization's network or not.

</td><td>

Configuration Management \(CMDB\)

</td><td>

Hardware \[cmdb\_ci\_hardware\]

</td><td>

06631

 00691

</td></tr><tr><td>

CIS Control 1.5

</td><td>

Maintain Asset Inventory Information:Ensure that the hardware asset inventory records the network address, hardware address, machine name, data asset owner, and department for each asset and whether the hardware asset has been approved to connect to the network.

</td><td>

Configuration Management \(CMDB\)

</td><td>

Base Configuration Item \[cmdb\]

</td><td>

06638

 06640

 12084

 06636

 13721

 13722

</td></tr><tr><td>

CIS Control 1.7

</td><td>

Deploy Port Level Access Control:Utilize port level access control, following 802.1x standards, to control which devices can authenticate to the network. The authentication system shall be tied into the hardware asset inventory data to ensure only authorized devices can connect to the network.

</td><td>

Configuration Management \(CMDB\)

</td><td>

ACL Endpoint \[cmdb\_ci\_endpoint\_acl\]

</td><td>

11841

 13718

</td></tr><tr><td>

CIS Control 1.8

</td><td>

Utilize Client Certificates to Authenticate Hardware Assets:Use client certificates to authenticate hardware assets connecting to the organization's trusted network.

</td><td>

Certification Core

</td><td>

Audit \[cert\_audit\]

</td><td>

01429

</td></tr><tr><td>

CIS Control 2.1

</td><td>

Maintain Inventory of Authorized Software:Maintain an up-to-date list of all authorized software that is required in the enterprise for any business purpose on any business system.

</td><td>

Configuration Management \(CMDB\)

</td><td>

Application Software \[cmdb\_ci\_application\_software\]

</td><td>

12093

 13723

</td></tr><tr><td>

CIS Control 2.2

</td><td>

Ensure Software is Supported by Vendor:Ensure that only software applications or operating systems currently supported by the software's vendor are added to the organization's authorized software inventory. Unsupported software should be tagged as unsupported in the inventory system.

</td><td>

Software Asset Management

</td><td>

Software Product Lifecycle \[sam\_sw\_product\_lifecycle\]

</td><td>

07054

</td></tr><tr><td>

CIS Control 2.3

</td><td>

Utilize Software Inventory Tools:Utilize software inventory tools throughout the organization to automate the documentation of all software on business systems.

</td><td>

Configuration Management \(CMDB\)

</td><td>

Application Software \[cmdb\_ci\_application\_software\]

</td><td>

11736

 12196

 13720

 13725

</td></tr><tr><td>

CIS Control 2.4

</td><td>

Track Software Inventory Information:The software inventory system should track the name, version, publisher, and installation date for all software, including operating systems authorized by the organization.

</td><td>

Software Asset Management Core

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

12085

</td></tr><tr><td>

CIS Control 2.5

</td><td>

Integrate Software and Hardware Asset Inventories:The software inventory system should be tied into the hardware asset inventory so all devices and associated software are tracked from a single location.

</td><td>

Configuration Management \(CMDB\)

</td><td>

Application Software \[cmdb\_ci\_application\_software\]

</td><td>

11637

 11857

</td></tr><tr><td>

CIS Control 3.1

</td><td>

Run Automated Vulnerability Scanning Tools:Utilize an up-to-date SCAP-compliant vulnerability scanning tool to automatically scan all systems on the network on a weekly or more frequent basis to identify all potential vulnerabilities on the organization's systems.

</td><td>

Vulnerability Response

</td><td>

Vulnerability Data Source Import Queue Entry \[sn\_vul\_ds\_import\_q\_entry\]

</td><td>

10635

</td></tr><tr><td>

CIS Control 3.2

</td><td>

Perform Authenticated Vulnerability Scanning:Perform authenticated vulnerability scanning with agents running locally on each system or with remote scanners that are configured with elevated rights on the system being tested.

</td><td>

Security Operations

</td><td>

Discovered Item \[sn\_sec\_cmn\_src\_ci\]

</td><td>

00706

</td></tr><tr><td>

CIS Control 3.6

</td><td>

Compare Back-to-back Vulnerability Scans:Regularly compare the results from back-to-back vulnerability scans to verify that vulnerabilities have been remediated in a timely manner.

</td><td>

Vulnerability Response

</td><td>

Vulnerability Remediation Status \[sn\_vul\_m2m\_ttr\_status\]

</td><td>

06080

</td></tr><tr><td>

CIS Control 4.2

</td><td>

Change Default PasswordsBefore deploying any new asset, change all default passwords to have values consistent with administrative level accounts.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

01698

 12122

</td></tr><tr><td>

CIS Control 4.4

</td><td>

Use Unique PasswordsWhere multi-factor authentication is not supported \(such as local administrator, root, or service accounts\), accounts will use passwords that are unique to that system.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

01915

 01337

</td></tr><tr><td>

CIS Control 4.8

</td><td>

Log and Alert on Changes to Administrative Group MembershipConfigure systems to issue a log entry and alert when an account is added to or removed from any group assigned administrative privileges.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

06312

</td></tr><tr><td>

CIS Control 4.9

</td><td>

Log and Alert on Unsuccessful Administrative Account LoginConfigure systems to issue a log entry and alert on unsuccessful logins to an administrative account.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

06312

 06331

</td></tr><tr><td>

CIS Control 6.2

</td><td>

Activate audit logging:Ensure that local logging has been enabled on all systems and networking devices.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

00897

</td></tr><tr><td>

CIS Control 6.3

</td><td>

Enable Detailed Logging:Enable system logging to include detailed information such as a event source, date, user, timestamp, source addresses, destination addresses, and other useful elements.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

00575

</td></tr><tr><td>

CIS Control 7.1

</td><td>

Ensure Use of Only Fully Supported Browsers and Email Clients:Ensure that only fully supported web browsers and email clients are allowed to execute in the organization, ideally only using the latest version of the browsers and email clients provided by the vendor.

</td><td>

Vulnerability Response

</td><td>

Application Vulnerable Item \[sn\_vul\_app\_vulnerable\_item\]

</td><td>

00575

 00576

</td></tr><tr><td>

CIS Control 8.1

</td><td>

Utilize Centrally Managed Anti-malware Software Any enterprise class AV software will have this capability. By having a centrally managed AV, you can easily enable individual requirements.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

11861

</td></tr><tr><td>

CIS Control 8.2

</td><td>

Ensure Anti-Malware Software and Signatures are UpdatedThe AV is only as good as it's signatures. While pure signature-based detection is no longer viable, even anomaly-based engines need to be updated on a regular basis. Ensure that the updates are rolled out automatically and use tools to verify that the signatures are actually up-to-date.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

01790

</td></tr><tr><td>

CIS Control 8.3

</td><td>

Enable Operating System Anti-Exploitation Features/ Deploy Anti-Exploit TechnologiesThe DISA hardening guides provide step-by-step instructions on enabling these settings and so much more.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

11637

 10678

</td></tr><tr><td>

CIS Control 8.4

</td><td>

Configure Anti-Malware Scanning of Removable Devices Most AVs have this capability turned on by default, but it's still important to verify that it's actually still enabled. Malware coming in via a USB stick is a viable attack vector for nearly every organization.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

11927

 04824

 06735

 00561

 00564

 04546

</td></tr><tr><td>

CIS Control 8.5

</td><td>

Configure Devices Not To Auto-run ContentFor the same reason why you do not want to scan it, you also don't want it to run when it's mounted. This is a pretty quick setting to enable, and both CIS and DISA hardening guides have step-by-step instructions on disabling auto-run. Some SCM tools can quickly check every endpoint in your environment to make sure this setting is disabled.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

N/A

</td></tr><tr><td>

CIS Control 9.3

</td><td>

Perform Regular Automated Port Scans:Perform automated port scans on a regular basis against all systems and alert if unauthorized ports are detected on a system.

</td><td>

Vulnerability Response

</td><td>

Vulnerability Scanner \[sn\_vul\_scanner\]

</td><td>

N/A

</td></tr><tr><td>

CIS Control 11.3

</td><td>

Use Automated Tools to Verify Standard Device Configurations and Detect ChangesCompare all network device configuration against approved security configurations defined for each network device in use and alert when any deviations are discovered.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

06428

 07058

</td></tr><tr><td>

CIS Control 11.4

</td><td>

Install the Latest Stable Version of Any Security-related Updates on All Network Devices:Install the latest stable version of any security-related updates on all network devices.

</td><td>

Vulnerability Response

</td><td>

Vulnerable Item \[sn\_vul\_vulnerable\_item\]

</td><td>

01696

</td></tr><tr><td>

CIS Control 12.6

</td><td>

Deploy Network-based IDS Sensor:Deploy network-based Intrusion Detection Systems \(IDS\) sensors to look for unusual attack mechanisms and detect compromise of these systems at each of the organization's network boundaries.

</td><td>

Configuration Management \(CMDB\)

</td><td>

Intrusion Detection System \[cmdb\_ci\_ids\_network\]

</td><td>

00581

</td></tr><tr><td>

CIS Control 13.2

</td><td>

Remove Sensitive Data or Systems Not Regularly Accessed by Organization:Remove sensitive data or systems not regularly accessed by the organization from the network. These systems shall only be used as stand alone systems \(disconnected from the network\) by the business unit needing to occasionally use the system or completely virtualized and powered off until needed.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

13726

 13727

</td></tr><tr><td>

CIS Control 13.9

</td><td>

Encrypt Data on USB Storage DevicesProvide the training to employees so they are aware of the risks of data on USB drives. Then provide them with the tools to secure your organization's critical data.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

11927

</td></tr><tr><td>

CIS Control 14.4

</td><td>

Encrypt All Sensitive Information in Transit:Encrypt all sensitive information in transit.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

00564

</td></tr><tr><td>

CIS Control 15.1

</td><td>

Maintain an Inventory of Authorized Wireless Access Points:Maintain an inventory of authorized wireless access points connected to the wired network.

</td><td>

Configuration Management \(CMDB\)

</td><td>

Wireless Access Point \[cmdb\_ci\_wap\_network\]

</td><td>

00693

</td></tr><tr><td>

CIS Control 16.1

</td><td>

Maintain an Inventory of Authentication Systems:Maintain an inventory of each of the organization's authentication systems, including those located onsite or at a remote service provider.

</td><td>

Configuration Management \(CMDB\)

</td><td>

Active Directory Domain Controller \[cmdb\_ci\_ad\_controller\]

</td><td>

13724

</td></tr><tr><td>

CIS Control 16.4

</td><td>

Encrypt or Hash all Authentication Credentials:Encrypt or hash with a salt all authentication credentials when stored.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

06735

</td></tr><tr><td>

CIS Control 16.5

</td><td>

Encrypt Transmittal of Username and Authentication Credentials:Ensure that all account usernames and authentication credentials are transmitted across networks using encrypted channels.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

00564

</td></tr><tr><td>

CIS Control 16.11

</td><td>

Lock Workstation Sessions After Inactivity:Automatically lock workstation sessions after a standard period of inactivity.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

04490

</td></tr><tr><td>

CIS Control 16.13

</td><td>

Alert on Account Login Behavior Deviation:Alert when users deviate from normal login behavior, such as time-of-day, workstation location and duration.

</td><td>

Security Incident Response

</td><td>

Security Incident \[sn\_si\_incident\]

</td><td>

07068

 07070

 07069

</td></tr><tr><td>

CIS Control 18.5

</td><td>

Use Only Standardized and Extensively Reviewed Encryption Algorithms:Use only standardized and extensively reviewed encryption algorithms.

</td><td>

CMDB CI Class Models

</td><td>

Unique Certificate \[cmdb\_ci\_certificate\]

</td><td>

00037

</td></tr><tr><td>

CIS Control 18.8

</td><td>

Establish a Process to Accept and Address Reports of Software Vulnerabilities:Establish a process to accept and address reports of software vulnerabilities, including providing a means for external entities to contact your security group.

</td><td>

Vulnerability Response

</td><td>

Discovery Model Vulnerable Software Match \[sn\_vul\_discovery\_model\_software\_match\]

</td><td>

04810

</td></tr><tr><td>

CIS Control 19.2

</td><td>

Assign Job Titles and Duties for Incident Response:Assign job titles and duties for handling computer and network incidents to specific individuals and ensure tracking and documentation throughout the incident through resolution.

</td><td>

Incident Management

</td><td>

User Roles \[sys\_user\_has\_role\]

</td><td>

07061

 00691

</td></tr><tr><td>

CIS Control 19.3

</td><td>

Designate Management Personnel to Support Incident Handling:Designate management personnel, as well as backups, who will support the incident handling process by acting in key decision-making roles.

</td><td>

Incident Management

</td><td>

User Roles \[sys\_user\_has\_role\]

</td><td>

01211

</td></tr><tr><td>

CIS Control 19.6

</td><td>

Publish Information Regarding Reporting Computer Anomalies and Incidents:Publish information for all workforce members, regarding reporting computer anomalies and incidents to the incident handling team. Such information should be included in routine employee awareness activities.

</td><td>

Security Incident Response

</td><td>

Knowledge \[kb\_knowledge\]

</td><td>

12093

</td></tr><tr><td>

CIS Control 19.8

</td><td>

Create Incident Scoring and Prioritization Schema:Maintain separate environments for production and non-production systems. Developers should not have unmonitored access to production environments.

</td><td>

Security Incident Response

</td><td>

Security Incident Calculator \[sn\_si\_calculator\]

</td><td>

12093

 13723

</td></tr></tbody>
</table><table id="table_a3c_kly_54b"><thead><tr><th>

Control

</th><th>

Name/Description

</th><th>

Compliance validated by

</th><th>

Source table

</th><th>

Related UCF IDs

</th></tr></thead><tbody><tr><td>

CIS Control 18.9

</td><td>

Separate Production and Non-Production Systems:Maintain separate environments for production and nonproduction systems. Developers should not have unmonitored access to production environments.

</td><td>

Configuration Management \(CMDB\)

</td><td>

Configuration Item \[cmdb\_ci\]

</td><td>

00922

</td></tr></tbody>
</table>## Indicator templates for ISO Controls

The following tables list the Basic and Script indicator templates for ISO Controls.

**Note:** Controls currently not covered by either basic or scripted indicator templates have manual indicator templates defined for the purposes of compliance validation.

<table id="table_zhw_5ny_54b"><thead><tr><th>

Control

</th><th>

Name/Description

</th><th>

Compliance validated by

</th><th>

Source table

</th><th>

Related UCF IDs

</th></tr></thead><tbody><tr><td>

ISO27002 - 5.1.1

</td><td>

Policies for information security:Define an “information security policy” which is approved by management and which sets out the organization’s approach to managing its information security objectives. The information security policy are supported by topic-specific policies, which further mandate the implementation of information security controls to include: access control; information classification \(and handling\); physical and environmental security; backup; information transfer; protection from malware; management of technical vulnerabilities; cryptographic controls; communications security; privacy and protection of personally identifiable information; supplier relationships and end user oriented topics such as: 1\) acceptable use of assets; 2\) clear desk and clear screen; 3\) information transfer; 4\) mobile devices and teleworking; 5\) restrictions on software installations and use.

</td><td>

GRC: Policy and Compliance Management

</td><td>

Compliance Policy \[sn\_compliance\_policy\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 6.1.1

</td><td>

Information security roles and responsibilities:Ensure responsibilities for the protection of individual assets are identified in the asset inventory. Ensure roles and responsibilities for the development and implementation of information security are clearly defined.

</td><td>

GRC: Policy and Compliance Management

</td><td>

Control \[sn\_compliance\_control\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 6.2.1

</td><td>

Mobile device policy:Utilize approved whole disk encryption software to encrypt the hard drive of all mobile devices.

</td><td>

GRC: Policy and Compliance Management

</td><td>

Compliance Policy \[sn\_compliance\_policy\]

</td><td>

07054

 01472

 12109

 06631

 00691

 06638

 06640

 12084

 06636

 13721

 13722

 12093

 11736

 12196

 13720

 13725

 00693

 13724

</td></tr><tr><td>

ISO27002 - 6.2.2

</td><td>

Teleworking:Enforce remote access policies for employees and contractors.

</td><td>

GRC: Policy and Compliance Management

</td><td>

Compliance Policy \[sn\_compliance\_policy\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 7.1.1

</td><td>

Screening:Ensure background verification check are performed for all employees and contractors prior to granting access to company's assets.

</td><td>

Human Resources: Core

</td><td>

HR Talent Management Cases \[sn\_hr\_core\_case\_talent\_management\]

</td><td>

12001

 00897

 04490

 12100

 12099

 04594

 04476

</td></tr><tr><td>

ISO27002 - 7.1.2

</td><td>

Terms and conditions of employment:Ensure all new hire employees or contractors signed and agreed to the terms and conditions of employment, including their responsibility for information security.

</td><td>

Human Resources: Core

</td><td>

sn\_hr\_core\_task

</td><td>

01429

</td></tr><tr><td>

ISO27002 - 8.1.1

</td><td>

Inventory of assets:Ensure that the hardware asset inventory records the network address, hardware address, machine name, data asset owner, and department for each asset and whether the hardware asset has been approved to connect to the network.

</td><td>

Configuration Management \(CMDB\)

</td><td>

Base Configuration Item \[cmdb\]

</td><td>

00562

 00561

 01915

 01337

 01421

 06440

</td></tr><tr><td>

ISO27002 - 8.1.2

</td><td>

Ownership of assets:Ensure that the hardware asset inventory records the network address, hardware address, machine name, data asset owner, and department for each asset and whether the hardware asset has been approved to connect to the network.

</td><td>

Configuration Management \(CMDB\)

</td><td>

Base Configuration Item \[cmdb\]

</td><td>

06080

 01273

</td></tr><tr><td>

ISO27002 - 8.1.3

</td><td>

Acceptable use of assets:Ensure employees and contractors are made aware of the information security requirements of the organizations assets associated with information and information processing facilities and resources. They should be responsible for their use of any information processing resources and of any such use carried out under their responsibility.

</td><td>

GRC: Policy and Compliance Management

</td><td>

Compliance Policy \[sn\_compliance\_policy\]

</td><td>

12001

 00897

 04490

 12100

 12099

 04594

 04476

</td></tr><tr><td>

ISO27002 - 9.3.1

</td><td>

Use of secret authentication information:Use client certificates to authenticate hardware assets connecting to the organization's trusted network.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

01429

</td></tr><tr><td>

ISO27002 - 9.4.2

</td><td>

Secure log-on procedures:Require all remote login access to the organization's network to encrypt data in transit and use multi-factor authentication.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

00562

 00561

 01915

 01337

 01421

 06440

</td></tr><tr><td>

ISO27002 - 9.4.3

</td><td>

Password management system:Where multi-factor authentication is not supported \(such as local administrator, root, or service accounts\), accounts will use passwords that are unique to that system.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

06080

 01273

</td></tr><tr><td>

ISO27002 - 10.1.1

</td><td>

Policy on the use of cryptographic controls:Ensure policy surrounding encryption exist and are applied, implemented and enforced in accordance to data classification requirements.

</td><td>

GRC: Policy and Compliance Management

</td><td>

Compliance Policy \[sn\_compliance\_policy\]

</td><td>

07058

 06428

</td></tr><tr><td>

ISO27002 - 10.1.2

</td><td>

Key management:Ensure management of encryption keys are managed following a formal policy and procedure for the entire lifecycle of the key.

</td><td>

GRC: Policy and Compliance Management

</td><td>

Compliance Policy \[sn\_compliance\_policy\]

</td><td>

00897

 00575

 00576

 11861

 01790

</td></tr><tr><td>

ISO27002 - 11.2.9

</td><td>

Clear desk and clear screen policy:Ensure clear desk policy is adapted by employees and contractors.

</td><td>

GRC: Policy and Compliance Management

</td><td>

Compliance Policy \[sn\_compliance\_policy\]

</td><td>

06312

 00577

 12210

</td></tr><tr><td>

ISO27002 - 12.1.2

</td><td>

Controls against malware:Ensure that only fully supported web browsers and email clients are allowed to execute in the organization, ideally only using the latest version of the browsers and email clients provided by the vendor.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 12.2.1

</td><td>

Controls against malware:Ensure that only fully supported web browsers and email clients are allowed to execute in the organization, ideally only using the latest version of the browsers and email clients provided by the vendor.

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 12.4.1

</td><td>

Event logging:Ensure that local logging has been enabled on all systems and networking devices.

</td><td>

Instance Security Center

</td><td>

Security Dashboard Event Logs \[appsec\_security\_dashboard\_event\_logs\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 12.4.2

</td><td>

Protection of log information:Ensure logs are securely protected from unauthorized access.

</td><td>

 

</td><td>

Access Roles \[sys\_security\_acl\_role\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 12.4.3

</td><td>

Administrator and operator logs:Enforce detailed audit logging for access to sensitive data or changes to sensitive data \(utilizing tools such as File Integrity Monitoring or Security Information and Event Monitoring\).

</td><td>

Configuration Compliance

</td><td>

Configuration Test \[sn\_vulc\_test\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 13.2.1

</td><td>

Information transfer policies and procedures:Ensure formal transfer policies, procedures and controls are in place to protect the transfer of information through the use of all types of communication facilities.

</td><td>

GRC: Policy and Compliance Management

</td><td>

Compliance Policy \[sn\_compliance\_policy\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 14.1.1

</td><td>

Information security requirements analysis and specification:Ensure information security related requirements are included in the requirements for new information systems or enhancements to existing information systems.

</td><td>

GRC: Advanced Risk

</td><td>

Risk Assessments \[sn\_risk\_advanced\_risk\_assessment\_instance\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 14.2.2

</td><td>

Technical review of applications after operating platform changes:Ensure business critical applications are reviewed and tested to ensure there is no adverse impact on organizational operations or security when ever there are changes to the operating platforms.

</td><td>

Change Request

</td><td>

Change Request \[change\_request\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 14.2.3

</td><td>

Restrictions on changes to software packages:Ensure modifications to software packages are discouraged, or limited to necessary changes and all changes are strictly controlled.

</td><td>

Change Request

</td><td>

Change Request \[change\_request\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 14.2.4

</td><td>

System security testing:Ensure security testing such as secure code reviews and vulnerability scan are performed during development lifecycle. Ensure identified vulnerabilities are documented and remediation are performed.

</td><td>

Change Request

</td><td>

Change Request \[change\_request\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 14.2.8

</td><td>

System acceptance testing:Ensure system acceptance testing includes testing of information security requirements and adherence to secure system development practices.

</td><td>

DevOps

</td><td>

Build Test Results \[sn\_devops\_build\_test\_result\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 14.2.9

</td><td>

System acceptance testing:Ensure system acceptance testing includes testing of information security requirements and adherence to secure system development practices.

</td><td>

DevOps

</td><td>

Task Executions \[sn\_devops\_task\_execution\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 15.1.1

</td><td>

Information security policy for supplier relationships:Ensure information security controls are addressed and resolved with the supplier prior to conducting business or granting vendor access to assets.

</td><td>

GRC: Vendor Risk Management

</td><td>

Vendor Risk Assessment \[sn\_vdr\_risk\_asmt\_assessmentsn\_vdr\_risk\_asmt\_assessment\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 15.1.3

</td><td>

Information and communication technology supply chain:Ensure risk assessment are performed to prior to doing business and granting suppliers and vendors access to assets and security controls and requirements are agreed upon and documented in the suppliers/vendors agreement.

</td><td>

GRC: Vendor Risk Management

</td><td>

Vendor Risk Assessment \[sn\_vdr\_risk\_asmt\_assessmentsn\_vdr\_risk\_asmt\_assessment\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 15.2.1

</td><td>

Monitoring and review of supplier services:Ensure supplier are regularly monitoring and review to ensure that the information security terms and conditions of the agreements are being adhered to and that information security incidents and problems are managed properly.

</td><td>

GRC: Vendor Risk Management

</td><td>

Vendor Risk Assessment \[sn\_vdr\_risk\_asmt\_assessmentsn\_vdr\_risk\_asmt\_assessment\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 15.2.2

</td><td>

Managing changes to supplier services:Ensure 3rd Party risk assessment are performed when ever there are changes to provision of services. Ensure changes to the provision of services by suppliers, including maintaining and improving existing information security policies, procedures and controls, are managed.

</td><td>

GRC: Vendor Risk Management

</td><td>

Repeating Assessments \[sn\_vdr\_risk\_asmt\_repeating\_assessment\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 16.1.2

</td><td>

Reporting information security events:Ensure there is a formal Incident Management program in place and all personnel and third parties are trained on how to recognize and report security incidents.

</td><td>

Security Incident Response

</td><td>

Security Incident \[sn\_si\_incident\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 16.1.4

</td><td>

Assessment of and decision on information security events:Ensure there is a formal information security event management to include agreed security event and incident classification scale for reporting and escalation. Ensure threat and risk classification scheme are documented. Ensure incident response notifications are maintained. Ensure impact thresholds to be used in categorizing incidents are documented.

</td><td>

Security Incident Response

</td><td>

Security Incident \[sn\_si\_incident\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 16.1.5

</td><td>

Response to information security incidents:Ensure information security incidents are responded to and managed in accordance with the documented procedures.

</td><td>

Security Incident Response

</td><td>

Security Incident \[sn\_si\_incident\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 16.1.6

</td><td>

Learning from information security incidents:Ensure incident monitoring procedures are included in the Incident Management Program to document incidents and ensuring security event are periodically analyzed to reduce future incident.

</td><td>

Security Incident Response

</td><td>

Security Incident \[sn\_si\_incident\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 17.1.1

</td><td>

Planning information security continuity:Ensure information security and the continuity of information security management are planned and included in business continuity plan or within the disaster recovery plan.

</td><td>

GRC: Business Impact Analysis

</td><td>

Impact Analysis \[sn\_bia\_analysis\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 17.1.2

</td><td>

Implementing information security continuity:Ensure business continuity or disaster recovery plan are formally documented.

</td><td>

GRC: Business Impact Analysis

</td><td>

Impact Analysis \[sn\_bia\_analysis\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 17.1.3

</td><td>

Verify, review and evaluate information security continuity:Ensure business continuity or disaster recovery plan are annual exercise to validate adequate security control are valid and effective during adverse situation.

</td><td>

GRC: Business Impact Analysis

</td><td>

Impact Analysis \[sn\_bia\_analysis\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 17.2.1

</td><td>

Availability of information processing facilities:Ensure failover and recovery components work as intended.

</td><td>

GRC: Crisis Management

</td><td>

Events \[sn\_recovery\_event\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 18.1.3

</td><td>

Protection of records:Ensure records and data are protected from loss, destruction, falsification, unauthorized access and unauthorized release, in accordance with legislator, regulatory, contractual and business requirements.

</td><td>

GRC: Policy and Compliance Management

</td><td>

Compliance Policy \[sn\_compliance\_policy\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 18.1.4

</td><td>

Privacy and protection of personally identifiable information:Ensure privacy and protection of personally identifiable information are protected and handled in accordance with legislation and regulation where applicable.

</td><td>

GRC: Policy and Compliance Management

</td><td>

Compliance Policy \[sn\_compliance\_policy\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 18.2.2

</td><td>

Compliance with security policies and standards:Ensure testing of in scope systems configuration against compliance and regulatory requirements are regularly performed. Ensure baseline configuration standards for systems are documented and based upon industry best practices.

</td><td>

Configuration Compliance

</td><td>

Policies \[sn\_vulc\_policy\]

</td><td>

01422

 01355

</td></tr><tr><td>

ISO27002 - 18.2.3

</td><td>

Technical compliance review:Ensure periodic vulnerability scan and penetration test are performed and testing of in scope systems configuration against compliance and regulatory requirements.

</td><td>

Configuration Compliance

</td><td>

Test Results \[sn\_vulc\_result\]

</td><td>

N/A

</td></tr></tbody>
</table><table id="table_bsh_14y_54b"><thead><tr><th>

Control

</th><th>

Name/Description

</th><th>

Compliance validated by

</th><th>

Source table

</th><th>

Related UCF IDs

</th></tr></thead><tbody><tr><td>

ISO27002 - 8.1.4

</td><td>

Return of assets:Ensure the termination process is formalized to include the return of all previously issued physical and electronic assets owned by or entrusted to the organization.

</td><td>

Human Resources: Core Asset Management

</td><td>

-   HR Profiles \[sn\_hr\_core\_profile\]
-   Asset \[alm\_asset\]

</td><td>

N/A

</td></tr><tr><td>

ISO27002 - 12.1.4

</td><td>

Separation of development, testing and operational environments:Maintain separate environments for production and nonproduction systems. Developers should not have unmonitored access to production environments.

</td><td>

Configuration Management \(CMDB\)

</td><td>

Configuration Item \[cmdb\_ci\]

</td><td>

01698

 12122

 00644

 00596

</td></tr></tbody>
</table>## Indicator templates common to CIS and ISO Controls

The following tables list the Basic and Script indicator templates that are common to both CIS and ISO Controls.

**Note:** Controls currently not covered by either basic or scripted indicator templates have manual indicator templates defined for the purposes of compliance validation.

<table id="table_xsd_wf1_w4b"><thead><tr><th>

Control

</th><th>

Name/Description

</th><th>

Indicator template type

</th><th>

Compliance validated by

</th><th>

Source table

</th><th>

Related UCF IDs

</th></tr></thead><tbody><tr><td>

CIS Control 2.6, ISO27002 - 12.5.1

</td><td>

Address unapproved software:Ensure software assets are managed and regularly updated.

</td><td>

Script

</td><td>

-   Software Asset Management Core
-   Software Asset Management Professional Core

</td><td>

-   Software Installation \[cmdb\_sam\_sw\_install\]
-   Software Models \[cmdb\_software\_product\_model\]

</td><td>

11637

 00656

 11624

</td></tr><tr><td>

CIS Control 3.7, ISO27002 - 12.6.1

</td><td>

Utilize a Risk-rating Process:Utilize a risk-rating process to prioritize the remediation of discovered vulnerabilities.

</td><td>

Basic

</td><td>

Vulnerability Response

</td><td>

Vulnerable Item \[sn\_vul\_vulnerable\_item\]

</td><td>

01273

</td></tr><tr><td>

CIS Control 7.2, ISO27002 - 12.6.2

</td><td>

Restrictions on software installation:Uninstall or disable any unauthorized browser or email client plugins or add-on applications.

</td><td>

Script

</td><td>

-   Software Asset Management Core
-   Software Asset Management Professional Core

</td><td>

-   Software Installation \[cmdb\_sam\_sw\_install\]
-   Software Models \[cmdb\_software\_product\_model\]

</td><td>

00575

 00574

</td></tr><tr><td>

CIS Controls 18.1, ISO27002 - 14.2.1

</td><td>

Establish Secure Coding Practices:Establish secure coding practices appropriate to the programming language and development environment being used.

</td><td>

Basic

</td><td>

GRC: Policy and Compliance Management

</td><td>

Policy \[sn\_compliance\_policy\]

</td><td>

11863

</td></tr><tr><td>

CIS Control 19.1, ISO27002 - 16.1.1

</td><td>

Document Incident Response Procedures:Ensure that there are written incident response plans that defines roles of personnel as well as phases of incident handling/management.

</td><td>

Basic

</td><td>

Security Incident Response

</td><td>

Security Incident \[sn\_si\_incident\]

</td><td>

11780

</td></tr><tr><td>

CIS Control 19.4, ISO27002 - 16.1.3

</td><td>

Reporting information security weaknesses:Devise organization-wide standards for the time required for system administrators and other workforce members to report anomalous events to the incident handling team, the mechanisms for such reporting, and the kind of information that should be included in the incident notification.

</td><td>

Basic

</td><td>

Security Incident Response

</td><td>

Security Incident \[sn\_si\_incident\]

</td><td>

07183

 12975

 10033

</td></tr></tbody>
</table>**Parent Topic:**[Technology Controls Monitoring Accelerator](tech-controls-monitoring-accel.md)

