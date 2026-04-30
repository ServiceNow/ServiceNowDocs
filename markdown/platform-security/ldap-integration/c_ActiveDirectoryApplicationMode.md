---
title: Active Directory Application Mode \(ADAM\)
description: Active Directory Application Mode \(ADAM\) is an Lightweight Directory Access Protocol \(LDAP\)-compliant directory service.
locale: en-US
release: yokohama
product: LDAP integration
classification: ldap-integration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [LDAP integration, Authentication, Access Management]
---

# Active Directory Application Mode \(ADAM\)

Active Directory Application Mode \(ADAM\) is an Lightweight Directory Access Protocol \(LDAP\)-compliant directory service.

**Note:** A basic level of understanding with Microsoft Windows Server and Active Directory is needed for understanding this topic. You must also have administrator permissions on the server you are configuring for ADAM.

These are sample procedures. Due to installation and environment variations, we cannot offer direct support. We recommend working with a Microsoft consultant.

ADAM has a simple install and runs as a service on Windows operating systems. It can be fully customized and distributed as an application component or used as a stand-alone LDAP directory. ADAM uses the same technologies found on Active Directory Domain Controllers \(including replication and delegation features\) and has its own administration and customization features. It can be run as a Windows service. ADAM can be installed on Windows XP, 2000, 2003, and 2008 operating systems. ADAM is included as part of Windows Server 2003 R2 and Windows Server 2008. A download is available at [http://www.microsoft.com/downloads](http://www.microsoft.com/downloads)http://www.microsoft.com/downloads for earlier operating systems.

## Security

Some company security policies prohibit external vendors and partners from connecting directly to an Active Directory \(AD\) Domain Controller. If exposing certain AD objects or attributes to an external vendor or partner is prohibited, access to objects and attributes can be blocked using AD Security Access Control Entries \(ACE or ACL\). Depending on security requirements, this method can introduce complexity in the integration. Consolidating multiple domains and forests is recommended. If all LDAP imports and authentications need to be channeled through a single source, ADAM can be used as a consolidated source. With the release of Windows 2008 this functionality has been renamed to Light-Weight-Directory Service, LDS. Installation and configuration is similar to Windows Server 2003 R2.

## Recommended Knowledge

For this task, you must understand AD, object classes and attributes. To have a successful integration, you need to be knowledgeable of the current AD object structure, familiar with Active Directory delegations, and have a strategy on how to use ADAM and for what purposes. If you are not familiar with AD or ADAM, work with your AD administrator to configure a new ADAM environment.

## Trusts

If userProxy objects is used, the computer hosting ADAM needs to be a member of the domain that has the AD accounts, or a member of a trusted domain.

## Internal Connectivity

If userProxy objects is used, the ADAM computer must be able to connect to the related Domain Controllers to perform proxy authentication.

**Related topics**  


[http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&amp;displaylang=en%7C](http://www.microsoft.com/downloads/en/details.aspx?familyid=9688f8b9-1034-4ef6-a3e5-2a2a57b5c8e4&displaylang=en%7C)

