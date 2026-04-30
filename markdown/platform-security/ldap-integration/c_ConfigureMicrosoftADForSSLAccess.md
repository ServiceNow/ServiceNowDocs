---
title: Configure Microsoft Active Directory for secure LDAPS communication
description: Use certificate pairs to enable Microsoft Active Directory \(AD\) LDAPS communications.
locale: en-US
release: zurich
product: LDAP integration
classification: ldap-integration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [LDAP integration, Authentication, Access Management]
---

# Configure Microsoft Active Directory for secure LDAPS communication

Use certificate pairs to enable Microsoft Active Directory \(AD\) LDAPS communications.

**Note:** These procedures were designed and tested using Windows 2003 R2 Standard Edition and work with all versions of Windows 2003.

Secure LDAP \(LDAPS\) communication is similar to SSL \(HTTPS\) communication in that both encrypt the data between servers and clients. To accomplish this, the server and clients share common information by using certificate pairs. The server holds the private key certificate and the clients hold the public key certificate. These certificates are required to enable Microsoft Active Directory \(AD\) LDAPS communications.

To configure LDAPS for Active Directory you must:

-   Ensure that the Active Directory domain is set up and that the instance is able to connect to the Active Directory server through the firewall.
-   Verify that there is a Certificate Authority \(CA\) that can issue a certificate for the domain controller \(DC\). If you don't already have a CA infrastructure there are two options.
    -   Setup a stand-alone CA to issue the certificate
    -   Request a third party certificate
-   If you already have a CA in place, you can generate a certificate from an internal CA.

All certificates have a defined expiration date which can be viewed in the certificate properties. If the certificate expires, all LDAPS traffic fails, and your users can no longer log into the instance. To resolve this, a new certificate must be issued and installed on your instance.

The default expiration for Microsoft CA certificates is one year. External CA certificates are usually purchased in one year increments. Note when your certificate expires, or use the application's Expiration Notification function \(located in **System LDAP** &gt; **Certificates**\). Ensure that you have a new certificate ready before the old one expires. This gives you time to install and test the new certificate before the old one expires.

