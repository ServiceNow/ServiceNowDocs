---
title: Understanding LDAP integration
description: An LDAP integration allows your instance to use your existing LDAP server as the primary source of user data.
locale: en-US
release: xanadu
product: LDAP integration
classification: ldap-integration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [LDAP integration, Authentication, Access Management]
---

# Understanding LDAP integration

An LDAP integration allows your instance to use your existing LDAP server as the primary source of user data.

## LDAP integration prerequisites

-   The directory services server must be LDAP v3 compliant
-   Inbound network access through the firewall must be allowed \(to the LDAP server\)
-   External IP or Name of the LDAP server
-   User credentials with read-only access
-   For LDAPS, a PKI certificate

## LDAP integration timing

LDAP integrations are usually done before the instance Go Live, but can be integrated at any time.

## LDAP server data integrity

Some users are concerned about a third party \(the instance in this case\) making changes \(writing\) to your LDAP server. In an LDAP integration, your instance does not write to the internal LDAP directory. The instance queries for information, and updates its database accordingly.

No changes are made to the internal LDAP server by the instance. The service account is read only.

Most changes \(including additions\) to your LDAP server are available to the instance within seconds, depending on how many components of the full LDAP integration are in place.

To keep LDAP records synchronized, schedule a periodic scan of the LDAP server to pick up changes.

The instance does not synchronize department records. Users and group memberships are kept up-to-date by the LDAP Listener mechanism and a daily full LDAP Browse, but the instance does not delete any of these entries once they disappear from LDAP.

If an entry were to be deleted, the entire history would also get deleted, and any references to it would be cleared or deleted. Configuration Items \(CIs\), SLA Agreements, Software Licenses, Purchase Orders, and Service Catalog Entries all have a reference to Department, and if Department is deleted, then those references get cleared. There are many references to Users, and so deleting a user would lose all history of what that user did. Currently, the decision to delete or not to delete is made by our customers.

## Security

The connection is made from a single machine using a fixed IP address through a specific port on your firewall. Authentication is done with a read-only LDAP account of your choosing. You can use standard LDAP, or load the public side of an [SSL certificate installed on your directory](../task/t_UploadTheX509SSLCertificate.md), in which case we can use LDAPS. To add another layer of security, we also offer the option of a point-to-point IPSEC VPN tunnel. Speak to your account manager for details and pricing.

|Connection|Description|
|----------|-----------|
|MID Server|To shield your LDAP server from external network traffic, install a MID Server on the local network and configure the system to communicate with the MID Server over a secure channel.|
|LDAPS|To establish an encrypted LDAPS connection, load the public side of your LDAP server's SSL certificate. The integration uses the certificate to encrypt all communication between the LDAP server and the instance.|
|VPN|To secure the LDAP server with an encrypted point-to-point IPSEC VPN tunnel, speak to your account manager for details and pricing.|

Another security aspect to consider is the data shared in an LDAP integration. To limit the data exposed to your instance, specify attributes in your transform map. For more information, see [LDAP transform maps](../concept/c_LDAPTransformMaps.md).

## Importing LDAP data to the instance

It is recommended that attributes are defined to import only required data. Defined attributes get mapped into the instance user database.

We cannot answer the question of which specific attributes are needed because this is determined by the scope of the project and business requirements.

## Supported types of LDAP servers

The instance has successfully integrated with Microsoft Active Directory, Novell, Domino \(Lotus Notes\), and Open LDAP. We use JNDI to interface with the LDAP Server. As long as your LDAP server is LDAP v3 compliant, the integration is successful.

## LDAP single-sign-on

Along with the data population functionality provided with the LDAP import, you can use the External Authentication functionality supported by the application to prevent your users from needing to sign on each time.

## Multiple LDAP domains

The recommended method for handling multiple domains is to create a separate LDAP server record for each domain. Each LDAP server record must point to a domain controller for that domain. This means the local network must allow connections to each of the domain controllers.

After expanding to more than one network domain, it is critical that you identify unique LDAP attributes for the application usernames and import coalesce values. A common unique coalesce attribute for Active Directory is [objectSid](http://msdn.microsoft.com/en-us/library/windows/desktop/ms679024(v=vs.85).aspx). Unique usernames may vary based on the LDAP data design. Common attributes are `email` or `userPrincipalName`.

## Handling query limits

By default, Active Directory 2000/2003 has an LDAP query limit \([maxPageSize](http://support.microsoft.com/kb/315071)\) of 1000 objects to prevent excessive loads and denial of service attacks. We have two methods of dealing with this limit.

The default method is to break up the query to return less than 1000 objects at a time. For example, query only for object starting with the letter 'a', then query for 'b' objects. The more efficient method for large environments is to enable paging. Paging is supported by default on all Microsoft Active Directory servers. It automatically splits the results into multiple result sets, so we don't have to split up the query into multiple requests.

## LDAP query type

If an LDAP password is supplied then a "Simple Bind" is performed. If no LDAP password is supplied then "none" is used, in which case the LDAP server must allow anonymous login.

## LDAP authentication

We use provided service account credentials for LDAP to retrieve the user DN from the LDAP server. Given the DN value for the user, we then rebind with LDAP given the users DN and the provided password.

## Password storage

The password that the user enters is contained entirely in their HTTPS session. We do not store that password anywhere.

## Setting up LDAP authentication

These fields on the user record pertain to LDAP:

-   **Source**: The Source field identifies whether or not a user is validated using LDAP. If the source field starts with "ldap", then the user is validated via LDAP. If the Source field does not start with "ldap", then the password on the user record is used to validate the user upon login.
-   **LDAP Server**: The instance supports multiple LDAP servers, so the LDAP Server field determines which server should be used to authenticate the user.

