---
title: LDAP integration requirements
description: Review the requirements for LDAP integration, which include a PKI certificate an LDAP compliant directory services server.
locale: en-US
release: xanadu
product: LDAP integration
classification: ldap-integration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [LDAP integration, Authentication, Access Management]
---

# LDAP integration requirements

Review the requirements for LDAP integration, which include a PKI certificate an LDAP compliant directory services server.

LDAP integration requires:

-   An LDAP v3 compliant directory services server
    -   Allows inbound network access through the firewall \(to the LDAP server\)
    -   \(Optional\) Accepts anonymous login
    -   \(Optional\) Supports paging for large LDAP queries
-   The external IP address or fully-qualified domain name of the LDAP server. You can also use a [MID server](../concept/c_LDAPIntegrationViaMIDServer.md).
-   A read-only LDAP account of your choosing
-   For multiple domains, network access for each domain controller
-   For LDAPS, a PKI certificate
-   For LDAP listener, a Microsoft Active Directory server that supports persistent queries \(ADNotify\)

## Supported LDAP servers

Using JNDI to interface with the LDAP server, the instance has successfully integrated with the following servers:

-   Microsoft Active Directory
-   Novell
-   Domino \(Lotus Notes\)
-   Open LDAP

## LDAP query limits

By default, Active Directory 2000/2003 has an LDAP query limit \([maxPageSize](http://support.microsoft.com/kb/315071)\) of 1000 objects to prevent excessive loads and denial of service attacks. The system has two methods of dealing with this limit.

-   The default method is to break up the query to return fewer than 1000 objects at a time. For example, query only for objects starting with the letter a, then query for b objects.
-   The more efficient method for large environments is to enable paging, which is supported by default on all Microsoft Active Directory servers. Paging automatically splits the results into multiple result sets so the integration does not have to split up the query into multiple requests.

